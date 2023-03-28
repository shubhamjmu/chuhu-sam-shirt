<template>
<div class="container-fluid">
    <div class="px-lg-2 px-sm-2 pb-5">
        <div class="header pt-5 pb-4">
            <p class="font1 text-center">Customize shirt</p>
            <!-- heading-->
        </div>
        <div class="row">
            <div class="col-lg-4 col-12 bg-pink">
                <!-- 1st box -->
                <!----first editing box---->
                <div class="tabbable">
                    <nav class="nav nav-pills d-flex justify-content-center pt-4" role="tablist" id="nav-tab">
                        <!-- nav tabs-->
                        <button class=" nav-link" data-bs-toggle="tab" data-bs-target="#tab1" type="button" role="tab" aria-selected="false">
                            Color
                        </button>
                        <button class=" active nav-link" data-bs-toggle="tab" data-bs-target="#tab2" type="button" role="tab" aria-selected="true" tabindex="-1">
                            Add Text and Graphics
                        </button>
                    </nav>

                    <!-- tables-->
                    <div class="tab-content " style="background-color:#f5f5f5;">

                        <div class="tab-pane  " id="tab1">
                            <details data-key="images">
                                <!-- different shirts corner -->
                                <summary class="p-3">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-images" viewBox="0 0 16 16">
                                        <path d="M4.502 9a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" />
                                        <path d="M14.002 13a2 2 0 0 1-2 2h-10a2 2 0 0 1-2-2V5A2 2 0 0 1 2 3a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2v8a2 2 0 0 1-1.998 2zM14 2H4a1 1 0 0 0-1 1h9.002a2 2 0 0 1 2 2v7A1 1 0 0 0 15 11V3a1 1 0 0 0-1-1zM2.002 4a1 1 0 0 0-1 1v8l2.646-2.354a.5.5 0 0 1 .63-.062l2.66 1.773 3.71-3.71a.5.5 0 0 1 .577-.094l1.777 1.947V5a1 1 0 0 0-1-1h-10z" />
                                    </svg>
                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Type of Shirts</span>
                                </summary>
                                <div class="well" style="display: flex; flex-wrap:wrap;">
                                    <select id="tshirttype ">
                                        <option value="./" selected="selected" v-on:click="shirt()">
                                            Men's Long Sleeves shirt
                                        </option>
                                        <option value="./" selected="selected">
                                            Men's Short Sleeves shirt
                                        </option>
                                        <option value="./" selected="selected">
                                            Women's Long Sleevs shirt
                                        </option>
                                        <option value="./" selected="selected">
                                            Women's short Sleevs shirt
                                        </option>
                                    </select>
                                </div>
                            </details>

                            <details data-key="color">
                                <!-- colors -->
                                <summary class="p-3">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="18" fill="currentColor" class="bi bi-palette" viewBox="0 0 16 16">
                                        <path d="M8 5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zm4 3a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zM5.5 7a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm.5 6a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" />
                                        <path d="M16 8c0 3.15-1.866 2.585-3.567 2.07C11.42 9.763 10.465 9.473 10 10c-.603.683-.475 1.819-.351 2.92C9.826 14.495 9.996 16 8 16a8 8 0 1 1 8-8zm-8 7c.611 0 .654-.171.655-.176.078-.146.124-.464.07-1.119-.014-.168-.037-.37-.061-.591-.052-.464-.112-1.005-.118-1.462-.01-.707.083-1.61.704-2.314.369-.417.845-.578 1.272-.618.404-.038.812.026 1.16.104.343.077.702.186 1.025.284l.028.008c.346.105.658.199.953.266.653.148.904.083.991.024C14.717 9.38 15 9.161 15 8a7 7 0 1 0-7 7z" />
                                    </svg>
                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Colors</span>
                                </summary>
                                <div class="well" style="display: flex; flex-wrap:wrap;margin:1.5rem">
                                    <div class="tColor" title="White">
                                        <div class="shirtColor" style="background-color: rgb(255, 255, 255);"></div>
                                    </div>
                                    <div class="tColor" title="Ice Grey ">
                                        <div class="shirtColor" style="background-color: rgb(219, 221, 220);"></div>
                                    </div>
                                    <div class="tColor" title="Sport Grey ">
                                        <div class="shirtColor" style="background-color: rgb(178, 171, 179);"></div>
                                    </div>
                                    <div class="tColor" title="Dark Heather Grey ">
                                        <div class="shirtColor" style="background-color: rgb(96, 102, 113);"></div>
                                    </div>
                                    <div class="tColor" title="Charcoal ">
                                        <div class="shirtColor" style="background-color: rgb(90, 86, 87);"></div>
                                    </div>
                                    <div class="tColor" title="Black ">
                                        <div class="shirtColor" style="background-color: rgb(19, 22, 25);"></div>
                                    </div>
                                    <div class="tColor" title="Red">
                                        <div class="shirtColor" style="background-color: rgb(178, 0, 12);"></div>
                                    </div>
                                    <div class="tColor" title="Cradinal Red">
                                        <div class="shirtColor" style="background-color: rgb(99, 9, 40);"></div>
                                    </div>
                                    <div class="tColor" title="Heliconia">
                                        <div class="shirtColor" style="background-color: rgb(247, 62, 134);"></div>
                                    </div>
                                    <div class="tColor" title="Maroon">
                                        <div class="shirtColor" style="background-color: rgb(66, 12, 36);"></div>
                                    </div>
                                    <div class="tColor" title="Light Pink">
                                        <div class="shirtColor" style="background-color: rgb(242, 194, 219);"></div>
                                    </div>
                                    <div class="tColor" title="Purple">
                                        <div class="shirtColor" style="background-color: rgb(77, 35, 121);"></div>
                                    </div>
                                    <div class="tColor" title="Royal">
                                        <div class="shirtColor" style="background-color: rgb(0, 50, 150);"></div>
                                    </div>
                                    <div class="tColor" title="Navy">
                                        <div class="shirtColor" style="background-color: rgb(32, 48, 74);"></div>
                                    </div>
                                    <div class="tColor" title="Light Blue">
                                        <div class="shirtColor" style="background-color: rgb(169, 189, 216);"></div>
                                    </div>
                                    <div class="tColor" title="Carolina Blue">
                                        <div class="shirtColor" style="background-color: rgb(86, 137, 185);"></div>
                                    </div>
                                    <div class="tColor" title="Turquoise">
                                        <div class="shirtColor" style="background-color: rgb(0, 136, 183);"></div>
                                    </div>
                                    <div class="tColor" title="Irish Green">
                                        <div class="shirtColor" style="background-color: rgb(0, 128, 43);"></div>
                                    </div>
                                    <div class="tColor" title="Light Green">
                                        <div class="shirtColor" style="background-color: rgb(13, 58, 21);"></div>
                                    </div>
                                    <div class="tColor" title="Lime">
                                        <div class="shirtColor" style="background-color: rgb(124, 199, 74);"></div>
                                    </div>
                                    <div class="tColor" title="Neon Yellow">
                                        <div class="shirtColor" style="background-color: rgb(204, 243, 55);"></div>
                                    </div>
                                    <div class="tColor" title="Military Green">
                                        <div class="shirtColor" style="background-color: rgb(65, 70, 35);"></div>
                                    </div>
                                    <div class="tColor" title="Yellow">
                                        <div class="shirtColor" style="background-color: rgb(255, 230, 66);"></div>
                                    </div>
                                    <div class="tColor" title="Gold">
                                        <div class="shirtColor" style="background-color: rgb(255, 204, 0);"></div>
                                    </div>
                                    <div class="tColor" title="Natural">
                                        <div class="shirtColor" style="background-color: rgb(253, 245, 223);"></div>
                                    </div>
                                    <div class="tColor" title="Sand">
                                        <div class="shirtColor" style="background-color: rgb(197, 186, 161);"></div>
                                    </div>
                                    <div class="tColor" title="Dark Brown">
                                        <div class="shirtColor" style="background-color: rgb(44, 28, 10);"></div>
                                    </div>
                                    <div class="tColor" title="Neon Orange">
                                        <div class="shirtColor" style="background-color: rgb(243, 120, 39);"></div>
                                    </div>
                                    <div class="tColor" title="Orange">
                                        <div class="shirtColor" style="background-color: rgb(236, 89, 47);"></div>
                                    </div>
                                    <div class="tColor" title="Dark Yellow">
                                        <div class="shirtColor" style="background-color: rgb(255, 158, 44);"></div>
                                    </div>

                                </div>
                            </details>
                        </div>

                    </div>
                    <div class="tab-content">
                        <div class="tab-pane active fade show" id="tab2">
                            <div class="well">
                                <div id="tshirttype">
                                    <div class="input-write">
                                       
                                        <T_controls />       <!-------- Text Controls(add text button and other text controls functions)-->

                                        <hr />

                                        <Dra_g />           <!-- graphics="Dra_g component" (upload images and drag and drop system)-->

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-lg-5 col-12 d-flex justify-content-center fabric">
                <!--2nd box-->
                <!-- shirt column -->
                <div id="canvas_cont" dragover="allowDrop(event)" drop="dropElement(event)">
                    <canvas ref="canvasRef" height="500" width="500" />

                </div>
            </div>
            <thirdColumn />
        </div>
    </div>
