---
title: "컬렉터"
linkTitle: "컬렉터"
weight: 4
date: 2022-06-07
description: >
    클라우드포레는 **컬렉터**를 통해 **클라우드 리소스**(링크. 클라우드 리소스 용어 정리 필요할듯.)들을 수집하며, 스케줄링을 통해 수집 시기를 결정할 수 있습니다.

---

## 개요

컬렉터로 데이터를 수집하기 위해서는 다음 두 가지 요소가 필요합니다.

### 컬렉터 플러그인

**클라우드 프로바이더**(링크. 프로바이더 링크가 필요해요!)로부터 어떤 리소스들을 수집할지, 수집한 데이터들을 어떻게 화면에 보여줄지에 대한 스펙이 정의된 요소입니다. 

프로바이더 별로 가지고 있는 데이터의 구조와 내용이 상이하므로 컬렉터는 철저히 **컬렉터 플러그인**에 의존하여 리소스들을 수집합니다.

이에 대한 자세한 설명은 [여기](/ko/docs/guides/plugins/asset-inventory-collector)를 참고하세요.
 
### 서비스 계정 

리소스를 수집하기 위해서는 **클라우드 프로바이더**(링크. 프로바이더 링크가 필요해요!)의 계정에 연결이 필요합니다.

**서비스 계정**은 프로바이더의 계정에 연결하기 위한 계정 정보입니다. 

컬렉터는 기존에 프로바이더 별로 만들어져 있는 서비스 계정을 통해 프로바이더 계정에 접근합니다. 

이에 대한 자세한 설명은 [여기](/ko/docs/guides/asset-inventory/service-account)를 참고하세요.

## 컬렉터 생성하기

(1) 왼쪽 상단의 [생성] 버튼을 클릭합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fb9a981d-9080-492d-804c-f06460a7bbbc/Untitled.png)

(2) 플러그인 목록 페이지에서 원하는 컬렉터 플러그인을 찾아 [생성] 버튼을 클릭합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4c037051-62c5-4e3b-ab05-7eff088f95cc/Untitled.png)

(3) [컬렉터 생성] 페이지에서 컬렉터 생성 과정을 거칩니다.

(3-1) [컬렉터 설정] 탭에서 이름과 플러그인의 버전을 선택합니다.

이름은 필수로 입력하여야 합니다.

버전은 앞에서 선택한 컬렉터 플러그인의 버전을 의미하며, 자동 업그레이드를 비활성화하면 선택할 수 있습니다. 이 경우에는 항상 지정한 버전의 플러그인으로 데이터가 수집됩니다.

반면, 자동 업그레이드를 활성화하면 항상 최신 버전의 플러그인으로 데이터가 수집됩니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/830a04f9-944d-4a2a-b056-d784e47e6c97/Untitled.png)

(3-2) 필요한 경우, [태그 추가] 탭에서 컬렉터에 대한 추가 정보를 입력합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6d2d7081-1561-480c-838d-f74f3e9686db/Untitled.png)

(4) [확인] 버튼을 클릭하여 컬렉터 생성을 완료합니다.

## 컬렉터 목록 조회하기

컬렉터 페이지에서 생성되어 있는 모든 컬렉터 목록을 조회할 수 있습니다.

쿼리 검색을 통해 세밀한 조건으로 목록을 필터링할 수 있습니다. 쿼리 검색에 대한 상세 설명은 여기(링크)를 참고하세요.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/67553f0e-cc4e-40a1-b9bc-d18f2b6105ee/Untitled.png)

## 컬렉터 상세 정보 확인하기

(1) 컬렉터 목록에서 상세 내용을 확인하고 싶은 컬렉터를 선택합니다.

(스샷!)

(2) 아래 [상세 정보] 탭에서 컬렉터의 상세한 정보를 확인할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cd34b069-c6e0-44a9-b600-e4fab7d96834/Untitled.png)

## 컬렉터 편집하기

(1) 컬렉터 목록에서 편집하고자 하는 컬렉터를 선택합니다.

(2) [작업] 드롭다운에서 [편집] 메뉴를 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a617f3b0-7e13-4ddf-aade-c5ad8aa18be5/Untitled.png)

(3) [컬렉터 편집] 모달에서 값을 변경한 후 [확인] 버튼을 클릭하여 편집을 완료합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e4311369-095f-4ff5-a2d7-5b4affa6a3d1/Untitled.png)

