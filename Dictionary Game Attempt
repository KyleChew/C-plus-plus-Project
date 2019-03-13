#include <iostream>
#include <fstream>
#include <string>
#include <vector>
#include <algorithm>
using namespace std;

class Word
{
protected:
string word;
string definition;
string wordtype;
public:
Word()
{
}
Word(string word, string definition, string wordtype)
{
this->word = word;
this->definition = definition;
this->wordtype = wordtype;
}
void setWord(string wordInput)
{
word = wordInput;
}
void setDefinition(string definitionInput)
{
definition = definitionInput;
}
void setWordType(string wordtypeInput)
{
wordtype = wordtypeInput;
}
string getWord()
{
return word;
}
string getDefinition()
{
return definition;

}
string getWordType()
{
return wordtype;
}
bool isNoun()
{
if (wordtype == "n")
{
return true;
}
return false;
};

bool isVerb()
{
if (wordtype == "v")
{
return true;
}
return false;
}
};

class Dictionary
{
private:
string record1, record2, record3, record4;
int i;
vector <Word> theNouns;
vector <Word> theVerbs;
string enterWord;
bool tryAgain = true;
public:
vector<Word> thedictionary;
void loadDictionary()
{
// a vector to hold all the employees from the file
string filename = "dictionary.txt";
ifstream myfile(filename);
Word everyword;
Word nouns;
if (myfile.is_open())

{
while (!myfile.eof())
{
getline(myfile, record1);
everyword.setWord(record1);
//cout << "this is the word name :" << everyword.getWord() << endl;

getline(myfile, record2);
everyword.setDefinition(record2);
//cout << "this is the definition :" << everyword.getDefinition() << endl;

getline(myfile, record3);
everyword.setWordType(record3);
//cout << "this is the word type:" << everyword.getWordType() << endl;
getline(myfile, record4);
thedictionary.push_back(everyword);
//cout << thedictionary[i].getWord()<<endl;
// i++;
bool nounTrue = false;
bool verbTrue = false;
nounTrue = everyword.isNoun();
verbTrue = everyword.isVerb();
if (nounTrue == true)
{
theNouns.push_back(everyword);
}
if (verbTrue == true)
{
theVerbs.push_back(everyword);
}
}
}
myfile.close();
}

/*void getTotalNumberOfWords1()
{
while (tryAgain = true)
{
cout << "what is the word you want def for :" << endl;
cin >> enterWord;

for (int i = 0; i < thedictionary.size(); i++)
{
if (enterWord == thedictionary[i].getWord())
{
cout << thedictionary[i].getDefinition() << endl;
tryAgain = false;
break;
}
else
{
tryAgain = true;
}
}
if (tryAgain == true)
{
cout << "please try again" << endl;
}
if (tryAgain == false)
{
break;
}
}
};

void getTotalNumberOfWords2()
{
for (i = 0; i < thedictionary.size();i++)
{
string str = thedictionary[i].getWord();
size_t found = str.find("z");
int iFoundTheLetterYo = 0;
if (found != string::npos)
{
for (int j = 0; j < str.length();j++)
{
if (str[j] == 'z')
{
iFoundTheLetterYo++;
if (iFoundTheLetterYo > 3)
{
cout << "\nthe word with 3 z's is :" << str << endl;
}
}
}
}
}
};
void getTotalNumberOfWords3()
{
cout << "\nthe word with q but no u after is : " << endl;
for (i = 0; i < thedictionary.size();i++)
{
string str = thedictionary[i].getWord();

size_t found = str.find("q");
if (found != string::npos)
{
for (int j = 0; j < str.length();j++)
{
if (str[j] == 'q')
{
if (str[j + 1] != 'u')
{
cout << str << endl;
}
}
}
}
}
};*/
void printNounVerb()
{
cout << "The words that is noun and verb are : " << endl;
for (int i = 0; i < theNouns.size(); i++)
{
cout << theNouns[i].getWord() << endl;
}
for (int v = 0; v < theVerbs.size(); v++)
{
cout << theVerbs[i].getWord() << endl;
}
}
void printPalindromes()
{
for (int i = 0; i < thedictionary.size(); i++)
{
string str = thedictionary[i].getWord();
if (str == string(str.rbegin(), str.rend()))
{
cout << str << " is a palindrome" << endl;
}
}
};
void showAnagrames()
{
vector<string>alphabets1;
vector<string>alphabets2;
string wordSelection;
cout << "what is the word that you want to find its anagram: " << endl;
cin >> wordSelection;
string str1 = wordSelection;
sort(wordSelection.begin(), wordSelection.end());

for (i = 0; i < thedictionary.size();i++)
{
string str2 = thedictionary[i].getWord();
sort(str2.begin(), str2.end());
if (wordSelection == str2)
{
cout << "The anagram is :" << thedictionary[i].getWord() << endl;
}
}
};
void guessGame()
{
string nounInput;
string nounInput2;
string nounInput3;
for (i = 0; i< theNouns.size();i++)
{
random_shuffle(theNouns.begin(), theNouns.end());
}
cout << "The definition of the word is :" << theNouns[3].getDefinition() << endl;
cout << "The length of the word is :" << theNouns[3].getWord().length() << endl;
cout << "Guess that Noun:" << endl;
cin >> nounInput;
string str = theNouns[3].getWord();
if (nounInput == str)
{
cout << "Congratulations you got it " << endl;
}
if (nounInput != str)
{
cout << "the first letter of the noun is: " << str[0] << endl;
cout << "Try again,guess that noun: " << endl;
cin >> nounInput2;
if (nounInput2 == str)
{
cout << "Congratulations you got it " << endl;
}
if (nounInput2 != str)
{
cout << "The second letter of the noun is: " << str[1] << endl;
cout << "Last chance try again,noun: " << endl;
cin >> nounInput3;
if (nounInput3 == str)
{
cout << "Congratulations you got it " << endl;
}
if (nounInput3 != str)
{
cout << "Sorry no more tries,the noun was : " << str << endl;
}
}
}
}
};
class Noun : public Word
{
};

class Verb : public Word
{
};
class Adverb :public Word
{
};
class Adjective : public Word
{
};
class MiscWord:public Word
{
};
class Preposition :public MiscWord
{
};
class properNoun : public Noun
{
};
class NounAndVerb:public Noun , public Verb
{
};
int main()
{
Dictionary theDictionary;
theDictionary.loadDictionary();
//theDictionary.getTotalNumberOfWords1();
//theDictionary.getTotalNumberOfWords2();
//theDictionary.getTotalNumberOfWords3();
//theDictionary.printNounVerb();
//theDictionary.printPalindromes();
//theDictionary.showAnagrames();
//theDictionary.guessGame();
system("pause");
return 0;
};
