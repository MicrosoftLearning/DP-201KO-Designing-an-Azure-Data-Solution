---
lab:
    title: 'Azure 실시간 참조 아키텍처'
    module: '모듈 3: Azure 실시간 참조 아키텍처'
---

# DP 201 - Azure 데이터 플랫폼 솔루션 설계
# 랩 3 - Azure 실시간 참조 아키텍처

**예상 소요 시간**: 60분

**필수 구성 요소**: 이 랩 관련 사례 연구의 내용을 확인했다고 가정합니다.

**랩 파일**: 이 랩용 파일은 _Allfiles\Labfiles\Starter\DP-201.3_ 폴더에 있습니다.

## 랩 개요

이 랩에서는 사례 연구를 활용하여 실시간 처리 측면에서 람다 아키텍처와 관련이 있는 업무/기술적 요구 사항을 파악합니다. 그런 다음 Azure Stream Analytics 및 Azure Databricks를 사용하여 스트리밍 파이프라인을 설계합니다. 그리고 마지막으로 AdventureWorks의 비즈니스 요구 사항을 충족하는 데 필요한 IoT 아키텍처를 설계해 봅니다.

## 랩 목표
  
이 랩을 완료하면 다음 작업을 수행할 수 있습니다.

1. Azure Stream Analytics를 통해 스트림 처리 파이프라인 설계 수행
1. Azure Databricks를 통해 스트림 처리 파이프라인 설계 수행
1. Azure IoT 참조 아키텍처 작성

## 시나리오
  
여러분은 AdventureWorks의 선임 데이터 엔지니어이며, 실시간 데이터 처리를 수행하는 솔루션 설계를 담당하고 있습니다. 업무상의 모든 요구 사항을 전체적으로 파악할 수 있는 솔루션 아키텍처 관련 제안서를 Word 문서로 제공해야 합니다.

먼저 람다 아키텍처의 실시간 처리에 적용되는 AdventureWorks 요구 사항을 파악합니다. 그런 다음 Azure Stream Analytics 및 Azure Databricks를 사용하여 스트림 처리 파이프라인용 아키텍처를 제공합니다. 그리고 IoT 아키텍처의 첫 번째 단계도 설계합니다.

이 랩을 마치면 다음 작업을 수행하는 방법을 배울 수 있습니다.

1. Azure Stream Analytics를 통해 스트림 처리 파이프라인 설계 수행
1. Azure Databricks를 통해 스트림 처리 파이프라인 설계 수행
1. Azure IoT 참조 아키텍처 작성

>**참고**: 이 랩은 두 부분으로 구성되어 있습니다. 이 부분(1부)에서는 그룹별로 작업을 하면서 강사의 질문에 대답합니다. 각 연습을 진행할 시간은 그룹별로 결정하면 됩니다. 전체 랩을 60분 내에 완료하면 됩니다. 2부에서는 강사가 랩에서 확인된 사항을 그룹과 함께 논의합니다.

>**리소스**: 이 랩용 과정 사례 연구를 사용할 수도 있고 [Microsoft 설명서](https://docs.microsoft.com), [Azure 참조 아키텍처 사이트](https://docs.microsoft.com/ko-kr/azure/architecture/reference-architectures/), [Microsoft 고객 사례 사이트](https://customers.microsoft.com/) 등에서 이 랩의 질문에 대답을 하는 데 도움이 되는 정보를 파악할 수도 있습니다.

## 연습 1: Azure Stream Analytics를 통해 스트림 처리 파이프라인 설계 수행

**그룹 연습**
  
이 연습의 주요 태스크는 다음과 같습니다.

1. 사례 연구를 통해 AdventureWorks의 실시간 데이터 처리에 적용되는 요구 사항 파악

1. Azure Stream Analytics를 사용하여 스트림 처리 파이프라인을 반영하는 대략적인 아키텍처 빌드

### 태스크 1: AdventureWorks의 실시간 처리 요구 사항 목록 작성

1. 컴퓨터에서 **Microsoft Word**를 시작하고 **Allfiles\Labfiles\Starter\DP-201.3** 폴더에서 **DP-201-Lab03_Ex01_Ta01.docx** 파일을 엽니다.

1. 그룹 단위로 **15분** 동안 AdventureWorks의 실시간 솔루션에 적용할 요구 사항을 논의한 다음 목록을 작성합니다. 사례 연구에서 해당 증거를 제시해야 합니다.

> **결과**: AdventureWorks의 실시간 처리 요구 사항 표가 포함된 Microsoft Word 문서를 작성하여 이 연습을 완료해야 합니다.

### 태스크 2: Azure Stream Analytics를 사용하여 스트림 처리 파이프라인을 반영하는 대략적인 아키텍처 빌드

1. 컴퓨터에서 **Microsoft Word**를 시작하고 **Allfiles\Labfiles\Starter\DP-201.3** 폴더에서 **DP-201-Lab03_Ex01_Ta02.docx** 파일을 엽니다.

1. 그룹 단위로 **20분** 동안 AdventureWorks의 엔터프라이즈 BI 솔루션에 적용할 아키텍처를 논의한 다음 다이어그램을 작성합니다. icon 폴더의 png 파일을 사용하여 아키텍처를 빌드할 수 있습니다.

> **결과**: AdventureWorks의 엔터프라이즈 BI 솔루션에 적용할 아키텍처를 작성하여 이 연습을 완료해야 합니다.

## 연습 2: Azure Databricks를 통해 스트림 처리 파이프라인 설계 수행

**그룹 연습**
  
이 연습의 주요 태스크는 다음과 같습니다.

1. AdventureWorks에서 Azure Databricks 솔루션을 사용하여 스트림 처리 파이프라인을 포함하도록 대략적인 아키텍처 작성

### 태스크 1: AdventureWorks에서 Azure Databricks 솔루션을 사용하여 스트림 처리 파이프라인을 포함하도록 대략적인 아키텍처 작성

1. 컴퓨터에서 **Microsoft Word**를 시작하고 **Allfiles\Labfiles\Starter\DP-201.3** 폴더에서 **DP-201-Lab03_Ex02_Ta01.docx** 파일을 엽니다. 문서를 읽고 예제를 검토합니다.

1. 그룹 단위로 **15분** 동안 자전거 예측 유지 관리 요구 사항을 충족하는 아키텍처를 작성합니다.

> **결과**: AdventureWorks에서 Azure Databricks 솔루션을 사용해 스트림 처리 파이프라인을 작성하여 이 연습을 완료해야 합니다.

## 연습 3: Azure IoT 참조 아키텍처 작성

**그룹 연습**
  
이 연습의 주요 태스크는 다음과 같습니다.

1. 생성된 아키텍처가 Azure IoT 참조 아키텍처에 포함되는지 확인

### 태스크 1: Azure IoT 참조 아키텍처 작성

1. 그룹 단위로 **5분** 동안 Azure IoT 참조 아키텍처에 적용하기 위해 지금까지 작성한 아키텍처를 논의하고 확인합니다.

> **결과**: Azure에서 엔터프라이즈급 대화형 봇을 포함하는 아키텍처를 작성하여 이 연습을 완료해야 합니다.

## 랩 복습

60분 정도가 지나면 강사가 이 랩을 종료합니다. 그러면 전체 수강생들이 각 그룹에서 확인한 사항을 발표합니다.