# Hartals-Uva10050-solution-
#include <bits/stdc++.h>
using namespace std;

int main() {
	int tc=0;
	scanf("%d",&tc);
	while(tc--){
		
		int t=0;
		scanf("%d",&t);
		int simulation[t+1];//for how many days the process will run
		
		int sum=6;
		
		for(int i=0;i<=t;i++){
			simulation[i]=0;
		}
		int r=0;//how many working days will be wasted 
		int tParty=0;
		scanf("%d",&tParty);//number of political parties
		for(int i=0;i<tParty;i++){
			sum=6;
			//r=0;
			int h=0;//gap between hartal
			scanf("%d",&h);
			for(int j=h;j<=t;j=j+h){
				
				//cout<<j<<" samner sukrobar"<<sum<<endl;
				if((j%7)!=0&&(j%7)!=6){
					//cout<<sum<<endl;
					if(simulation[j]==0){
					  simulation[j]=1;
					  r++;
					  
				}
				if(j>=sum){
					  	sum=sum+7;
				}
				
			}
		}
	
		}
		//cout<<endl;
		cout<<r<<endl;
	}
	return 0;
}
