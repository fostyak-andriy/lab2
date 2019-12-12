message = input("Enter massage: ")
version = input("select a or b: ")

def remove_message(txt):
    final_list = []
    for num in txt:
        if num not in final_list:
            final_list.append(num)
    return final_list

if version == "a":
    for char in message:
        if (char != " ") & (not char.isalpha()):
            message = message.replace(char, "")

    words = message.split()
    words.sort()
    print("sorted words")
    print(remove_message(words))

if version == "b":
    for char in message:
        if not char.isalpha():
            message = message.replace(char, "")
    letter = { }
    for x in message:
        if x in letter:
            letter[x] += 1
        else:
            letter[x] = 1
    print("number letter :\n" + str(letter))

