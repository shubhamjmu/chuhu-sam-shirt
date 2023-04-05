<template>
<div class="container-fluid">
    <div class="px-lg-2 px-sm-2 pb-5">
        <div class="header pt-5 pb-4">
            <p class="font1 text-center">Customize shirt</p>
            <!-- heading-->
        </div>
        <div class="row">
            <div class="col-lg-4 col-12 pb-sm-3 bg-pink">
                <!-- 1st box -->
                <!----first editing box---->
                <div class="tabbable">
                    <nav class="nav nav-pills d-flex justify-content-center pt-4" role="tablist" id="nav-tab">
                        <!-- nav tabs-->
                        <button class=" nav-link" data-bs-toggle="tab" data-bs-target="#tab1" type="button" role="tab" aria-selected="false">
                            Color
                        </button>
                        <button class=" active nav-link" data-bs-toggle="tab" data-bs-target="#tab2" type="button" role="tab" aria-selected="true" tabindex="-1">
                            Image
                        </button>
                    </nav>

                    <!-- tables-->
                    <div class="tab-content " style="background-color:#f5f5f5;">

                        <div class="tab-pane fade  " id="tab1">

                            <details data-key="color-id">
                                <!-- colors -->
                                <summary class="p-3">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="18" fill="currentColor" class="bi bi-palette" viewBox="0 0 16 16">
                                        <path d="M8 5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zm4 3a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zM5.5 7a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm.5 6a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" />
                                        <path d="M16 8c0 3.15-1.866 2.585-3.567 2.07C11.42 9.763 10.465 9.473 10 10c-.603.683-.475 1.819-.351 2.92C9.826 14.495 9.996 16 8 16a8 8 0 1 1 8-8zm-8 7c.611 0 .654-.171.655-.176.078-.146.124-.464.07-1.119-.014-.168-.037-.37-.061-.591-.052-.464-.112-1.005-.118-1.462-.01-.707.083-1.61.704-2.314.369-.417.845-.578 1.272-.618.404-.038.812.026 1.16.104.343.077.702.186 1.025.284l.028.008c.346.105.658.199.953.266.653.148.904.083.991.024C14.717 9.38 15 9.161 15 8a7 7 0 1 0-7 7z" />
                                    </svg>
                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Colors</span>
                                </summary>
                                <label for="head" class="px-5 pb-3">Color Input:
                                    <input type="color" class="color-input" value="#ff0000" />
                                </label>
                            </details>
                        </div>

                    </div>
                    <div class="tab-content">
                        <div class="tab-pane active fade show" id="tab2">
                            <div class="well">
                                <div id="tshirttype">
                                    <div class="input-write">
                                        <!-- graphics="Dra_g component" (upload images and drag and drop system)-->
                                        <div id="tshirttype">
                                            <details data-key="graphics">
                                                <summary class="pb-3">
                                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-easel" viewBox="0 0 16 16">
                                                        <path d="M8 0a.5.5 0 0 1 .473.337L9.046 2H14a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1h-1.85l1.323 3.837a.5.5 0 1 1-.946.326L11.092 11H8.5v3a.5.5 0 0 1-1 0v-3H4.908l-1.435 4.163a.5.5 0 1 1-.946-.326L3.85 11H2a1 1 0 0 1-1-1V3a1 1 0 0 1 1-1h4.954L7.527.337A.5.5 0 0 1 8 0zM2 3v7h12V3H2z" />
                                                    </svg>
                                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Graphics</span>
                                                </summary>
                                                <!-- make card and boards to grag and drop-->
                                                <div class="row">
                                                    <div class="col-4">
                                                        <B_oard id="board-1">
                                                            <C_ard id="card-1" draggable="true" style="width: 8rem;justify-content:center;align-items:center">
                                                                <img draggable="true" style="cursor: pointer" class="img-fluid" src="./assets/v.jpg" />
                                                            </C_ard>
                                                        </B_oard>
                                                    </div>
                                                    <div class="col-4">
                                                        <B_oard id="board-2">
                                                            <C_ard id="card-2" draggable="true" style="width: 8rem;justify-content:center;align-items:center">
                                                                <img draggable="true" style="cursor: pointer" class="img-fluid" src="./assets/rm.jpg" />
                                                            </C_ard>
                                                        </B_oard>
                                                    </div>
                                                    <div class="col-4">
                                                        <B_oard id="board-1">
                                                            <C_ard id="card-1" draggable="true" style="width: 8rem;justify-content:center;align-items:center">
                                                                <img draggable="true" style="cursor: pointer" class="img-fluid" src="./assets/bts.jpg" />
                                                            </C_ard>
                                                        </B_oard>
                                                    </div>
                                                </div>
                                                <div class="row">
                                                    <div class="col-4">
                                                        <B_oard id="board-1">
                                                            <C_ard id="card-1" draggable="true" style="width: 8rem;justify-content:center;align-items:center">
                                                                <img draggable="true" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-bts-character-a-cute-face-cartoon-suitable-for_11363122.jpg" />
                                                            </C_ard>
                                                        </B_oard>
                                                    </div>
                                                    <div class="col-4">
                                                        <B_oard id="board-1">
                                                            <C_ard id="card-1" draggable="true" style="width: 8rem;justify-content:center;align-items:center">
                                                                <img draggable="true" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363157.jpg" />
                                                            </C_ard>
                                                        </B_oard>
                                                    </div>
                                                    <div class="col-4">
                                                        <B_oard id="board-1">
                                                            <C_ard id="card-1" draggable="true" style="width: 8rem;justify-content:center;align-items:center">
                                                                <img draggable="true" style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-set-bt21-character-a-cute-face-cartoon-suitable-for_11363192.jpg" />
                                                            </C_ard>
                                                        </B_oard>
                                                    </div>
                                                </div>
                                                <img draggable="true" style="cursor: pointer" class="img-fluid" :src="imageFile" />
                                                <div class="np-upload-in-progress" v-if="isImageUploading">
                                                    Please wait while your file is being uploaded ...
                                                </div>
                                            </details>
                                            <!-- upload and submit button-->
                                        </div>
                                        <hr />
                                        <div>
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

                                        <!-- file upload -->
                                        <!-- <input style="display: none;" type="file" @change="OnFileSelected" ref="fileInput">
                                        <button @click="$refs.fileInput.click()">Pick File</button>
                                        <button @click="onUpload">Upload</button> -->

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-lg-5 col-12 d-flex pt-sm-3 pb-sm-3 justify-content-center" :style="{ backgroundColor: BackgroundColor }">
                <!--2nd box-->
                <!-- shirt column -->
                <div class="product">
                    <img src="./assets/casual-white-blouse-women-rsquo-s-fashion.png" alt="without background" class="img-1">
                    <img src="./assets/blouse-women-rsquo-s-fashion.png" alt="with background" class="img-2">
                    <div class="color"></div>

                </div>
            </div>
            <thirdColumn />
          
        </div>
    </div>
