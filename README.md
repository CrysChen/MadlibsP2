# MadlibsP2
UdacityP2
# Let's put it all together. Write code for the function process_madlib, which takes in 
# a string "madlib" and returns the string "processed", where each instance of
# "NOUN" is replaced with a random noun and each instance of "VERB" is 
# replaced with a random verb. You're free to change what the random functions
# return as verbs or nouns for your own fun, but for submissions keep the code the way it is!

from random import randint

def random_verb():
    random_num = randint(0, 1)
    if random_num == 0:
        return "run"
    else:
        return "kayak"
        
def random_noun():
    random_num = randint(0,1)
    if random_num == 0:
        return "sofa"
    else:
        return "llama"

def word_transformer(word):
    if word == "NOUN":
        return random_noun()
    elif word == "VERB":
        return random_verb()
    else:
        return word
def show_word_sub(new,old):
    number_new=len(new)
    number_old=len(old)
    return new[number_old+1:number_new-1]
def stringtoge(this, that)
    m = this[:]
    n = that[:]
    return m+n
    
def process_madlib(mad_lib):
    i=0
    while mad_lib[i]!="":
        if mad_lib[i]!=" ":
            while mad_lib[i]!=" ":
                i=i+1
            catch_word = mad_lib[:i-1]
            processed=""
            catch_word = show_word_sub (catch_word,processed)
            processed = stringtoge (processed,word_transformer(catch_word))
        processed = stringtoge (processed," ")
        mad_lib=show_word_sub(mad_lib,processed)
        i+=1
    # your code here
    # you may find the built-in len function useful for this quiz
    # documentation: https://docs.python.org/2/library/functions.html#len
    
test_string_1 = "This is a good NOUN to use when you VERB your food"
test_string_2 = "I'm going to VERB to the store and pick up a NOUN or two."
print process_madlib(test_string_1)
print process_madlib(test_string_2)