## 컬렉터 활성화/비활성화 하기

컬렉터를 활성화하거나 비활성화할 수 있습니다. 컬렉터를 비활성화하면 스케줄러에 의한 데이터 수집이 이뤄지지 않습니다.

(1) 컬렉터 목록에서 활성화 혹은 비활성화 하려는 컬렉터를 선택합니다. 여러 개를 선택하여 일괄 적용이 가능합니다.

(2) [작업] 드롭다운에서 [활성화] 혹은 [비활성화] 항목을 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0d4c3d33-24c6-42f8-93f1-b9ebe21a1927/Untitled.png)

(3) [컬렉터 활성화] 혹은 [컬렉터 비활성화] 모달에서 선택한 항목들을 확인한 후, [확인] 버튼을 클릭하여 활성화/비활성화를 완료합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/87e27c88-3e15-470b-a309-ec46991a7ea9/Untitled.png)

## 컬렉터 삭제하기

컬렉터를 영구히 삭제할 수 있습니다.

(1) 컬렉터 목록에서 삭제하려는 컬렉터를 선택합니다. 여러 개를 선택하여 일괄 삭제가 가능합니다.

(2) [작업] 드롭다운에서 [삭제] 메뉴를 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cb76fcf7-58ea-4374-9d08-f60154eeefd8/Untitled.png)

(3) [컬렉터 삭제] 모달에서 선택한 항목들을 확인한 후, [확인] 버튼을 클릭하여 삭제를 완료합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/91743ef8-c286-4095-9b8c-92fb87a8459d/Untitled.png)

## 일회성 데이터 수집하기

스케줄링하지 않고 일회성으로 데이터를 수집할 수 있습니다.

이 기능을 사용하면 컬렉터가 비활성화 상태여도 데이터 수집이 이뤄집니다.

데이터 수집은 두 가지 방식으로 동작합니다.

- [모든 서비스 계정에 대하여 데이터 수집](/ko/docs/guides/asset-inventory/collector/#연결된-모든-서비스-계정에-대하여-데이터-수집하기)
- [하나의 서비스 계정에 대하여 데이터 수집](/ko/docs/guides/asset-inventory/collector/#하나의-서비스-계정에-대하여-데이터-수집하기)

### 연결된 모든 서비스 계정에 대하여 데이터 수집하기

컬렉터는 데이터 수집을 위해 **프로바이더**(링크. 프로바이더 링크가 필요해요!)의 계정 정보를 필요로 하며, 이는 [**서비스 계정**](/ko/docs/guides/asset-inventory/service-account)을 통해 등록됩니다.

기본적으로 컬렉터는 클라우드 프로바이더에 대한 모든 서비스 계정으로 데이터를 수집합니다.

(1) 컬렉터 목록에서 데이터를 수집할 컬렉터를 선택합니다.

(2) [작업] 드롭다운에서 [데이터 수집] 메뉴를 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fcc087ad-8fa2-4f8f-b7ef-4aa088fc6244/Untitled.png)

(3) [데이터 수집] 모달에서 [확인] 버튼을 클릭하여 데이터 수집을 시작합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d1710f42-c867-41b3-b517-f76baa30f974/Untitled.png)

(4) 해당 컬렉터가 데이터 수집을 완료했는지 여부는 컬렉터 히스토리(링크)에서 확인 가능합니다. 선택한 컬렉터의 [상세 보기] 링크를 클릭하여 해당 페이지로 이동할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dc45ace9-afb8-405e-84ad-b19518f3c077/Untitled.png)

### 하나의 서비스 계정에 대하여 데이터 수집하기

컬렉터로 데이터를 수집할 때에 특정한 클라우드 프로바이더 계정의 데이터만을 수집할 수도 있습니다.

(1) 컬렉터 목록에서 데이터를 수집할 컬렉터를 선택합니다.

(2) 아래의 [서비스 계정] 탭을 선택합니다.

여기에는 선택한 컬렉터를 통해 데이터 수집 시 사용되는 서비스 계정 목록이 표시됩니다.

{{<alert title="서비스 계정">}}
[서비스 계정](/ko/docs/guides/asset-inventory/service-account)은 데이터 수집에 필요한 프로바이더 계정에 대한 접근 정보를 가지고 있습니다.

