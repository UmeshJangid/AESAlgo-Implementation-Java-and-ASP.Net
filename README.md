# AESAlgo-Implementation-Java-and-ASP.Net
AES(Advanced Encryption Standards) Algorithm implementation code in java as well in Asp.net(C#) compatible

# About Algorithm(AES):
The Advanced Encryption Standard, also known by its original name Rijndael, is a specification for the encryption of electronic data established by the U.S. National Institute of Standards and Technology in 2001.
AES was developed by two Belgian cryptographers, Vincent Rijmen and Jan Daemen. AES supports 128, 192, and 256 bits key sizes and 128 bits block size.
# Use:
Advanced Encryption Standard (AES) is one of the symmetric encryption algorithms that allows both parties, sender and receiver, to use the same key to encrypt and decrypt data.
This article demonstrates how to use AesManaged class to apply  an AES algorithm to encrypt and decrypt data in .NET C# and Java
The java code below uses a base64 util class from android SDK but you can replace it like with one from ***apache commons***

## Usage(Java/Kotlin and C#)

```java
************************************************************************
  //Java
  
    //Encryption
     String publickey = "Publickey";
        String encryptText = null;
        try {
            encryptText = new Crypto().encrypt("TestPassword", publickey);
        } catch (UnsupportedEncodingException e) {
            e.printStackTrace();
        } catch (InvalidKeyException e) {
            e.printStackTrace();
        } catch (NoSuchAlgorithmException e) {
            e.printStackTrace();
        } catch (NoSuchPaddingException e) {
            e.printStackTrace();
        } catch (InvalidAlgorithmParameterException e) {
            e.printStackTrace();
        } catch (IllegalBlockSizeException e) {
            e.printStackTrace();
        } catch (BadPaddingException e) {
            e.printStackTrace();
        }
        println(encryptText);
        
        //Decryption
        
        String decryptText = null;
        try {
            decryptText = new Crypto().decrypt(encryptText, publickey);
        } catch (GeneralSecurityException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
        }
        println(decryptText);
  
  
  //Kotlin(Android)
  var publickey = applicationContext.resources.getString(R.string.public_key)
        var enc = Crypto().encrypt("TestPassword", publickey)
        Log.e("TAG", enc)
        var dec = Crypto().decrypt(enc, publickey)
        Log.e("TAG", dec)

************************************************************************
C# (Code)
 ***********************************************************************
 string enc = new Crypto().Encrypt("TestPassword", "YourPublicKey");
 Console.WriteLine(enc);
            
 string dec = new Crypto().Decrypt(enc, "YourPublicKey");
 Console.WriteLine(dec);
            
 ************************************************************************




