---
description: 專案 <templateInfo> 是 folderType 專案的容器，可指定資料夾類型，以顯示透過此程式庫查詢的結果。 這個元素是選擇性的，且沒有任何屬性。
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: 'templateInfo 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512197"
---
# <a name="templateinfo-element-library-schema"></a>templateInfo 元素 (程式庫架構) 

專案 <templateInfo> 是 [folderType](schema-library-foldertype.md) 專案的容器，可指定資料夾類型，以顯示透過此程式庫查詢的結果。 這個元素是選擇性的，且沒有任何屬性。

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

 

 
