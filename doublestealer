import os

path = "./"
m3u8_file = input ("File with m3u adresses:")
m3u8_list = open (m3u8_file, "r")
num = 1

if not os.path.exists(path):
    os.mkdir(path)
    print("Folder created")

for link in m3u8_list:
    os.system ("ffmpeg -i '" + link.strip () + "' -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 " + path + "/ep_" + str (num) + ".mkv")
    print ("Епізод №" + str (num) + " завантажено!")
    num += 1
