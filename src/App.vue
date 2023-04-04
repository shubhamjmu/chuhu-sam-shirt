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
                            Image
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
                                    <select id="tshirttype"  >
                                       
                                    </select>
                                </div>
                            </details>

                            <details data-key="color-id">
                                <!-- colors -->
                                <summary class="p-3">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="18" fill="currentColor" class="bi bi-palette" viewBox="0 0 16 16">
                                        <path d="M8 5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zm4 3a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zM5.5 7a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm.5 6a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" />
                                        <path d="M16 8c0 3.15-1.866 2.585-3.567 2.07C11.42 9.763 10.465 9.473 10 10c-.603.683-.475 1.819-.351 2.92C9.826 14.495 9.996 16 8 16a8 8 0 1 1 8-8zm-8 7c.611 0 .654-.171.655-.176.078-.146.124-.464.07-1.119-.014-.168-.037-.37-.061-.591-.052-.464-.112-1.005-.118-1.462-.01-.707.083-1.61.704-2.314.369-.417.845-.578 1.272-.618.404-.038.812.026 1.16.104.343.077.702.186 1.025.284l.028.008c.346.105.658.199.953.266.653.148.904.083.991.024C14.717 9.38 15 9.161 15 8a7 7 0 1 0-7 7z" />
                                    </svg>
                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Colors</span>
                                </summary>
                                <div class="well"   style="display: flex; flex-wrap:wrap;margin:1.5rem">
                                    <div class="tColor" title="White" >
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
                                        <!-- graphics="Dra_g component" (upload images and drag and drop system)-->
                                        <div id="tshirttype">
                                            <details data-key="graphics">
                                                <summary class="pb-3">
                                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-easel" viewBox="0 0 16 16">
                                                        <path d="M8 0a.5.5 0 0 1 .473.337L9.046 2H14a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1h-1.85l1.323 3.837a.5.5 0 1 1-.946.326L11.092 11H8.5v3a.5.5 0 0 1-1 0v-3H4.908l-1.435 4.163a.5.5 0 1 1-.946-.326L3.85 11H2a1 1 0 0 1-1-1V3a1 1 0 0 1 1-1h4.954L7.527.337A.5.5 0 0 1 8 0zM2 3v7h12V3H2z" />
                                                    </svg>
                                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Graphics</span>
                                                </summary>

                                                <div  class="px-5 px-sm-5 board" @dragover.prevent @drop.prevent="drop" style="display: flex; flex-wrap:wrap;">
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/v.jpg" />
                                                    <img draggable="true" style="cursor: pointer" class="img-fluid" src="./assets/rm.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/bts.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-bts-character-a-cute-face-cartoon-suitable-for_11363122.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363157.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363158.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-koya-character-a-cute-face-cartoon-suitable-for_11363199.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-rj-character-a-cute-face-cartoon-suitable-for_11363161.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" src="./assets/vecteezy_icon-set-bt21-character-a-cute-face-cartoon-suitable-for_11363192.jpg" />
                                                    <img draggable="true"  style="cursor: pointer" class="img-fluid" :src="imageFile" />
                                                    <div class="np-upload-in-progress" v-if="isImageUploading">
                                                        Please wait while your file is being uploaded ...
                                                    </div>
                                                </div>
                                            </details>
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
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-lg-5 col-12 d-flex justify-content-center">
                <!--2nd box-->
                <!-- shirt column -->
              
                  <img src="https://5.imimg.com/data5/IB/IA/FQ/SELLER-31533998/men-white-plain-full-sleeves-shirts-500x500.png" class="img-fluid">
                
               
            </div>
            
            <thirdColumn />
        </div>
    </div>
</div>
</template>

    
         <!--------------------------------------------------------------script------------------------------------------------------------------->

<script>
import thirdColumn from './components/thirdColumn';


export default {
    name: "app",
    components: {
        thirdColumn,

    },
    
    mounted() {
       
    },
    data() {
        return {
            dissapear: 'blue',
            active: false,
            getText: true,
            Font: "delicious",
            FontFamily: [{
                    text: "Delicious",
                    value: "delicious",
                    id: 1
                },
                {
                    text: "Corsiva",
                    value: "corsiva",
                    id: 2
                },
                {
                    text: "Monaco",
                    value: "monaco",
                    id: 3
                },
                {
                    text: "Impact",
                    value: "impact",
                    id: 4
                },
                {
                    text: "Times New Roman",
                    value: "Times New Roman",
                    id: 5
                },
                {
                    text: "Helvetica",
                    value: "Helvetica",
                    id: 6
                },
                {
                    text: "Lucida Console",
                    value: "Lucida Console",
                    id: 7
                },
                {
                    text: "Serif",
                    value: "Serif",
                    id: 8
                },
                {
                    text: "Cursive",
                    value: "Cursive",
                    id: 9
                },
                {
                    text: "Fantasy",
                    value: "Fantasy",
                    id: 10
                },
            ],
            fSize: 1,
            textColor: "#000000",
            backColor: "#000000",
            line: 1,
            style: "normal",
            FontStyle: [{
                    text: 'Normal',
                    value: 'normal',
                    id: 1
                },
                {
                    text: 'Italic',
                    value: 'italic',
                    id: 2
                },
                {
                    text: 'Oblique',
                    value: 'oblique',
                    id: 3
                },
            ],
            imageFile: null,
            input: null,
            isImageUploading: false,
            
        };
    },
    methods: {
        dissapearColor () {

   
    console.log( this.title)
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
