<template>
    <v-container>
        <v-btn @click="saveFile" color="primary">Save File</v-btn>
    </v-container>
</template> 
<script>
import { saveAs } from 'file-saver';
import  JSZip  from 'jszip';
export default {
    created(){
        
    }, 

    methods: {
        saveFile: function() {        
            var zip = new JSZip();
            zip.file("common.xml", "This is where we generate the xml");
            zip.file("definition.xml", "This is where we generate the xml");
            //zip.file("thumbnail.png", "We should select a thumbnail and set it");
            zip.generateAsync({type:"blob"})
            .then(function(content) {
                saveAs(content,"module.mod");
            });
 
        }
    }
} 
        
</script>