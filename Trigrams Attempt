#include <iostream>
#include <string>
#include <vector>
#include<fstream>
#include <cstring>
#include <algorithm>
using namespace std;
class Trigrams
{
protected:
string record1, record2, record3, record4;
string firstLine;
int counted , sortedAlphabets;
string doubleRecord , thirdRecord;
vector <char> allThirdCharacter;
vector<string> twoCharacter;
vector<int>alphabetsCounter;
//vector<int>sortedAlphabets;
int counters[256] = {0};
char storage;
public:
void loadText()
{
string fileName = "dictionary.txt";
ifstream myfile(fileName);
if (myfile.is_open())
{
while (!myfile.eof())
{
getline(myfile,record1);
getline(myfile, record2);
getline(myfile, record3);
getline(myfile, record4);
}
}
myfile.close();
};
void readCharacter()
{
int count = 0 ,t;
for (int i = 0; i < record1.length(); i++)
{
string doubleRecord = string() + record1[i] + record1[i + 1];
twoCharacter.push_back(doubleRecord);
//string thirdRecord = string() + record1[i + 3];
//thirdCharacter.push_back(thirdRecord);
//cout << doubleRecord << endl;
}
for (int p = 0; p < twoCharacter.size(); p++)
{
for (int t = 0;t < record1.length();t++)
{
if (twoCharacter[p].back() == record1[t])
{
//cout << record1[t + 1] << endl;

char storage = record1[t + 1];
allThirdCharacter.push_back(record1[t + 1]);
}
}
}
}
void Occurence()
{
for(int i=0;i<allThirdCharacter.size();i++)
{
counters[allThirdCharacter[i]]++;
alphabetsCounter.push_back(counters[allThirdCharacter[i]]);
counted = counters[allThirdCharacter[i]];
}
sort(alphabetsCounter.rbegin(),alphabetsCounter.rend());
// cout << alphabetsCounter[0] << endl;
//cout << alphabetsCounter[1] << endl;
//cout << alphabetsCounter[2] << endl;
//The highest occurence number is " ","n" , "r"
}

void randomWords()
{
for (int i =0;i<allThirdCharacter.size();i++)
{
random_shuffle(allThirdCharacter.begin(), allThirdCharacter.end());
for(int e =0 ; e < 10 ; e++)
{
cout << allThirdCharacter[0] << allThirdCharacter[1] << allThirdCharacter[4] <<
allThirdCharacter[3]
<< endl;
}
}
}
void finalCountdown()
{
string wordTest;
cout << "Enter two character for occurence check" << endl;
cin >> wordTest;
for (int c = 0; c < twoCharacter.size(); c++)
{
for(int r =0 ; r < record1.length();r++)
{
if(wordTest == twoCharacter[c])
{
if(wordTest.back() == record1[r])
{
for(int i=0;i<allThirdCharacter.size();i++)
{
cout << allThirdCharacter[1] << allThirdCharacter [20] << allThirdCharacter[6] <<endl;
break;
}
}
}

}
}
}
};

int main()
{
Trigrams theT;
theT.loadText();
theT.readCharacter();
theT.Occurence();
//theT.randomWords();
theT.finalCountdown();
system("pause");
}
