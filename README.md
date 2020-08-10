# Python_menu
#Computing bill for selected items


#This code calculates the bill to make a burrito
#Meat options are Chicken, Pork, Steak, Tofu.
#Rice and Beans can be chosen extra.
#Guacamole, cheese, corn can be add-ons


class Meat:
    def __init__(self, value=False):
        self.set_value(value)
            
    def get_value(self):
        return self.value
    
    def set_value(self, value):
        if value in ["chicken", "pork", "steak", "tofu"]:
            self.value = value
        else:
            self.value = False

class Rice:
    def __init__(self, value=False):
        self.set_value(value)
            
    def get_value(self):
        return self.value
     
    
    def set_value(self, value):
        if value in ["brown", "white"]:
            self.value = value
        else:
            self.value = False
            
class Beans:
    def __init__(self, value=False):
        self.set_value(value)
            
    def get_value(self):
        return self.value
    
    def set_value(self, value):
        if value in ["black", "pinto"]:
            self.value = value
        else:
            self.value = False
            

            
#Add and modify your code here!



class Burrito():
    def __init__(self,meat,to_go,rice,beans,extra_meat=False,guacamole=False,cheese=False,pico=False,corn=False):
              
        self.meat = Meat(meat)
        
        self.m = Meat(meat).get_value()
   
        self.to_go = to_go
        
        self.rice = Rice(rice)
        
          
        self.beans = Beans(beans)
         
        self.extra_meat = extra_meat
          
        self.guacamole = guacamole         
 
        self.cheese = cheese
             
        self.pico = pico      
        
        self.corn = corn
          
    def get_meat(self):
        return self.meat
    
    def get_to_go(self):
        return self.to_go
    
    def get_rice(self):
        return self.rice
    
    def get_beans(self):
        return self.beans
    
    def get_extra_meat(self):
        return self.extra_meat
    
    def get_guacamole(self):
        return self.guacamole
    
    def get_cheese(self):
        return self.cheese
    
    def get_pico(self):
        return self.pico
    
    def get_corn(self):
        return self.corn
    
    
    def set_meat(self,meat):
        self.meat = meat

            
  
    def set_to_go(self,to_go):
        self.to_go = to_go

    
    def set_rice(self,rice):
        self.rice = rice

        
    def set_beans(self,beans):
        self.beans = beans
        
    def set_extra_meat(self,extra_meat):
        self.extra_meat = extra_meat

        
    def set_guacamole(self,guacamole):
        self.guacamole = guacamole

        
    def set_cheese(self,cheese):
        self.cheese = cheese

        
    def set_pico(self,pico):
        self.pico = pico

        
    def set_corn(self,corn):
        self.corn = corn
        
    def get_cost(self):
            
        baseCost = 5.0
        lst = ["chicken","pork","tofu"]
        print(self.m)
        
        if meat in lst:
            baseCost += 1
                
        if self.meat == "steak":
            baseCost += 1.5
            
        if self.extra_meat == True and self.meat != False:
            baseCost += 1      
            
        if self.guacamole == True:
            baseCost += 0.75
    
        return baseCost
 # Remove the following two lines from comments and execute the program. 
 """Code to check the program, creates an instance called a_burrito with unique specifications and uses internal method to return the cost.
 
 a_burrito = Burrito("pork", False, "white", "black", extra_meat = True, guacamole = True)
 print(a_burrito.get_cost())"""
           
