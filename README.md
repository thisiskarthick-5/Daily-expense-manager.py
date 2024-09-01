# Daily-expense-manager.py
created using python

#expense tracker

      import csv
      
      def display():
          print("\n 1. Add Expense")
          print("2.View Expense ")
          print("3.Total")
          print("4.Exit")
          
      def add_ex(amount):
          usage = input("Enter the usage : ")
          ex_amount = float(input("Enter the Expense Amount : "))
          amount.append((usage,ex_amount))
          print(f"Added expense {usage} - ${ex_amount}")
          
      def view_ex(amount):
          print("\n All expense ") 
          for usage,ex_amount in amount:
              print(f"{usage} : ${ex_amount}")
              
      def view_total_expense(amount):
          totals = {}
          for usage,ex_amount in amount:
              if usage in totals:
                  totals[usage] += ex_amount
              else:
                  totals[usage] = ex_amount
                
          for usage,total in totals.items():
              print(f"{usage} : ${total1:.2f}")
              
      def main():
          
          amount = []
          
          while True:
              
              display()
              choice = input("Enter the choice = ")  
              
              if choice == '1':
                  add_ex(amount)
              elif choice == '2':
                  view_ex(amount)
                  
              elif choice == '3':
                  view_total_expense(amount)
              elif choice == '4':
                  print("good bye")
                  break
              else:
                  print("invalid choice ")
                  
              
      if __name__ == "__main__":
          main()

          
            
                
                      
                           
    
    
        
