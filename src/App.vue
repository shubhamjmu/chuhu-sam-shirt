<template>
    <div class="container-fluid">
        <div class="px-lg-2 px-sm-2  pb-5">
            <div class="header pt-5 pb-4">
                <p class="font1 text-center">Customize shirt</p> <!-- heading-->
            </div>
            <div class="row">
                <div class="col-lg-4 col-12 bg-pink ">
                    <!-- 1st box -->
                    <!----first editing box---->
                    <div class="tabbable">
                        <nav class="nav nav-pills d-flex justify-content-center pt-4" role="tablist" id="nav-tab">
                            <!-- nav tabs-->
                            <button class="active nav-link " data-bs-toggle="tab" data-bs-target="#tab1" type="button" role="tab" aria-selected="false">
                                Add Text and Color
                            </button>
                            <button class=" nav-link " data-bs-toggle="tab" data-bs-target="#tab2" type="button" role="tab" aria-selected="true" tabindex="-1">
                                Graphics
                            </button>
                        </nav>
                        <div class="tab-content d-flex justify-content-center">
                            <div class="tab-pane " id="tab1">
                                <div class="well">
                                    <select id="tshirttype ">
                                        <option value="./" selected="selected" v-on:click="shirt()">Men's Long Sleeves shirt</option>
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
                        <div class="tab-content ">
                            <div class="tab-pane active fade show " id="tab2">
                                <div class="well">
                                    <div id="tshirttype">
                                        <div class="input-write">
                                            <div class="d-flex justify-content-center">
                                                <button id="add-text" class="btn btn-warning px-2 " title="Add text" v-on:click="Addtext()"> Add Text Here...
                                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-90deg-right" viewBox="0 0 16 16">
                                                        <path fill-rule="evenodd" d="M14.854 4.854a.5.5 0 0 0 0-.708l-4-4a.5.5 0 0 0-.708.708L13.293 4H3.5A2.5 2.5 0 0 0 1 6.5v8a.5.5 0 0 0 1 0v-8A1.5 1.5 0 0 1 3.5 5h9.793l-3.147 3.146a.5.5 0 0 0 .708.708l4-4z" />
                                                    </svg>
                                                </button>
                                            </div>
                                            <div id="text-controls">
                                                <div id="text-wrapper" style="margin-top: 10px" v-show="getText">
                                                    <div id="text-controls">
                                                        Text-color:<input type="color" value="" id="color" size="10"><br>
                                                        <label for="font-family" style="display:inline-block">Font family:</label>
                                                        <select select name="sortBy" id="font-family" @change="FontChange(Font)" v-model="Font">
                                                            <option v-for="item in FontFamily" :key=item.value :value="item.value">{{ item.text }}</option>
                                                        </select>
                                                        <br>
                                                        <label for="text-align" style="display:inline-block">Text align:</label>
                                                        <select name="sortBy" id="sortBy" @change=" handleClick(Alignment)" v-model="Alignment">
                                                            <option v-for="item in AlignmentOptions" :value="item.value" :key="item.value">{{item.text}}</option>
    
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
                                                            <input type="range" value="1" min="1" max="5" id="text-stroke-width">
                                                        </div>
                                                        <div>
                                                            <label for="text-font-size">Font size:</label>
                                                            <input type="range" value="" min="1" max="120" step="1" id="text-font-size">
                                                        </div>
                                                        <div>
                                                            <label for="text-line-height">Line height:</label>
                                                            <input type="range" value="" min="0" max="10" step="0.1" id="text-line-height">
                                                        </div>
    
                                                        <div id="text-controls-additional">
                                                            <input type='checkbox' name='fonttype' id="text-cmd-bold">
                                                            Bold
    
                                                            <input type='checkbox' name='fonttype' id="text-cmd-italic">
                                                            Italic
    
                                                            <input type='checkbox' name='fonttype' id="text-cmd-underline">
                                                            Underline
    
                                                            <input type='checkbox' name='fonttype' id="text-cmd-linethrough">
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
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/v.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/rm.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/bts.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/vecteezy_icon-bts-character-a-cute-face-cartoon-suitable-for_11363122.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363157.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363158.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/vecteezy_icon-koya-character-a-cute-face-cartoon-suitable-for_11363199.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/vecteezy_icon-rj-character-a-cute-face-cartoon-suitable-for_11363161.jpg">
                                                    <img draggable="true" style="cursor:pointer;" class="img-fluid" src="./assets/vecteezy_icon-set-bt21-character-a-cute-face-cartoon-suitable-for_11363192.jpg">
                                                </div>
                                            </div>
                                            <div>
                                                <hr>
                                                <form enctype="multipart/form-data" class="d-flex justify-content-center btnn">
                                                    <input type="file" name="fileToUpload" id="fileToUpload">
                                                    <button class="btn btn-warning  " type="submit" value="upload image" name="submit">Upload </button>
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
                            <button type="submit" class="btn btn-large btn-block btn-primary " name="addToTheBag" id="addToTheBag">Add To Bag
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
                    height: _img.height,
                    lockMovementX: true,
                    lockMovementY: true,
                })
                canvas.add(_me)
            });
        },
        data() {
            return {
                image: 'https://5.imimg.com/data5/PO/FN/MY-52170301/men-plain-t-shirt-500x500.jpg',
                active: false,
                getText: true,
                Alignment: 'left',
                AlignmentOptions: [{
                        text: 'Left',
                        value: 'left'
                    },
                    {
                        text: 'Right',
                        value: 'right'
                    },
                    {
                        text: 'Center',
                        value: 'center'
                    }
                ],
                fillColor: 'brown',
                Font: 'delicious',
                FontFamily: [{
                        text: 'Delicious',
                        value: 'delicious'
                    },
                    {
                        text: 'Helvetica',
                        value: 'helvetica'
                    },
                    {
                        text: 'Corsiva',
                        value: 'corsiva'
                    },
                    {
                        text: 'Verdana',
                        value: 'verdana'
                    },
                    {
                        text: 'Georgia',
                        value: 'georgia'
                    },
                    {
                        text: 'Monaco',
                        value: 'monaco'
                    },
                    {
                        text: 'Optima',
                        value: 'optima'
                    },
                    {
                        text: 'Hoefler Text',
                        value: 'hoefler text'
                    },
                    {
                        text: 'Plaster',
                        value: 'plaster'
                    },
                    {
                        text: 'Engagement',
                        value: 'engagement'
                    },
                    {
                        text: 'Impact',
                        value: 'impact'
                    },
                ]
            }
        },
        methods: {
            Addtext() {
                var text = new fabric.IText('Tap and Type', {
                    left: 0,
                    top: 0,
                    fontFamily: this.Font,
                    fill: this.fillColor,
                    fontSize: 20,
                    align: this.Alignment,
                   
                })
                canvas.add(text);
                canvas.renderAll()
            },
            FontChange(value ) {
                this.Font = value;
                console.log(value);
            },
            handleClick(value) {
                this.Alignment = value;
                console.log(value);
            },
        },
    }
    </script>
          
          <!------------------------------------------------------------- style-------------------------------------------------------------------->
   
    
      
      <!------------------------------------------------------------- style-------------------------------------------------------------------->

<style src="./style/style.css"></style>