</div>
</template>

    
         <!--------------------------------------------------------------script------------------------------------------------------------------->

<script>
import thirdColumn from './components/thirdColumn';
//import axios from 'axios'
import B_oard from './components/B_oard';
import C_ard from './components/C_ard';

export default {
    name: "app",
    components: {
        thirdColumn,
        C_ard,
        B_oard
    },

    mounted() {
        //Get elements from the DOM
        const color = document.querySelector('.color');
        const colorInput = document.querySelector('.color-input');
        //Add input event listener
        colorInput.addEventListener('input', () => {
            /*Set background of the color div to
            the color set in the input field*/
            color.style.backgroundColor = colorInput.value;
        });

    },
    data() {
        return {
            BackgroundColor: '#ffffff',
            active: false,
            getText: true,
            imageFile: null,
            input: null,
            isImageUploading: false,
            // SelectedFile: null,
        };
    },
    methods: {
        
        /* onUpload() {
            const fd = new FormData();
            fd.append('image', this.SelectedFile, this.SelectedFile.name)
            axios.post("database ka url", fd, {
                    onUploadProgress: uploadEvent => {
                        console.log('Upload progress:' + Math.round(uploadEvent.loaded / uploadEvent.total * 100) + '%')
                    }
                })

                .then(res => {
                    console.log(res)
                })
        },
        OnFileSelected(event) {
            this.SelectedFile = event.files.target[0];
        }, */
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
            console.log(this.input.files[0]);

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
