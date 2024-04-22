morse_dict = {
    'A': '.-', 'B': '-...', 'C': '-.-.', 'D': '-..', 'E': '.', 'F': '..-.', 'G': '--.', 'H': '....',
    'I': '..', 'J': '.---', 'K': '-.-', 'L': '.-..', 'M': '--', 'N': '-.', 'O': '---', 'P': '.--.',
    'Q': '--.-', 'R': '.-.', 'S': '...', 'T': '-', 'U': '..-', 'V': '...-', 'W': '.--', 'X': '-..-',
    'Y': '-.--', 'Z': '--..', '1': '.----', '2': '..---', '3': '...--', '4': '....-', '5': '.....',
    '6': '-....', '7': '--...', '8': '---..', '9': '----.', '0': '-----', ', ': '--..--', '.': '.-.-.-',
    '?': '..--..', '/': '-..-.', '-': '-....-', '(': '-.--.', ')': '-.--.-', ' ': '/'
}
def Encript(Message):
  cipher = ""
  for letter in Message:
    if letter != " ":
      cipher += morse_dict[letter] + " "
    else:
      cipher += " "
  return cipher

def Decript(Message):
  Message += " "
  decipher = " "
  citext = " "
  for letter in Message:
    if letter != " ":
      i = 0
      citext += letter
    else:
      i += 1
      if i == 2:
        decipher += " "
      else:
        decipher += list(morse_dict.keys())[list(morse_dict.values()).index(citext)]
        citext = " "
def main():
  message = "Avyukt"
  result = Encript(message.upper())
  print (result)

 # message = ".- ...- -.-- ..- -.- - "
 # result = Decript(message)
  #print (result)

if __name__ == '__main__':
  main() 
  
            
       
      
