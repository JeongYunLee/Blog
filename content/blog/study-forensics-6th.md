---

title: 디지털 포렌식 4주차 스터디(1)
description: III. 디지털포렌식(비휘발성) 분석 2-1 디지털증거 무결성 분석
slug: study-forensics-6th
img: not-yet-generated.png
datetime: 2021. 11. 22.
category: 디지털 포렌식
author: 최예지

---

# 2-1 디지털증거 무결성 분석

## 무결성 분석 (해쉬값 검증)

디지털 저장매체를 처음 인계받고 우선적으로 해야 할 작업은 해쉬 값 검증 작업이다.

> **무결성의 원칙**: 수집된 증거가 위변조되지 않았음을 증명해야 한다. 보통 디지털 증거 수집시 데이터 해쉬(Hash) 값과 법정제출시점의 데이터 해쉬값이 같다면 디지털 증거의 무결성이 입증된다.
> 

### 해쉬값 검증 절차

1. **하드디스크 정보(Physical Media Information) 확인**
    
    : 하드디스크 이미지(image) 정보를 확인한다.
    
2. **해쉬(Hash) 검증**
    
    : 쓰기방지장치를 통해 디지털 증거를 연결한 후 HashCalc.exe 또는 FTK Imager 프로그램을 활용하여 무결성을 검증한다. 프로그램에 디지털증거 이미지 파일 넣어 나온 분석 해쉬 값과 수집 해쉬 값이 동일한지 확인하여 검증한다.
    

### 포렌식 분석 프로그램의 특이점

- 디지털 저장장치를 대상으로 디지털증거 파일을 생성하는 종류에는 대표적으로 RAW 이미지파일과 E01 이미지 파일이 있다.
    - **RAW 이미지 파일**: bit 단위로 복사하여 디지털 저장장치와 동일한 크기의 이미지 파일을 생성한다.
    - **E01 이미지 파일**: 파일을 압축하여 용량을 줄이고 별도의 점검내용을 같이 저장하는 파일이다.
- FTK Imager 프로그램과 같이 포렌식 분석 프로그램은 같은 이미지 파일에 대해서 RAW 형태와 E01 형태 모두 동일한 해쉬 값을 출력한다.
- 단순한 해쉬 값 출력 프로그램인 HashCalc 프로그램은 CRC 값과 압축 등으로 인해 다른 해쉬 값을 출력한다.
