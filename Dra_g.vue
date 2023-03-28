<template>
    <div id="tshirttype">
        <details data-key="graphics">
            <summary class="pb-3">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-easel" viewBox="0 0 16 16">
                    <path d="M8 0a.5.5 0 0 1 .473.337L9.046 2H14a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1h-1.85l1.323 3.837a.5.5 0 1 1-.946.326L11.092 11H8.5v3a.5.5 0 0 1-1 0v-3H4.908l-1.435 4.163a.5.5 0 1 1-.946-.326L3.85 11H2a1 1 0 0 1-1-1V3a1 1 0 0 1 1-1h4.954L7.527.337A.5.5 0 0 1 8 0zM2 3v7h12V3H2z" />
                </svg>
                <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px;font-weight: bold;">Graphics</span>
            </summary>
    
            <div class="px-5 px-sm-5" style="display: flex; flex-wrap:wrap;">
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/v.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/rm.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/bts.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/vecteezy_icon-bts-character-a-cute-face-cartoon-suitable-for_11363122.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363157.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/vecteezy_icon-cooky-character-a-cute-face-cartoon-suitable-for_11363158.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/vecteezy_icon-koya-character-a-cute-face-cartoon-suitable-for_11363199.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/vecteezy_icon-rj-character-a-cute-face-cartoon-suitable-for_11363161.jpg" />
                <img draggable="true" dragstart="dragElement(event)" style="cursor: pointer" class="img-fluid" src="./../assets/vecteezy_icon-set-bt21-character-a-cute-face-cartoon-suitable-for_11363192.jpg" />
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
    </template>
    
    <!------------------------------------------script part------------------------------------>
    
    <script>
    
    export default {
        name: "Dra_g",
        data() {
            return {
                imageFile: null,
                input: null,
                isImageUploading: false,
            }
    
        },
        methods: {
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
        }
    }
    </script>
    