mini-PJT : LLM기반 PDF Reader
===

LLM을 통한 영문 동화의 번역,요약 및 음성 생성 프로젝트입니다.

![alt text](image.png)

개요
---
영어로 된 어린이 동화책을 한국어 오디오북으로 변환하는 프로그램입니다.
주요 기능 순서는 아래와 같습니다. 

1. 사용자가 PDF 업로드 
2. PDF 텍스트 추출
3. 인공지능 모델(gpt-4o-mini) 기반하여 핵심 내용 파악 및 요약
- Prompt engineering(등장인물, 줄거리, 주제, 교훈)
4. 요약된 내용을 한국어로 번역 기능
5. 오디오 버전 다운로드 가능

이 프로그램은 영문 어린이 동화책을 한국어 사용자들이 교육 및 학습 목적으로 활용할 수 있습니다. 

사용 라이브러리
---
requirement.txt 참고

```
from datetime import datetime
import streamlit as st
from openai import OpenAI # Model : gpt-4o-mini
from PyPDF2 import PdfReader
from pathlib import Path
```

