<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=>, initial-scale=1.0">
    <title>STRINGS</title>
</head>
<body>

    <p id="uppercaseString"></p>
    <p id="lowercaseString"></p>
    <p id="substring"></p>
    <p id="foxLocator"></p>
    <p id="lastIndexOfO"></p>
    <p id="CCString1"></p>
    <p id="CCString2"></p>
    <p id="wordCount"></p>


    <script>

        const hw = "Hello, world!";
        const uppercaseString = hw.toUpperCase();  // Default varible hw to UpperCase Format 
        const lowercaseString = hw.toLowerCase();  // Default varible hw to lowercase format 

        console.log(uppercaseString);   // DISPLAYING uppercase
        console.log(lowercaseString);   // Displaying Lowercase 


        // 2 . Create a string containing "JavaScript is awesome!".
        //Use the substring() method to extract the word "awesome" from the string.
        //Print the extracted substring to the console.

        const awesomeString = "JavaScript is awesome!";
        const awesomeIndex = awesomeString.indexOf("awesome");  // To locate particular string 
        const substring = awesomeString.substring(awesomeIndex, awesomeIndex + "awesome".length);  //Remove desire term : Awesome 

        console.log(substring);  // displaying the objective format 

        const allString = "The quick brown fox jumps over the lazy dog";
        const foxLocator = allString.indexOf("fox"); 
        const lastIndexOfO = allString.lastIndexOf("o"); 
        console.log(foxLocator);  
        console.log(lastIndexOfO);  

        function camelcaseConv (str) 
        {
        const words = str.split(/[-_]/);  
        return words.map(word => word.charAt(0).toUpperCase() + word.slice(1)).join("");  
        }
        //map function: The map function is used to iterate through each word in the words array.
        //First letter capitalization: The map function uses word to capitalize each word's initial letter.charAt (0).toUpperCase().
        //Join remaining letters: Next, it uses word to merge the word's remaining letters.slice (1).
        //Add the changed words together: it uses join("") to reunite all of the altered words into a single string.

        const CCString1 = toCamelCase("snake_case");
        const CCString2 = toCamelCase("kebab-case");
        console.log(CCString1);  
        console.log(CCString2); 

        function WordCounter(str) {
        return str.trim().split(/\s+/).length;  
        }

        const wordCount = countWords("for Web Development Class II");

        console.log(wordCount);  // 


    </script>
</body>
</html>
 
