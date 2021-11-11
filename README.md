# programmers_codingtest
coding
//이상한 문자 만들기 풀이
class Solution {
    public String solution(String s) {
        String answer = "";
        String[] str = s.split("");
        
        int idx = 0;
        for(int i=0; i<str.length; i++){
            if(str[i].equals(" ")){
                idx = 0;
            }else if(idx%2==0){
                str[i] = str[i].toUpperCase();
                idx++;
            }else if(idx%2!=0){
                str[i] = str[i].toLowerCase();
                idx++;
            }
            answer = answer + str[i];
        }
        return answer;
    }
}
핸드폰 번호 가리기
class Solution {
  public String solution(String phone_number) {
    return phone_number.replaceAll(".(?=.{4})", "*");
  }
}
// 패턴공부하기!
