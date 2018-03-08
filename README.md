# Image-Encryption-using-AES-and-Shuffing
Basic encryption for an image.
First, we are encrypting this image by converting this image to string format and applying AES
and after that we are using modified version (2,n)Share Encryption for better results. For
decryption , we are using Secret image generated during encryption.

Modified (2,n)Share Encryption:
In this scheme we have a secret image which is encoded into N shares printed on
transparencies. The shares appear random and contain no decipherable information about the
underlying secret image, however if any 2 of the shares are stacked on top of one another the
secret image becomes decipherable by the human eye.
Every pixel from the secret image is encoded into multiple subpixels in each share image using a
matrix to determine the color of the pixels. In the (2,N) case a white pixel in the secret image is
encoded using a matrix from the following set, where each row gives the subpixel pattern for
one of the components.
Modification -: As this algo uses 1bit pixel image and we are working on rgb(3X8 byte pixel)
images, So we are shuffling it with 0 to 255 bits for each layer and generating secret image and
after that we are encrypting our message image by using (mssg[i]+seret[i])%256 and decrypting
using (cipher[i]-secret[i])%256.

Platform Used
1. Python 2.7
2. Linux
