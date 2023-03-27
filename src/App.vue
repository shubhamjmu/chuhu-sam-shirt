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
                                <div class="well" style="display: flex; flex-wrap:wrap;">
                                    <label for="filter-color-all" class="pe-2">
                                        <input data-key="color" data-option="all" data-all="1" type="radio" id="filter-color-all" name="filter-color" value="all" style="width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-red" class="pe-2">
                                        <input data-key="color" data-option="red" type="radio" id="filter-color-red" name="filter-color" value="red" style="background:#FB5252; border:1px solid #FB5252; width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-orange" class="pe-2">
                                        <input data-key="color" data-option="orange" type="radio" id="filter-color-orange" name="filter-color" value="orange" style="background:#FCA120; border:1px solid #FCA120;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-pink" class="pe-2">
                                        <input data-key="color" data-option="pink" type="radio" id="filter-color-pink" name="filter-color" value="pink" style="background:#FFC0CB; border:1px solid #FFC0CB;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-yellow" class="pe-2">
                                        <input data-key="color" data-option="yellow" type="radio" id="filter-color-yellow" name="filter-color" value="yellow" style="background:#FCDB7E; border:1px solid #FCDB7E;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-green" class="pe-2">
                                        <input data-key="color" data-option="green" type="radio" id="filter-color-green" name="filter-color" value="green" style="background:#4AD295; border:1px solid #4AD295;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-cyan" class="pe-2">
                                        <input data-key="color" data-option="cyan" type="radio" id="filter-color-cyan" name="filter-color" value="cyan" style="background:#92CDFA; border:1px solid #92CDFA;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-blue" class="pe-2">
                                        <input data-key="color" data-option="blue" type="radio" id="filter-color-blue" name="filter-color" value="blue" style="background:#1273EB; border:1px solid #1273EB;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-purple" class="pe-2">
                                        <input data-key="color" data-option="purple" type="radio" id="filter-color-purple" name="filter-color" value="purple" style="background:#8080F1; border:1px solid #8080F1;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-black" class="pe-2">
                                        <input data-key="color" data-option="black" type="radio" id="filter-color-black" name="filter-color" value="black" style="background:#000000;; border:1px solid #000000;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-gray" class="pe-2">
                                        <input data-key="color" data-option="gray" type="radio" id="filter-color-gray" name="filter-color" value="gray" style="background:#BAC8D3; border:1px solid #BAC8D3;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                    <label for="filter-color-white" class="pe-2">
                                        <input data-key="color" data-option="white" type="radio" id="filter-color-white" name="filter-color" value="white" checked style="background:#ffffff; border:1px solid #ffffff;width: 20px;height: 20px; border-radius: 100%;" autocomplete="off" />
                                    </label>
                                </div>
                            </details>
                        </div>

                    </div>
                    <div class="tab-content">
                        <div class="tab-pane active fade show" id="tab2">
                            <div class="well">
                                <div id="tshirttype">
                                    <div class="input-write">
                                        <div class="d-flex justify-content-center">
                                            <!-- add text button -->
                                            <button id="add-text" class="btn btn-warning px-2" title="Add text" v-on:click="Addtext()">
                                                Add Text Here...
                                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-90deg-right" viewBox="0 0 16 16">
                                                    <path fill-rule="evenodd" d="M14.854 4.854a.5.5 0 0 0 0-.708l-4-4a.5.5 0 0 0-.708.708L13.293 4H3.5A2.5 2.5 0 0 0 1 6.5v8a.5.5 0 0 0 1 0v-8A1.5 1.5 0 0 1 3.5 5h9.793l-3.147 3.146a.5.5 0 0 0 .708.708l4-4z" />
                                                </svg>
                                            </button>
                                        </div>
                                        <div id="text-controls">
                                            <!-- text-controls -->
                                            <div id="text-wrapper" style="margin-top: 10px" v-show="getText">
                                                <details data-key="controls">
                                                    <summary class="pb-3">
                                                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-menu-button" viewBox="0 0 16 16">
                                                            <path d="M0 1.5A1.5 1.5 0 0 1 1.5 0h8A1.5 1.5 0 0 1 11 1.5v2A1.5 1.5 0 0 1 9.5 5h-8A1.5 1.5 0 0 1 0 3.5v-2zM1.5 1a.5.5 0 0 0-.5.5v2a.5.5 0 0 0 .5.5h8a.5.5 0 0 0 .5-.5v-2a.5.5 0 0 0-.5-.5h-8z" />
                                                            <path d="m7.823 2.823-.396-.396A.25.25 0 0 1 7.604 2h.792a.25.25 0 0 1 .177.427l-.396.396a.25.25 0 0 1-.354 0zM0 8a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V8zm1 3v2a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2H1zm14-1V8a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v2h14zM2 8.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm0 4a.5.5 0 0 1 .5-.5h6a.5.5 0 0 1 0 1h-6a.5.5 0 0 1-.5-.5z" />
                                                        </svg>
                                                        <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Text Controls</span>
                                                    </summary>
                                                    <div class="text-controls px-5 px-sm-5">
                                                        <div class="pb-1">
                                                            <label for="text-bg-color">Text color:</label>
                                                            <input type="color" id="color" size="10" v-on:input="colorChange()" v-model="textColor" />
                                                        </div>
                                                        <div class="pt-1 pb-1">
                                                            <label for="font-family" style="display: inline-block">Font family:</label>
                                                            <select select name="sortBy" id="font-family" @change="FontChange()" v-model="Font">
                                                                <option v-for="item in FontFamily" :key="item.value" :value="item.value">
                                                                    {{ item.text }}
                                                                </option>
                                                            </select>
                                                        </div>
                                                        <div class="pt-1 pb-1">
                                                            <label for="text-bg-color">Background color:</label>
                                                            <input type="color" id="text-color" size="10" v-on:input="bgChange()" v-model="backColor" />
                                                        </div>
                                                        <div class="pt-1 pb-1">
                                                            <label for="text-font-size">Font size:</label>
                                                            <input type="range" min="1" max="120" step="1" id="text-font-size" v-on:input="fsizeChange()" v-model="fSize" />
                                                        </div>
                                                        <div class="pt-1 pb-1">
                                                            <label for="text-line-height">Line height:</label>
                                                            <input type="range" min="0" max="10" step="0.1" id="text-line-height" v-on:input="lineChange()" v-model="line" />
                                                        </div>

                                                        <div id="text-controls-additional" class="pt-1 pb-1">
                                                            <label for="font-family" style="display: inline-block">Font Style:</label>
                                                            <select select name="sortBy" id="font-style" @change="styleChange()" v-model="style">
                                                                <option v-for="item in FontStyle" :key="item.value" :value="item.value">
                                                                    {{ item.text }}
                                                                </option>
                                                            </select>
                                                        </div>
                                                    </div>
                                                </details>
                                            </div>
                                        </div>
                                        <hr />
                                        <div id="tshirttype">
                                            <details data-key="graphics">
                                                <summary class="pb-3">
                                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-easel" viewBox="0 0 16 16">
                                                        <path d="M8 0a.5.5 0 0 1 .473.337L9.046 2H14a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1h-1.85l1.323 3.837a.5.5 0 1 1-.946.326L11.092 11H8.5v3a.5.5 0 0 1-1 0v-3H4.908l-1.435 4.163a.5.5 0 1 1-.946-.326L3.85 11H2a1 1 0 0 1-1-1V3a1 1 0 0 1 1-1h4.954L7.527.337A.5.5 0 0 1 8 0zM2 3v7h12V3H2z" />
                                                    </svg>
                                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Graphics</span>
                                                </summary>

                                                <div class="px-5 px-sm-5" style="display: flex; flex-wrap:wrap;">
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/v.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/rm.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/bts.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-bts-character-a-cute-face-cartoon-suitable-for_11363122.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363157.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363158.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-koya-character-a-cute-face-cartoon-suitable-for_11363199.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-rj-character-a-cute-face-cartoon-suitable-for_11363161.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-set-bt21-character-a-cute-face-cartoon-suitable-for_11363192.jpg" />
                                                    <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" :src="imageFile" />
                                                    <div class="np-upload-in-progress" v-if="isImageUploading">
                                                        Please wait while your file is being uploaded ...
                                                    </div>
                                                </div>
                                            </details>
                                        </div>
                                        <div>
                                            <hr />
                                            <form enctype="multipart/form-data" class="d-flex justify-content-center btnn">
                                                <div v-if="imageFile == null || imageFile.length == 0">
                                                    <input type="file" name="fileToUpload" id="fileToUpload" @change="showImagePreview($event)" accept="image/*" />
                                                </div>
                                                <div v-if="imageFile != null && imageFile.length != 0 && !isImageUploading">
                                                    <button class="btn btn-warning pe-2" type="submit" value="upload image" name="submit" v-on:click="uploadImage()">
                                                        Upload
                                                    </button>
                                                    <button class="btn btn-warning ps-2" v-on:click="clearImage()">
                                                        Cancel
                                                    </button>
                                                </div>
                                            </form>
                                        </div>
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
            <div class="col-lg-3 col-12 justify-content-end">
                <!--3rd box-->
                <div class="well">
                    <h3 class="text-center">Preferable Sizes</h3>
                    <!-- heading-->
                    <table class="table">
                        <tbody>
                            <tr>
                                <td><input type="checkbox" />&emsp;S</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;M</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;L</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;XL</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;XXL</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                        </tbody>
                    </table>
                    <div class="d-flex justify-content-center">
                        <button type="submit" class="btn btn-large btn-block btn-primary" name="addToTheBag" id="addToTheBag">
                            Add To Bag
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cart4" viewBox="0 0 16 16">
                                <path d="M0 2.5A.5.5 0 0 1 .5 2H2a.5.5 0 0 1 .485.379L2.89 4H14.5a.5.5 0 0 1 .485.621l-1.5 6A.5.5 0 0 1 13 11H4a.5.5 0 0 1-.485-.379L1.61 3H.5a.5.5 0 0 1-.5-.5zM3.14 5l.5 2H5V5H3.14zM6 5v2h2V5H6zm3 0v2h2V5H9zm3 0v2h1.36l.5-2H12zm1.11 3H12v2h.61l.5-2zM11 8H9v2h2V8zM8 8H6v2h2V8zM5 8H3.89l.5 2H5V8zm0 5a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0zm9-1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0z" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

    
         <!--------------------------------------------------------------script------------------------------------------------------------------->

