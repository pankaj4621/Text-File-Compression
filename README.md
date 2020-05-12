# Text-File-Compression
<h2>Compression and Decompression of text file using Huffman Coding</h2>
<h3>Program is divided into two parts:</h3>
<h4>1. Compression<br></h4>
<h4>2. Decompression</h4>


<h3>Compression implementation include following steps:</h3>

Step1: Create Dictionary to store frequency of diffrent elements in the text.<br>
Step2: Construct a heap based on minimum frequency priority i.e. element with least frequency will be the root and so on.<br>
Step3: Construct a binary tree from heap by selecting two nodes having least frequencies and merge them and push that back in        the heap.<br>
Step4: Repeat step 3 until there is just one node left in the heap.<br>
Step5: Construct the huffman code for each element by placing 0 on the left child and 1 on the right child. Do it        recurrsively to cover all the nodes in the binary tree. This will create huffman codes for each elements.<br>
Step6: Encode the text using huffman codes we obtained from the binary tree.<br>
Step7: Pad the encoded text with 0 to make it's size in the multiples of 8.<br>
Step8: Create an array where every 8 elements are represented by a decimal number.<br>
Step9: Now create the final encoded text by converting the elements of array into bytes.<br>
Step10:Now write the final encoded text into output file of .bin extension.<br>


<h3>Decompression implementation include following steps:<br></h3>

Step1: Convert the data of the output file into their unicodes.<br>
Step2: Convert all the unicodes into binary numbers.<br>
Step3: Remove padding that we did while compressing the file.<br>
Step4: Decode the binary numbers into the chracters based on the dictionary containing key value pair.<br>
Step5: Now, write the final text into the output file of .txt extension.<br>



