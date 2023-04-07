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
                        <button class="nav-link" data-bs-toggle="tab" data-bs-target="#tab1" type="button" role="tab" aria-selected="false">
                            Color
                        </button>
                        <button class="active nav-link" data-bs-toggle="tab" data-bs-target="#tab2" type="button" role="tab" aria-selected="true" tabindex="-1">
                            Image
                        </button>
                    </nav>

                    <!-- tables-->
                    <div class="tab-content" style="background-color: #f5f5f5">
                        <div class="tab-pane fade" id="tab1">
                            <details data-key="color-id">
                                <!-- colors -->
                                <summary class="p-3">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="18" fill="currentColor" class="bi bi-palette" viewBox="0 0 16 16">
                                        <path d="M8 5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zm4 3a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zM5.5 7a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm.5 6a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" />
                                        <path d="M16 8c0 3.15-1.866 2.585-3.567 2.07C11.42 9.763 10.465 9.473 10 10c-.603.683-.475 1.819-.351 2.92C9.826 14.495 9.996 16 8 16a8 8 0 1 1 8-8zm-8 7c.611 0 .654-.171.655-.176.078-.146.124-.464.07-1.119-.014-.168-.037-.37-.061-.591-.052-.464-.112-1.005-.118-1.462-.01-.707.083-1.61.704-2.314.369-.417.845-.578 1.272-.618.404-.038.812.026 1.16.104.343.077.702.186 1.025.284l.028.008c.346.105.658.199.953.266.653.148.904.083.991.024C14.717 9.38 15 9.161 15 8a7 7 0 1 0-7 7z" />
                                    </svg>
                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px; font-weight: bold">Colors</span>
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
                                        <div id="tshirttype">
                                            <details data-key="graphics">
                                                <summary class="pb-3">
                                                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-easel" viewBox="0 0 16 16">
                                                        <path d="M8 0a.5.5 0 0 1 .473.337L9.046 2H14a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1h-1.85l1.323 3.837a.5.5 0 1 1-.946.326L11.092 11H8.5v3a.5.5 0 0 1-1 0v-3H4.908l-1.435 4.163a.5.5 0 1 1-.946-.326L3.85 11H2a1 1 0 0 1-1-1V3a1 1 0 0 1 1-1h4.954L7.527.337A.5.5 0 0 1 8 0zM2 3v7h12V3H2z" />
                                                    </svg>
                                                    <span class="overflow-lines overflow-lines--1 ps-2" style="font-size: 20px; font-weight: bold">Short sleeves Shirt</span>
                                                </summary>
                                                <select v-model="selectedImage">
                                                    <option v-for="image in images" :key="image.id" :value="image.url">{{ image.name }}</option>
                                                </select>
                                            </details>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-lg-5 col-12 d-flex pt-sm-3 pb-sm-3 justify-content-center " :style="{ backgroundColor: BackgroundColor }">
                <!--2nd box-->
                <!-- shirt column -->
                <div  >
                <img :src="selectedImage" alt="Selected Image" v-if="selectedImage" style="position:absolute;z-index:1">
            </div>   
                <div class="product">
                    <img src="./assets/casual-white-blouse-women-rsquo-s-fashion.png" alt="without background" class="img-1" />
                    <img src="./assets/blouse-women-rsquo-s-fashion.png" alt="with background" class="img-2" />
                    <div class="color"></div>                  
                </div>
           
            </div>
            <thirdColumn />  <!-- 3rd div -->  
        </div>
    </div>
</div>
</template>

    
         <!--------------------------------------------------------------script------------------------------------------------------------------->

<script>
import thirdColumn from "./components/thirdColumn";

export default {
    name: "app",
    props: ["id"],
    components: {
        thirdColumn,
    },

    mounted() {
        //Get elements from the DOM
        const color = document.querySelector(".color");
        const colorInput = document.querySelector(".color-input");
        //Add input event listener
        colorInput.addEventListener("input", () => {
            /*Set background of the color div to
                  the color set in the input field*/
            color.style.backgroundColor = colorInput.value;
        });
    },
    data() {
        return {
            BackgroundColor: "#ffffff",
            active: false,
            getText: true,
            imageFile: null,
            input: null,
            isImageUploading: false,
            selectedImage: '',
            images: [{
                    id: 1,
                    name: "Orange color short sleeve shirt",
                    url: "https://svgsilh.com/svg/303329-ff5722.svg",

                },
                {
                    id: 2,
                    name: "Red color short sleeve shirt",
                    url: "https://media.istockphoto.com/id/1354031012/photo/red-t-shirt-mockup-men-as-design-template-tee-shirt-blank-isolated-on-white-front-view.jpg?s=612x612&w=0&k=20&c=_5QLLkUa0-ZzSK1rp6Ie-ZRBPOEku4as4ZMrZg-y2GI=",

                },
                {
                    id: 3,
                    name: "Pink color short sleeve shirt",
                    url: "https://www.mdtextile.com/images/stories/virtuemart/product/foursquare-160gsm-roundneck-pink-tshirt.jpg",

                },
                {
                    id: 4,
                    name: "Purple color short sleeve shirt",
                    url: "https://i.pinimg.com/474x/21/49/63/2149635c5faa59c25455914543248328.jpg",

                },
                {
                    id: 5,
                    name: "Purple color short sleeve shirt",
                    url: "https://media.istockphoto.com/id/1209887384/photo/green-t-shirt-isolated-on-white-background.jpg?s=612x612&w=0&k=20&c=8M4gaRs-fUz6CdYEl4OblIoDvNjcRs8_Sbzs0VxWlMY=",

                },
                {
                    id: 6,
                    name: "Brown color short sleeve shirt",
                    url: "https://image.s5a.com/is/image/saks/0400017061182_DUST?wid=480&hei=640&qlt=90&resMode=sharp2&op_usm=0.9,1.0,8,0",

                },
               
                
            ],
            
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
    },
};
</script>
          
          <!------------------------------------------------------------- style-------------------------------------------------------------------->

<style src="./css/style.css"></style>
