<template>
    <div class="container-fluid d-flex  ">
        <div class="px-lg-2 px-sm-2  pb-5">
            <div class="header pt-5 pb-4">
                <p class="font1 text-center">Customize shirt</p> <!-- heading-->
            </div>
            <div class="row">
                <div class="col-lg-4 col-12 bg-pink d-flex justify-content-start  ">
                    <!-- 1st box -->
                    <!----first editing box---->
                    <div class="tabbable">
                        <ul class="nav nav-tabs d-flex justify-content-center">
                            <!-- nav tabs-->
                            <li class="active  pe-4">
                                <a href="#tab1" data-toggle="tab" data-original-title style="text-decoration-color: black;">
                                    <h4>Add Text and Color</h4>
                                </a>
                            </li>
                            <li>
                                <a href="#tab2" data-toggle="tab" data-original-title style="text-decoration-color: black;">
                                    <h4>Graphics</h4>
                                </a>
                            </li>
                        </ul>
                        <div class="tab-content">
                            <div class="tab-pane    " id="tab1">
                                <div class="well">
                                    <select id="tshirttype ">
                                        <option value="./" selected="selected" v-on:click="shirt()">Men's Long Sleeves shirt
                                        </option>
                                        <option value="./" selected="selected">Men's Short Sleeves shirt</option>
                                        <option value="./" selected="selected">Women's Long Sleevs shirt</option>
                                        <option value="./" selected="selected">Women's short Sleevs shirt</option>

                                    </select>
                                </div>
                                <div class="well">
                                    <ul class="nav color-style">
                                        <li class="color-preview" title="black" style="background-color:#000;"></li>
                                        <li class="color-preview" title="grey" style="background-color:#adb5bd;"></li>
                                        <li class="color-preview" title="white" style="background-color:#ffffff;"></li>
                                        <li class="color-preview" title="cyan" style="background-color:#0dcaf0;"></li>
                                        <li class="color-preview" title="teal" style="background-color:#20c997;"></li>
                                        <li class="color-preview" title="green" style="background-color:#198754;"></li>
                                        <li class="color-preview" title="blue" style="background-color:#0d6efd;"></li>
                                        <li class="color-preview" title="yellow" style="background-color:#ffc107;"></li>
                                        <li class="color-preview" title="orange" style="background-color:#fd7e14;"></li>
                                        <li class="color-preview" title="red" style="background-color:#dc3545;"></li>
                                        <li class="color-preview" title="pink" style="background-color:#d63384;"></li>
                                        <li class="color-preview" title="purple" style="background-color:#6f42c1;"></li>
                                        <li class="color-preview" title="indigo" style="background-color:#6610f2;"></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                        <div class="tab-content">
                            <div class="tab-pane active" id="tab2">
                                <div class="well">
                                    <div id="tshirttype">
                                        <div class="input-write">
                                            <div class="d-flex justify-content-center">
                                                <button id="add-text" class="btn btn-warning px-2 " title="Add text"
                                                    v-on:click="Addtext()"> Add Text Here...
                                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                                                        fill="currentColor" class="bi bi-arrow-90deg-right"
                                                        viewBox="0 0 16 16">
                                                        <path fill-rule="evenodd"
                                                            d="M14.854 4.854a.5.5 0 0 0 0-.708l-4-4a.5.5 0 0 0-.708.708L13.293 4H3.5A2.5 2.5 0 0 0 1 6.5v8a.5.5 0 0 0 1 0v-8A1.5 1.5 0 0 1 3.5 5h9.793l-3.147 3.146a.5.5 0 0 0 .708.708l4-4z" />
                                                    </svg>
                                                </button>
                                            </div>
                                            <div id="text-controls">
                                                <div id="text-wrapper" style="margin-top: 10px" v-show="getText">
                                                    <div id="text-controls">
                                                        Text-color<input type="color" value="" id="color" size="10"><br>
                                                        <label for="font-family" style="display:inline-block">Font
                                                            family:</label>
                                                        <select select name="sortBy" id="sortBy"
                                                            @change="FontChange(Font)" v-model="Font">
                                                            <option v-for="item in FontFamily" :key=item.id
                                                                :value="item.value">{{ item.text }}</option>
                                                        </select>
                                                        <br>
                                                        <label for="text-align" style="display:inline-block">Text
                                                            align:</label>
                                                        <select id="text-align" v-model="value" v-on:change="onChange">
                                                            <option value="left">Left</option>
                                                            <option value="center">Center</option>
                                                            <option value="right">Right</option>
                                                            <option value="justify">Justify</option>
                                                        </select>
                                                        <div>
                                                            <label for="text-bg-color">Background color:</label>
                                                            <input type="color" value="" id="text-bg-color" size="10">
                                                        </div>
                                                        <div>
                                                            <label for="text-lines-bg-color">Background text color:</label>
                                                            <input type="color" value="" id="text-lines-bg-color" size="10">
                                                        </div>
                                                        <div>
                                                            <label for="text-stroke-color">Stroke color:</label>
                                                            <input type="color" value="" id="text-stroke-color">
                                                        </div>
                                                        <div>
                                                            <label for="text-stroke-width">Stroke width:</label>
                                                            <input type="range" value="1" min="1" max="5"
                                                                id="text-stroke-width">
                                                        </div>
                                                        <div>
                                                            <label for="text-font-size">Font size:</label>
                                                            <input type="range" value="" min="1" max="120" step="1"
                                                                id="text-font-size">
                                                        </div>
                                                        <div>
                                                            <label for="text-line-height">Line height:</label>
                                                            <input type="range" value="" min="0" max="10" step="0.1"
                                                                id="text-line-height">
                                                        </div>

                                                        <div id="text-controls-additional">
                                                            <input type='checkbox' name='fonttype' id="text-cmd-bold">
                                                            Bold

                                                            <input type='checkbox' name='fonttype' id="text-cmd-italic">
                                                            Italic

                                                            <input type='checkbox' name='fonttype' id="text-cmd-underline">
                                                            Underline

                                                            <input type='checkbox' name='fonttype'
                                                                id="text-cmd-linethrough">
                                                            Linethrough

                                                            <input type='checkbox' name='fonttype' id="text-cmd-overline">
                                                            Overline

                                                        </div>

                                                    </div>
                                                </div>
                                            </div>
                                            <hr>
                                            <div id="tshirttype">
                                                <div class="px-3 px-sm-3">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/v.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/rm.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/bts.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/vecteezy_icon-bts-character-a-cute-face-cartoon-suitable-for_11363122.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363157.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363158.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/vecteezy_icon-koya-character-a-cute-face-cartoon-suitable-for_11363199.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/vecteezy_icon-rj-character-a-cute-face-cartoon-suitable-for_11363161.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid"
                                                        src="./assets/vecteezy_icon-set-bt21-character-a-cute-face-cartoon-suitable-for_11363192.jpg">
                                                </div>
                                            </div>
                                            <div>
                                                <hr>
                                                <form enctype="multipart/form-data"
                                                    class="d-flex justify-content-center btnn">
                                                    <input type="file" name="fileToUpload" id="fileToUpload">
                                                    <button class="btn btn-warning  " type="submit" value="upload image"
                                                        name="submit">Upload </button>
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

                    <canvas ref="canvasRef" height="500" width="500" />

                </div>
                <div class="col-lg-3 col-12  justify-content-end ">
                    <!--3rd box-->
                    <div class="well">
                        <h3 class="text-center">Preferable Sizes</h3> <!-- heading-->
                        <table class="table">
                            <tbody>
                                <tr>
                                    <td>
                                        <input type="checkbox">&emsp;S
                                    </td>
                                    <td align="right">
                                        <input min="0" style="width:40px" value="1" type="number">
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <input type="checkbox">&emsp;M
                                    </td>
                                    <td align="right">
                                        <input min="0" style="width:40px" value="1" type="number">
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <input type="checkbox">&emsp;L
                                    </td>
                                    <td align="right">
                                        <input min="0" style="width:40px" value="1" type="number">
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <input type="checkbox">&emsp;XL
                                    </td>
                                    <td align="right">
                                        <input min="0" style="width:40px" value="1" type="number">
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <input type="checkbox">&emsp;XXL
                                    </td>
                                    <td align="right">
                                        <input min="0" style="width:40px" value="1" type="number">
                                    </td>
                                </tr>

                            </tbody>

                        </table>
                        <div class="d-flex justify-content-center">
                            <button type="submit" class="btn btn-large btn-block btn-primary " name="addToTheBag"
                                id="addToTheBag">Add To Bag
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                                    class="bi bi-cart4" viewBox="0 0 16 16">
                                    <path
                                        d="M0 2.5A.5.5 0 0 1 .5 2H2a.5.5 0 0 1 .485.379L2.89 4H14.5a.5.5 0 0 1 .485.621l-1.5 6A.5.5 0 0 1 13 11H4a.5.5 0 0 1-.485-.379L1.61 3H.5a.5.5 0 0 1-.5-.5zM3.14 5l.5 2H5V5H3.14zM6 5v2h2V5H6zm3 0v2h2V5H9zm3 0v2h1.36l.5-2H12zm1.11 3H12v2h.61l.5-2zM11 8H9v2h2V8zM8 8H6v2h2V8zM5 8H3.89l.5 2H5V8zm0 5a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0zm9-1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0z" />
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
} from 'fabric';
var canvas = null;

