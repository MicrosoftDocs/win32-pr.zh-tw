---
description: '&lt;TemplateInfo &gt; 元素是 folderType 專案的容器，可指定用來顯示此程式庫查詢結果的資料夾類型。 這個元素是選擇性的，且沒有任何屬性。'
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: 'templateInfo 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f55fec64bf7418eef8e70c4cf8fa1ee47006c5f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885524"
---
# <a name="templateinfo-element-library-schema"></a>templateInfo 元素 (程式庫架構) 

&lt;TemplateInfo &gt; 元素是[folderType](schema-library-foldertype.md)專案的容器，可指定用來顯示此程式庫查詢結果的資料夾類型。 這個元素是選擇性的，且沒有任何屬性。

## <a name="syntax"></a>Syntax

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>項目資訊



| Parent 項目                                                               | 子元素                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md) | [folderType 元素 (程式庫架構) ](schema-library-foldertype.md)       |
|                                                                              | [propertyStore 元素 (程式庫架構) ](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> <dt>

[搜尋連接器描述架構](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
