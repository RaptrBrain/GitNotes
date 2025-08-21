 
file = open("news02.txt")
know = file.read()

# print(know)
if "Coronavirus" in know:
	print("Crime Patrol")
elif "Trafficking" in know:
	print("Damn, they took the girls again")
else:
	print ("Nothing good to read")


file = open("email.txt")
know = file.read()

#print(know)

words=know.split()
#print(words)

my_names = []
for item in words:
	if "@" in item and ".com" in item:
		updated = item.replace(";", "").replace(",","").replace("<","").replace(">","")
		if updated not in my_names:
			my_names.append(updated)

print(my_names)

new_File = open("My first file.txt","w")
for row in my_names:
	new_File.write(row + "\n")
new_File.close()