export default {
    name: 'app',
    mounted() {
        canvas = new fabric.Canvas(this.$refs.canvasRef, {
            isDrawingMode: false

        });
        new fabric.Image.fromURL(this.image, (_img) => {
            const _me = _img.set({
                left: 0,
                top: 0,
                width: _img.width,
                height: _img.height
            })
            canvas.add(_me)
        });

    },
    data() {
        return {
            image: 'https://5.imimg.com/data5/PO/FN/MY-52170301/men-plain-t-shirt-500x500.jpg',
            getText: true,
            value: '',
            fillColor: 'brown',
            Font: 'delicious',
            FontFamily: [
                { text: 'Delicious', value: 'delicious' },
                { text: 'Helvetica', value: 'helvetica' },
                { text: 'Corsiva', value: 'corsiva' }
            ]
        };
    },
    methods: {

        FontChange(value){
            this.Font = value;
            
        },
        Addtext() {
              
            let x =  new fabric.IText('Tap and Type', {
                left: 0,
                top: 0,
                fontFamily: this.Font,
                fill: this.fillColor,
                fontSize: 20,
                align: this.Alignment

            })

            canvas.add(x);
        },
        onChange() {
            console.log(this.value);

        }
    }

}
</script>
    
      
      <!------------------------------------------------------------- style-------------------------------------------------------------------->

