---
description: '&lt;IconReference &gt; 元素會指定這個程式庫的自訂圖示。 這個元素是選擇性的，且沒有任何屬性或子項目。'
title: 'iconReference 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: db34a387200f3078da08747191242ae7414be410
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884264"
---
# <a name="iconreference-element-library-schema"></a>iconReference 元素 (程式庫架構) 

&lt;IconReference &gt; 元素會指定這個程式庫的自訂圖示。 這個元素是選擇性的，且沒有任何屬性或子項目。

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                               | 子元素 |
|------------------------------------------------------------------------------|----------------|
| [libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>備註

您必須在適合 [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) 函數的表單中指定圖示參考。 例如：`ModuleFileName,IconResourceIndex`。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[folderType 元素 (程式庫架構) ](schema-library-foldertype.md)
</dt> <dt>

[isLibraryPinned 元素 (程式庫架構) ](schema-library-islibrarypinned.md)
</dt> <dt>

[libraryDescription 元素 (程式庫架構) ](schema-librarydescription.md)
</dt> <dt>

[ (程式庫架構的 name 元素) ](schema-library-name.md)
</dt> <dt>

[ownerSID 元素 (程式庫架構) ](schema-library-ownersid.md)
</dt> <dt>

[propertyStore 元素 (程式庫架構) ](schema-library-propertystore.md)
</dt> <dt>

[searchConnectorDescription 元素 (程式庫架構) ](schema-library-searchconnectordescription.md)
</dt> <dt>

[searchConnectorDescriptionList 元素 (程式庫架構) ](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[templateInfo 元素 (程式庫架構) ](schema-library-templateinfo.md)
</dt> <dt>

[version 元素 (程式庫架構) ](schema-library-version.md)
</dt> </dl>

 

 



