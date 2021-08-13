---
description: 包含筆記本便箋中個別頁面的詳細資料。
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: JournalPage 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5062838476e6f67605101157640a490645e454b62d852b69f51dc4bb2215db99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442798"
---
# <a name="journalpage-element"></a>JournalPage 元素

包含筆記本便箋中個別頁面的詳細資料。

## <a name="definition"></a>定義

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>父項目

[**JournalDocument**](journaldocument-element.md)

## <a name="child-elements"></a>子元素

[**靜止**](stationery-element.md)

[**DocImage**](docimage-element.md)

[**TitleInfo**](titleinfo-element.md)

[**內容**](content-element--journal-reader.md)

## <a name="attributes"></a>屬性



| 屬性      | 類型                      | 必要 | 描述                                                                        | 可能的值                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | 必要 | 在日誌檔中，從一個 (1) 開始的頁面序數。 | 任何非負整數。                                |
| **寬度**      | **xs:nonNegativeInteger** | 必要 | 頁面的寬度。                                                             | 任何非負整數。                                |
| **高度**     | **xs:nonNegativeInteger** | 必要 | 頁面的高度。                                                            | 任何非負整數。                                |
| **LineHeight** | **xs:nonNegativeInteger** | 選擇性 | 頁面上所使用之線條的高度。                                           | 任何非負整數。                                |
| **LanguageId** | **xs:nonNegativeInteger** | 選擇性 | 用於頁面的語言識別項。                                                 | 代表有效語言識別項的非負整數。 |



 

## <a name="element-information"></a>項目資訊



|  元素     | 值                                                     |
|--------------|---------------------------------------------------------------------|
| 項目類型 | [**JournalPageType**](journalpagetype-complex-type.md) complexType |
| 命名空間    | urn：架構-microsoft-com：平板電腦： richink                          |
| 結構描述名稱  | 日誌讀者                                                      |



 

 

 