<style scoped>
.fabric {
    align-items: center;
    justify-content: center;
    display: flex;
    height: 800px;
}

#my-image {
    display: none;
}

.clearfix:before,
.clearfix:after {
    display: table;
    line-height: 0;
    content: "";
}

.canvas {
    border: 1px solid #CCC;
    border-radius: 4px;
}

#v {
    width: 150px;
    height: 150px;
    padding: 0.5em;
}

.file-upload {
    display: none;
}

.font1 {
    font-family: 'OpenSans', sans-serif;
    font-size: 30px;
    color: rgb(7, 96, 73);
    font-weight: bold;
}

.bg-pink {
    background-color: rgb(221, 180, 180);
}

.well {
    min-height: 20px;
    padding: 19px;
    margin-bottom: 20px;
    background-color: #f5f5f5;
    border: 1px solid #e3e3e3;
    box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}

.nav {
    margin-left: 0;
    margin-bottom: 20px;
    list-style: none;
}

ul,
ol {
    padding: 0;
    margin: 0 0 10px 25px;
}

.color-style {
    margin-left: 0;
    margin-bottom: 20px;
    list-style: none;

}

.color-preview {
    border: 1px solid #CCC;
    margin: 2px;
    zoom: 1;
    vertical-align: top;
    display: inline-block;
    cursor: pointer;
    overflow: hidden;
    width: 20px;
    height: 20px;
}

nav-tabs:before,
.nav-tabs:after {
    display: table;
    content: "";
    line-height: 0;
}

.nav-tabs>.active>a,
.nav-tabs>.active>a:hover {
    color: #555555;

    border-bottom-color: transparent;
    cursor: default;
}

.nav-tabs {
    border-bottom: 1px solid #ddd;
}

.nav-tabs>li {
    margin-bottom: -1px;
    float: left;
}

.nav-tabs>li>a {
    padding-top: 8px;
    padding-bottom: 8px;
    line-height: 20px;
    border: 1px solid transparent;
    -webkit-border-radius: 4px 4px 0 0;
    -moz-border-radius: 4px 4px 0 0;
    border-radius: 4px 4px 0 0;
}

#draggable {
    width: 150px;
    height: 150px;
    padding: 0.5em;
}

.tab-content {
    overflow: auto;
}

.tab-content>.tab-pane {
    display: none;
}

.tab-content>.active {
    display: block;
}
</style>