만약 여기에서 아무런 정보를 확인할 수 없다면, 프로바이더에 접근할 수 있는 계정 정보가 없는 것이므로 컬렉터가 실행되더라도 데이터 수집이 일어나지 않습니다.

따라서 컬렉터로 데이터를 수집하려면 [서비스 계정] 메뉴에서 해당 프로바이더의 계정 정보를 먼저 등록해두어야 합니다.

{{</alert>}}

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f6c0d0ea-e39b-424f-a0a2-f2d04e414485/Untitled.png)

(3) 데이터를 수집하고자 하는 서비스 계정의 오른쪽 [데이터 수집] 버튼을 클릭합니다.

(4) [데이터 수집] 모달에서 [확인] 버튼을 클릭하여 데이터 수집을 시작합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f9020813-3bcb-4ea6-8a07-5472fafac819/Untitled.png)

## 데이터 수집 스케줄 설정하기

주기적으로 리소스들을 수집해오도록 컬렉터에 스케줄링을 할 수 있습니다.

(1) 컬렉터 목록에서 스케줄을 설정할 컬렉터를 선택합니다.

(2) 아래의 [스케줄] 탭을 선택합니다.

여기에서 스케줄 목록을 확인하거나 추가/변경/삭제할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1c713307-a411-457d-980e-03b46631940b/Untitled.png)

### 스케줄 추가하기

(1) [추가] 버튼을 클릭합니다.

(2) [스케줄 추가] 모달에서 값을 입력합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f7625de0-d1ad-452f-84c2-f38565fadafd/Untitled.png)

(2-1) 식별 가능한 이름과 설정한 스케줄이 동작할 시간대(타임존)를 선택합니다.

(2-2) 컬렉터가 데이터를 수집할 스케줄을 설정합니다. 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9000c263-1248-4e67-a2f9-24287877cbaa/Untitled.png)
<br>
<br>

스케줄을 설정할 때에는 두 가지 방식이 있습니다.

- 시간으로 설정: 반복을 원하는 시간을 입력하면, 입력한 모든 시간마다 데이터를 수집합니다. 이를 매일 반복합니다.
- 반복 주기로 설정: 입력한 시간 주기로 데이터를 수집합니다. 플러그인에서 지원하는 시간 단위(시, 분, 초)에 따라 입력 양식도 달라집니다.

{{<alert title="반복 주기 설정이 보이지 않는 경우">}}
선택한 컬렉터의 **플러그인**이 무엇인지에 따라 반복 주기 설정 양식이 때로는 보이지 않거나, 그 시간 단위(시, 분, 초) 입력 양식이 다를 수 있습니다.

컬렉터의 데이터 수집은 철저히 컬렉터 플러그인에 의존합니다. 그런데 만약 해당 플러그인이 수집하는 데이터의 양이 방대하다면, 반복 주기 설정은 매우 위험할 수 있습니다. 이런 문제를 방지하기 위해 반복 주기 설정은 기본 값으로 제공되지 않습니다.

반면, 오히려 자주 데이터를 수집해야 하는 플러그인도 있습니다. 이 경우에는 플러그인이 지원하는 조건에 따라 반복 주기 설정 양식이 화면에 표시됩니다.

플러그인에 대한 자세한 설명은 [여기](/ko/docs/guides/plugins/asset-inventory-collector)를 참고하세요.

{{</alert>}}

(3) [확인] 버튼을 클릭하여 컬렉터를 생성합니다.

### 스케줄 변경하기

(1) 스케줄 목록에서 변경할 항목을 선택합니다.

(2) [작업] 드롭다운에서 [변경]을 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2e9daf3f-d688-4544-a738-5001ad0fc9dd/Untitled.png)

(2-1) [스케줄 변경] 모달에서 변경할 내용을 입력합니다. 스케줄 추가 양식과 동일하므로, 위의 스케줄 추가하기(링크)를 참고하세요.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/925575a5-40ad-4c9d-b486-955342769ea1/Untitled.png)

(3) [확인] 버튼을 클릭하여 변경을 완료합니다.

### 스케줄 삭제하기

(1) 스케줄 목록에서 변경할 항목을 선택합니다.

(2) [작업] 드롭다운에서 [삭제] 메뉴를 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a7801fd3-5412-42e5-b0fa-72f09b95f8b1/Untitled.png)

