
### Phase 0 Week 2_Jumat - Solve Problems menggunakan JavaScript


Student : Tunggul Sutrambuko Mubowo  
Class : VictoryFox

#### [Exercises 10] Bandingkan Angka
##### Logic Challenge - Bandingkan Angka

#### Problem

Diberikan sebuah function bandingkanAngka(angka1, angka2) yang menerima dua parameter angka. Function akan me-return nilai true jika angka2 lebih besar dari angka1, dan false jika sebaliknya. Jika kedua angka bernilai sama, function akan me-return -1.

#### Code


```javascript
function bandingkanAngka(angka1, angka2) {
  // you can only write your code here!
    if (angka2 > angka1)
        {
            return true;
        }
    else if (angka2 === angka1)
        {
            return -1;
        }
    else { return false;}
}

// TEST CASES
console.log(bandingkanAngka(5, 8)); // true
console.log(bandingkanAngka(5, 3)); // false
console.log(bandingkanAngka(4, 4)); // -1
console.log(bandingkanAngka(3, 3)); // -1
console.log(bandingkanAngka(17, 2)); // false
```

    true
    false
    -1
    -1
    false


### [Exercises 11] Balik Kata  
#### Logic Challenge - Balik Kata

#### Problem  

Diberikan sebuah function balikKata(kata) yang menerima satu parameter berupa string. Function akan me-return kata yang dibalik. Contoh, jika kata adalah "John Doe", function akan me-return "eoD nhoJ".

#### Code


```javascript
// Function Balik Kata using For Loop

function balikKata(kata) {
  // you can only write your code here!
    
    var storeWord = "";
           
    for(a = kata.length-1;  a >= 0 ; a--)
        {
            storeWord = storeWord + kata[a];
        }
    return storeWord;
}

// TEST CASES
console.log(balikKata('Hello World and Coders')); // sredoC dna dlroW olleH
console.log(balikKata('John Doe')); // eoD nhoJ
console.log(balikKata('I am a bookworm')); // mrowkoob a ma I
console.log(balikKata('Coding is my hobby')); // ybboh ym si gnidoC
console.log(balikKata('Super')); // repuS
```

    sredoC dna dlroW olleH
    eoD nhoJ
    mrowkoob a ma I
    ybboh ym si gnidoC
    repuS



```javascript
// Function balik kata using while loop

function balikKata(kata) {
  // you can only write your code here!
    
    var storeWord = "";
    var a = kata.length;
           
    while (a > 0)
        {
            storeWord = storeWord + kata.substring(a - 1, a);
            a = a - 1;
            
        } return storeWord;
    
} 

// TEST CASES
console.log(balikKata('Hello World and Coders')); // sredoC dna dlroW olleH
console.log(balikKata('John Doe')); // eoD nhoJ
console.log(balikKata('I am a bookworm')); // mrowkoob a ma I
console.log(balikKata('Coding is my hobby')); // ybboh ym si gnidoC
console.log(balikKata('Super')); // repuS
```

    sredoC dna dlroW olleH
    eoD nhoJ
    mrowkoob a ma I
    ybboh ym si gnidoC
    repuS


### [Exercises 12] Konversi Menit  

#### Logic Challenge - Konversi Menit

#### Problem  

Diberikan sebuah function konversiMenit(menit) yang menerima satu parameter berupa angka yang merupakan ukuran waktu dalam menit. Function akan me-return string waktu dalam format jam:menit berdasarkan menit tersebut. Contoh, jika menit adalah 63, maka function akan me-return "1:03".

##### Code


```javascript

function konversiMenit(menit) {
  // you can only write your code here!
    
    var jamMenit = 0;
    var sisaMenit = 0;
    
     
    jamMenit = Math.floor(menit / 60);
    sisaMenit = (menit % 60);
    
    if (sisaMenit < 10)
        {
            sisaMenit = '0' + sisaMenit;
        }
    
    return (jamMenit+":"+sisaMenit);
    
}

// TEST CASES
console.log(konversiMenit(63)); // 1:03
console.log(konversiMenit(124)); // 2:04
console.log(konversiMenit(53)); // 0:53
console.log(konversiMenit(88)); // 1:28
console.log(konversiMenit(120)); // 2:00
```

    1:03
    2:04
    0:53
    1:28
    2:00


### [Exercises 13] X dan O  

#### Logic Challenge - X dan O

#### Problem  

Diberikan sebuah function xo(str) yang menerima satu parameter berupa string. Function akan me-return true jika jumlah karakter x sama dengan jumlah karakter o, dan false jika tidak.

#### Code


```javascript


function xo(str) {
  // you can only write your code here!
        
    var cariCharacter = "";
    var counter1 = 0;
    var counter2 = 0;
    
      
    for(var a = 0; a < str.length; a++)
        {
            //console.log(str.length);
            
            cariCharacter = cariCharacter + str[a];
            
            if (cariCharacter[a] === "x") 
                {
                   
                    counter1 = counter1 + 1;
                }
                
            else if (cariCharacter[a] === "o")
                {
                    counter2 = counter2 + 1;
                }
        };
    
           
        if (counter1 == counter2)
            {
                return true;
            }
        else 
            {
                return false;
            }
}

// TEST CASES
console.log(xo('xoxoxo')); // true
console.log(xo('oxooxo')); // false
console.log(xo('oxo')); // false
console.log(xo('xxxooo')); // true
console.log(xo('xoxooxxo')); // true
```

    true
    false
    false
    true
    true

