---
description: <name>元素指定此程式庫的名稱。 此為必要專案，而且沒有任何屬性或子項目。
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: " (程式庫架構的 name 元素) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 179d8b4a1f4358ccb441cc38c6c0765a6dc4d9ade8b3c32a1504be2151cfedaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883938"
---
# <a name="name-element-library-schema"></a> (程式庫架構的 name 元素) 

<name>元素指定此程式庫的名稱。 此為必要專案，而且沒有任何屬性或子項目。

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

名稱是顯示在 Windows 檔案總管中的易記程式庫名稱。 您可以使用格式來指定名稱 <dllname> ， <index> 如下列範例所示。


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

 

 
