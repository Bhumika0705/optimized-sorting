# optimized-sorting
optimized sorting in java
public class optimizeSorting {
    public optimizeSorting() {
    }

    static void OptimizeSort(int[] a) {
        int n = a.length;

        for(int i = 0; i <= n - 1; ++i) {
            boolean flag = false;

            for(int j = 0; j <= n - i - 1; ++j) {
                if (flag) {
                    return;
                }

                if (a[j] > a[j + 1]) {
                    int temp = a[j];
                    a[j] = a[j + 1];
                    a[j + 1] = temp;
                }
            }
        }

    }

    public static void main(String[] args) {
        int[] a = new int[]{0, 2, 4, 5, 6};
        OptimizeSort(a);
        int[] var2 = a;
        int var3 = a.length;

        for(int var4 = 0; var4 < var3; ++var4) {
            int i = var2[var4];
            System.out.println("" + i + " ");
        }

    }
}