</div>
</template>

    
         <!--------------------------------------------------------------script------------------------------------------------------------------->

<script>
import thirdColumn from './components/thirdColumn.vue';
import Dra_g from './components/Dra_g.vue';
import T_controls from './components/T_controls.vue';
import {
    fabric
} from "fabric";

var canvas = null;
export default {
    name: "app",
    components: {
        thirdColumn,
        Dra_g,
        T_controls
    },
    mounted() {
        canvas = new fabric.Canvas(this.$refs.canvasRef, {
            isDrawingMode: false,
            preserveObjectStacking: true,
        });
        new fabric.Image.fromURL(this.image, (_img) => {
            const _me = _img.set({
                left: 0,
                top: 0,
                width: _img.width,
                height: _img.height,
                lockMovementX: true,
                lockMovementY: true,

            });
            canvas.add(_me);
        });
        /*  var canvas;
          window.onload = function () {
              canvas = new fabric.Canvas(document.getElementById("canvas"));
          }  */

    },
    data() {
        return {
            image: "https://5.imimg.com/data5/PO/FN/MY-52170301/men-plain-t-shirt-500x500.jpg",
            active: false,
            
        };
    },
    methods: {
       
        /* Follow Camel Casing
          Using Accepted/ Valid Variable / Class Namespaces
          Class: start with capital e.g.ClassName
          Variable: small e.g.varName
          CommentShortcut: alt + shift + a
          Find: ctrl + f
          indent: alt + shift + f */
    }
}
</script>
          
          <!------------------------------------------------------------- style-------------------------------------------------------------------->

<style src="./css/style.css"></style>