(3) [스케줄 삭제] 모달에서 삭제할 스케줄의 내용을 확인하고, [확인] 버튼을 클릭하여 삭제를 완료합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/12893694-4172-4bc1-bcd9-3a97a580374c/Untitled.png)

## 데이터 수집 내역 확인하기

**컬렉터 히스토리** 페이지에서 데이터 수집 내역을 확인할 수 있습니다.

컬렉터 페이지 상단의 [컬렉터 히스토리] 버튼을 클릭하여 컬렉터 히스토리 페이지로 이동할 수 있습니다.

특정 컬렉터의 데이터 수집 내역만을 확인하고 싶다면, 컬렉터 목록의 [상세 보기] 버튼을 클릭하여 이동할 수도 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/90929aa9-7942-4b37-9bee-222ece88711c/Untitled.png)

### 데이터 수집 목록 조회하기

컬렉터 히스토레 페이지 상단의 차트를 통해, 날짜별 데이터 수집 현황을 빠르게 확인할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2e2c2095-148a-49c2-865e-99719eae29ed/Untitled.png)

하단의 목록에서는 쿼리 검색과 상태 필터 조건에 맞는 데이터 수집 목록이 표시됩니다. 쿼리 검색에 대한 자세한 설명은 여기(링크)를 참고하세요.

데이터 수집이 진행중인 항목의 경우, Job Progress 필드의 상태바를 통해 수집 현황을 확인할 수 있습니다.

### 데이터 수집 내역 상세 정보 확인하기

데이터 수집 내역에 대하여 더욱 자세한 정보를 확인하려면, 목록에서 확인하려는 항목을 선택하여 수집 내역 상세 페이지로 이동합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/37a97d10-fd59-4510-b585-1e76c620ce1a/Untitled.png)

데이터 수집 상태와 기본 정보, 그리고 **서비스 계정 별 상세 수집 목록**을 확인할 수 있습니다.

#### 서비스 계정 별 상세 수집 목록 확인하기

컬렉터를 실행하면, 연결된 서비스 계정 별로 수집이 이뤄집니다.

각 계정 별로 수집 작업이 어떻게 이뤄졌는지에 대한 정보를 목록을 통해 확인 가능합니다.

{{<alert title="">}}
컬렉터는 데이터 수집 시 서비스 계정을 통해 클라우드 프로바이더의 계정에 접근하여 데이터를 가져옵니다.
{{</alert>}}

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56a99b55-16cd-4eef-9940-d441da40a9cc/Untitled.png)

- Created Count: 새롭게 추가된 리소스의 개수
- Updated Count: 가져온 리소스의 개수
- Disconnected Count: 가져오지 못한 리소스의 개수
- Deleted Count: 삭제된 리소스의 개수 (여러 번 가져오지 못하면 삭제된 것으로 간주됩니다.)

#### 데이터 수집 에러 내용 확인하기

(1) 계정 별 상세 수집 목록에서 에러 내용을 확인하고자 하는 항목을 선택합니다.

(2) 아래의 [에러 목록] 탭에서 오류에 대한 자세한 내역을 확인할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cc2c2029-bf36-413c-a9d2-9e33f250c4bd/Untitled.png)

## 컬렉터 태그 관리하기

컬렉터에 태그를 추가하여 관리할 수 있습니다.

(1) [태그] 탭을 선택합니다.

(2) [편집] 버튼을 클릭합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d3c58e2b-f08c-468a-b758-f89b844b4669/Untitled.png)

(2-1) [태그] 페이지에서 [태그 추가] 버튼을 클릭합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bc422be2-b162-4528-b2a1-8e1e84aca3a2/Untitled.png)

(2-2) 추가하고자 하는 값을 `키: 값` 형태로 입력합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a474e2eb-0f29-46c7-94db-b6abd07077b3/Untitled.png)

(2-3) 태그를 더 추가하고자 한다면, 원하는 개수만큼 [태그 추가] 버튼을 클릭합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/86e6ac95-2234-4664-a494-ddcdd3484f42/Untitled.png)

2-4) 추가한 태그 입력 창을 삭제하고자 한다면, 값 입력 창 오른쪽의 [삭제] 버튼을 클릭하여 삭제합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/22196a6f-78f8-4339-b6bd-fc8cd9f66851/Untitled.png)

(2-5) [저장] 버튼을 클릭하여 태그 추가를 완료한 후, [태그] 탭에서 확인합니다.