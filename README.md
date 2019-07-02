# ssh_test
test the ssh
/*-------------- solution1:C_Style using fopen()------------------*/
//filePaths //iter storing the a series of img paths
char fname[50];
for (auto &itr : filePaths){
	strcpy(fname, itr);
	f = fopen(fname,'rb')
}

/*-------------- solution2:C++_Style using fin.open()------------------*/
std::ifstream fin;
char *pFile;
fin.open("../txt.json", std::ios::in | std::ios::binary);
if(!fin)
{
std::cout << "文件打开失败！" << std::endl;
}
else
{
fin.seekg(0, std::ios::end);
unsigned int size = fin.tellg();
pFile = new char[size + 1];
pFile[size] = 0;
fin.seekg(std::ios::beg);
fin.read(pFile, size);
}
fin.close();
