# Test-1
#mod and packages 
#def say_hello(name='world', greeting =None):
    # if greeting==None:
    #  print(f'Hello {name}!')
    # else:
    #   print(f'{greeting} {name} !')
    

# say_hello()
# say_hello('Bob')
# say_hello(greeting='Howdy')
# say_hello('Bob','Howdy')

# def add_two_numbers(x,y):
#     return x + y

# add_two_numbers (4,6)
# result = add_two_numbers (5,7)
# print (result)

#list returning funktions 

def create_deck():
    suits = ['Hearts','Sapdes', 'Clubs','Diamonds']
    ranks = ['2','3','4','5','6','7','8','9','10','Jack','Queen','king','Ace']
    deck = []

    for suit in suits:
        for rank in ranks:
            deck.append(f'{rank} of {suit}')

    return deck

my_deck = create_deck()
print(len(my_deck))

# arbitrary arguments list *args
def print_args(*args):
    for arg in args:
        print (f'arg={arg}')
    
print_args('a')

# named arguments 

def print_keyword_args(**kwargs):

  print('\n')

  for key, value in kwargs.items():
    print(f'{key} = {value}')

  third = kwargs.get('third', None)
  if third != None:
    print('third arg =', third)


print_keyword_args(first='a')
print_keyword_args(first='b', second='c')
print_keyword_args(first='d', second='e', third='f')
