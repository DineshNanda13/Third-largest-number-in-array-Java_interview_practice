# Third-largest-number-in-array-Java_interview_practice
Java program to find third largest number in array
package third_largest;

/**
 *
 * @author Dinesh Nanda
 */
 
public class Third_Largest_In_Array {

    public int third(int[] items) {
        
        int temp;
        int third_largest = 0;
        
        for (int i = 0; i < items.length; i++) {
            for (int j = i + 1; j < items.length; j++) {

                if (items[i] < items[j]) {

                    temp = items[i];
                    items[i] = items[j];
                    items[j] = temp;
                }
            }
        }
        for (int i = 0; i < items.length; i++) {
            if (i == 2) {
                third_largest = items[i];
            }
        }
        return third_largest;
    }

    public static void main(String[] args) {

        int arr[] = {44, 66, 99, 77, 33, 22, 55};

        Third_Largest_In_Array arr_obj = new Third_Largest_In_Array();

        System.out.println("Third largest number in array is: "+arr_obj.third(arr));
    }

}