<script>
import {
    fabric
} from "fabric";
var canvas = null;
export default {
    name: "app",
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
            getText: true,
            Alignment: "left",
            AlignmentOptions: [{
                    text: "Left",
                    value: "left",
                },
                {
                    text: "Right",
                    value: "right",
                },
                {
                    text: "Center",
                    value: "center",
                },
            ],
            Font: "delicious",
            FontFamily: [{
                    text: "Delicious",
                    value: "delicious",
                },
                {
                    text: "Corsiva",
                    value: "corsiva",
                },
                {
                    text: "Monaco",
                    value: "monaco",
                },
                {
                    text: "Impact",
                    value: "impact",
                },
                {
                    text: "Times New Roman",
                    value: "Times New Roman",
                },
                {
                    text: "Helvetica",
                    value: "Helvetica",
                },
                {
                    text: "Lucida Console",
                    value: "Lucida Console",
                },
                {
                    text: "Serif",
                    value: "Serif",
                },
                {
                    text: "Cursive",
                    value: "Cursive",
                },
                {
                    text: "Fantasy",
                    value: "Fantasy",
                },
            ],
            fSize: 1,
            textColor: "#000000",
            backColor: "#000000",
            line: 1,
            style: "normal",
            FontStyle: [{
                    text: 'Normal',
                    value: 'normal'
                },
                {
                    text: 'Italic',
                    value: 'italic'
                },
                {
                    text: 'Oblique',
                    value: 'oblique'
                },
            ],
            imageFile: null,
            input: null,
            isImageUploading: false,
        };
    },
    methods: {
        Addtext() {
            // for adding text on button click
            var textbox = new fabric.Textbox("Tap and Type here", {
                left: 70,
                top: 50,
                width: 150,
                textAlign: 'center'
            });
            canvas.add(textbox).setActiveObject(textbox);
        },
        colorChange() {
            canvas.getActiveObject().set("fill", this.textColor);
            console.log(canvas.getActiveObject());
            canvas.renderAll();
        },
        FontChange() {
            // for font-family
            canvas.getActiveObject().set("fontFamily", this.Font);
            console.log(canvas.getActiveObject());
            canvas.requestRenderAll();
        },
        bgChange() {
            //background  color
            canvas.getActiveObject().set("backgroundColor", this.backColor);
            console.log(canvas.getActiveObject());
            canvas.renderAll();
        },
        fsizeChange() {
            // for font size
            canvas.getActiveObject().set("fontSize", this.fSize);
            console.log(canvas.getActiveObject());
            canvas.renderAll();
        },
        lineChange() {
            //for line height
            canvas.getActiveObject().set("lineHeight", this.line);
            console.log(canvas.getActiveObject());
            canvas.renderAll();
        },
        styleChange() { // adding style to the font
            canvas.getActiveObject().set("fontStyle", this.style);
            console.log(canvas.getActiveObject());
            canvas.renderAll();
        },
        showImagePreview(event) { // choose image file
            this.input = event.target;
            if (this.input.files && this.input.files[0]) {
                let reader = new FileReader();
                reader.onload = (e) => {
                    this.imageFile = e.target.result;
                };
                reader.readAsDataURL(this.input.files[0]);
            }
        },
        uploadImage() { // upload image file                //baki rhta h iska kaam
            this.isImageUploading = true;
            setTimeout(() => {
                console.log(this.imageFile);
                this.isImageUploading = false;
                this.clearImage();
                alert("Image uploaded sucessfully!");
            }, 1000);
        },
        clearImage() { // clear the file
            this.imageFile = null;
            this.input = null;
        },
        /*      allowDrop(e) { // for allowing an image to drop
                  e.preventDefault();
              },
              dragElement(e) {
                  e.dataTransfer.setData("id", e.target.id); //transfer the "data" i.e. id of the target dragged.
              },
              //dropElement function called on ondrop event.
              dropElement(e) {
                 e.preventDefault();
                  var data = e.dataTransfer.getData("id"); //receiving the "data" i.e. id of the target dropped.
                  var imag = document.getElementById(data); //getting the target image info through its id. 
                  var img = new fabric.Image(imag, { //initializing the fabric image.
                      left: e.layerX - 80, //positioning the target on exact position of mouse event drop through event.layerX,Y.
                      top: e.layerY - 40,
                  });
                  img.scaleToWidth(imag.width); 
                  img.scaleToHeight(imag.height);
                  canvas.add(img);
              
              }
          },   */
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
