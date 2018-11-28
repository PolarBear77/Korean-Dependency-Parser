# Korean-Dependency-Parser

본 레포는 end-to-end 한국어 의존 문법 파서의 개발 과정을 담고 있습니다. 국문 문장이 주어졌을때, 파서는 확률이 제일 높은 파싱 결과 N개를 줍니다. 현재는 형태소분석기와 품사태거만 제공하고 있습니다. Cython으로 컴파일된 .so파일로 제공되며, CLI환경과 파이썬 환경에서 모두 사용할 수 있습니다. 파이썬 환경에서는 다른 모듈처럼 import 키워드로 불러온 후 사용하시면 됩니다 :D

This is a end-to-end dependency parser for Korean. Given a Korean sentence, the parser gives you N most likely parses for the sentence. Currently, only the morpheme analyzer & POS tagger are supported. The project is in the form of a Cython-compiled .so(dynamic linked library) files, so it is both runnable in CLI environments and Python environments. In a Python evironment, the files can be imported using the import keyword like many other Python modules. 

Sample Output: <br></br>
The below is an example output from the sentence "우리는 누가 보아도 어엿한 대학생이다. 전통에 빛나고 밝은 앞날의 전망을 가진 연세의 대학인이다." with N = 3.<br></br><br></br>
![alt text](https://github.com/PolarBear77/Korean-Constituency-Parser/blob/master/sample_output.jpg)

Each row in the output is a unit of Korean morpheme (Root + Josa), with the first pair being the tags with the highest probabilities. The preceding pairs in brackets are the next N-best tags.



### Python environment
import RunModel<br></br>
RunModel.main()
- input_file_path: path to input file, each sentence must be delimited with a line break (\n)
- output_file_path: path to save output parse
- topN: top N number of parses to output<br></br><br></br>
![alt text](https://github.com/PolarBear77/Korean-Dependency-Parser/blob/master/sample_run.jpg)


### Software Dependencies
Python Version >= 3.5
Foma https://code.google.com/archive/p/foma/

#### Python packages:
Tensorflow >= 1.8.0
Numpy >= 1.14.0
Keras
numpy <br></br>
cython <br></br>
nltk <br></br>

### Resources
Sejong corpus https://ithub.korean.go.kr/user/guide/total/guide1.do
