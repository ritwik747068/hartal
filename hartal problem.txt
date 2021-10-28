#include <stdio.h>
#include <string.h>

//using namespace std;

int main(){
    int T,N,P,a[100],found,i,j,ans;
   
    scanf("%d",&T);
   
    while(T--){
        scanf("%d %d",&N,&P);
       
        for(i = 0;i<P;++i) scanf("%d",&a[i]);
       
        ans = 0;
       
        for(i = 1;i<=N;++i){
            if(i%7==6 || i%7==0) continue;
           
            found = 0;
           
            for(j = 0;j<P;++j)
                if(i%a[j]==0)
                    found = 1;
           
            if(found) ++ans;
        }
       
        printf("%d\n",ans);
    }
   
    return 0;
}