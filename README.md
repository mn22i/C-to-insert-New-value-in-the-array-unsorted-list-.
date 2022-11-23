C#-to insert New value in the array unsorted list-
Test Data:
Input the size of array : 3 
Input 3 elements in the array:
element - 0: 5
element - 1 : 3
element - 2 : 9
Input the value to be inserted: 8
Input the Position, where the value to be inserted :2
                 
Expected Output: 
   The exist array list is: 5 3 9
   After Insert the list is: 5 8 3 9



int[] arr = new int[10];

            int n, i, num, loc;

            Console.Write("Input the size of array : ");
            n = Convert.ToInt32(Console.ReadLine());
            Console.Write("Input 3 elements in the array:\n");

            for (i = 0; i < n; i++)
            {
                Console.Write("Element[" + (i ) + "]: ");
                arr[i] = Convert.ToInt32(Console.ReadLine());
            }

            Console.Write("Input the value to be inserted: ");
            num = Convert.ToInt32(Console.ReadLine());

            Console.Write("Input the Position, where the value to be inserted :");
            loc = Convert.ToInt32(Console.ReadLine());

            for (i = n; i >= loc; i--)
            {
                arr[i] = arr[i - 1];
            }
            n++;
            arr[loc - 1] = num;

            Console.Write("\nList After Insertion :");
            for (i = 0; i < n; i++)
            {
                Console.Write(arr[i] + " ");
            }
            Console.ReadLine();
        }
