<template>
    <div ref="canvasHolder" class="canvasHolder">
        <div ref="canvas" class="canvas"></div>
    </div>
</template>

<script>
import * as THREE from 'three'

export default {
    name: 'Globe',
    components: {},
    props: {},
    data() {
        return {
            camera: null,
            cameraHolder: null,
            scene: null,
            world: null,
            renderer: null,
            container: null,
            controls: null,
            sunLight: null,
            ambientLight: null,
            globe: null,
        }
    },
    computed: {},
    watch: {},
    mounted() {
        const self = this
        if (process.browser) {
            self.$nextTick(function () {
                self.init()
            })
        }
    },
    methods: {
        init() {
            this.container = this.$refs.canvas
            this.scene = new THREE.Scene()
            this.renderer = new THREE.WebGLRenderer()
            this.renderer.setSize(
                this.container.clientWidth,
                this.container.clientHeight
            )
            this.container.appendChild(this.renderer.domElement)

            this.camera = new THREE.PerspectiveCamera(
                75,
                this.container.clientWidth / this.container.clientHeight,
                0.1,
                1000
            )

            this.camera.position.z = 150;
            
            this.createWorld()

            window.addEventListener('resize', this.resize, false)
        },

        async createWorld() {
            var spotLight = new THREE.SpotLight(0xffffff);
            spotLight.position.set(100,100,100);
            spotLight.castShadow = true;
            spotLight.shadowMapWidth = 1024;
            spotLight.shadowMapHeight = 1024;
            spotLight.shadowCameraNear = 600;
            spotLight.shadowCameraFar = 5000;
            spotLight.shadowCameraFov = 90;
            this.scene.add(spotLight)

            const material = new THREE.MeshPhongMaterial({
                color      : new THREE.Color("rgb(102,33,33)"),  
                emissive   : new THREE.Color("rgb(102, 153, 153)"),
                specular   : new THREE.Color("rgb(133,33,33)"),
                wireframe  : true,                                  
                transparent: true,
                opacity    : 0.33                                 
            });


            var geometry = new THREE.SphereGeometry(50,22,22,0,Math.PI*2.77,0,Math.PI*2.23);
            this.globe = new THREE.Mesh(geometry, material);
            this.globe.position.set(0, 0.501, 0)
            this.globe.rotation.set(0, 0, 0)
            this.globe.castShadow = true
            this.scene.add(this.globe)


            await this.renderer.setAnimationLoop(this.render.bind(this))
            this.resize()

            this.$root.$emit('finished-loading')
        },
        render(timestamp, frame) {
            const self = this
            
            self.renderer.render(self.scene, self.camera)
            self.globe.rotation.y += 0.01337;
            self.renderer.setAnimationLoop(self.render.bind(self))
        },
        resize() {
            const self = this
            self.camera.aspect =
                self.container.clientWidth / self.container.clientHeight
            self.camera.updateProjectionMatrix()
            self.renderer.setSize(
                self.container.clientWidth,
                self.container.clientHeight
            )
        },
    },
}
</script>

<style lang="scss" scoped>
.canvasHolder {
    height: 360px;
    overflow: hidden;
    background: #000;
}
.canvas {
    position: absolute;
    top: 30px;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: all;
    z-index: 0;
}
</style>