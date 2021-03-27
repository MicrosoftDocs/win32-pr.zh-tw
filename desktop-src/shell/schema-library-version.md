---
description: <version>元素指定此程式庫的內容版本。 此元素沒有屬性和子項目。
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: 'version 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972296"
---
# <a name="version-element-library-schema"></a>version 元素 (程式庫架構) 

<version>元素指定此程式庫的內容版本。 此元素沒有屬性和子項目。

## <a name="syntax"></a>Syntax

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>項目資訊



| Parent 項目                                                               | 子元素 |
|------------------------------------------------------------------------------|----------------|
| [libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md) | 無           |



 

## <a name="remarks"></a>備註

程式庫的內容版本與程式庫的檔案格式不同 (library \* -ms) 版本。 程式庫的檔案格式版本是在 [命名空間](library-schema-entry.md)中指定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> <dt>

[搜尋連接器描述架構](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
