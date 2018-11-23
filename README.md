# Korean-Constituency-Parser

본 레포는 end-to-end 한국어 의존 문법 파서의 개발 과정을 담고 있습니다. 국문 문장이 주어졌을때, 파서는 확률이 제일 높은 파싱 결과 N개를 줍니다. Cython으로 컴파일된 .so파일로 제공되며, CLI환경과 파이썬 환경에서 모두 사용할 수 있습니다. 파이썬 환경에서는 다른 모듈처럼 import 키워드로 불러온 후 사용하시면 됩니다 :D

This is a end-to-end Constituency Parser for Korean. Given a Korean sentence, the parser gives you N most likely parses for the sentence. The parser is in the form of  a Cython-compiled .so(dynamic linked library) files, so it is both runnable in CLI environments and Python 
environments. In a Python evironment, the files can be imported using the import keyword like many other Python modules. 

Sample Output:
The below is an example output from the sentence "우리는 누가 보아도 어엿한 대학생이다. 전통에 빛나고 밝은 앞날의 전망을 가진 연세의 대학인이다."
![alt text](https://github.com/PolarBear77/Korean-Constituency-Parser/blob/master/sample_output.jpg)

Sample usages

### Python environment
import RunModel
RunModel.main()
- input_file_path
- output_file_path
- topN

APIs

### Software Dependencies
#### Available through pip:
Keras
numpy <br></br>
cython <br></br>
nltk <br></br>
#### Others:
Foma https://code.google.com/archive/p/foma/

### Resources
Sejong corpus https://ithub.korean.go.kr/user/guide/total/guide1.do
