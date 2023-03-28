<template>
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
</template>

<!-----------------------------------------script here---------------------------------->

<script>
import {
    fabric
} from "fabric";
var canvas = null;
export default {
    name: "T_controls",
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
    },
    data() {
        return {
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
        }
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
    }
}
</script>
