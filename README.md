# MadlibsP2
UdacityP2

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

    
test_string_1 = "This is a good NOUN to use when you VERB your food"
test_string_2 = "I'm going to VERB to the store and pick up a NOUN or two."
print process_madlib(test_string_1)
print process_madlib(test_string_2)
