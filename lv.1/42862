import java.util.Arrays;

public class Solution {

    public static void main(String[] args) {
        int n = 3;
        int[] lost = {1,2};
        int[] reserve = {2,3};

        System.out.println(solution(n, lost, reserve));
    }

    public static int solution(int n, int[] lost, int[] reserve) {
        Arrays.sort(lost);
        Arrays.sort(reserve);

        int answer = n - lost.length;
        int llen = lost.length;
        int rlen = reserve.length;

        for(int i = 0; i < llen; i++) {
            for(int j = 0; j < rlen; j++) {
                if(lost[i] == reserve[j]) {
                    answer++;
                    reserve[j] = -100;
                    lost[i] = -100;
                    break;
                }
            }
        }

        for(int l : lost) {
            for(int i = 0; i < rlen; i++) {
                if(l == reserve[i]-1 || l == reserve[i]+1) {
                    answer += 1;
                    reserve[i] = -1;
                    break;
                }
            }
        }

        return answer;
    }
}
