def check(data_type):

    def wrapper(fun):

        def inner_wrapper(*args):
            print(args[0])
            print(data_type)
            print(type(args[0]))
            if type(args[0])==data_type:

                fun(*args)
            
            else:
                print("Not Allow")
        return inner_wrapper    
    
    return wrapper

@check(int)
def main(num):
    print(num**2)
    

a=main(6)

print(a)
