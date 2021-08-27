---
description: '&lt;Name &gt; 元素會指定這個程式庫的名稱。 此為必要專案，而且沒有任何屬性或子項目。'
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: " (程式庫架構的 name 元素) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880854"
---
# <a name="name-element-library-schema"></a> (程式庫架構的 name 元素) 

&lt;Name &gt; 元素會指定這個程式庫的名稱。 此為必要專案，而且沒有任何屬性或子項目。

## <a name="syntax"></a>Syntax

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>項目資訊



| Parent 項目                                                               | 子元素 |
|------------------------------------------------------------------------------|----------------|
| [libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>備註

名稱是顯示在 Windows 檔案總管中的易記程式庫名稱。 您可以使用 &lt; dllname &gt; （ &lt; 索引格式）指定名稱， &gt; 如下列範例所示。


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md)
</dt> <dt>

[搜尋連接器描述架構](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
