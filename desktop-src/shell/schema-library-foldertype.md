---
description: '&lt;FolderType &gt; 元素會指定資料夾類型的 GUID。 如果 &lt; templateInfo 元素存在，則需要這個元素 &gt; ，否則它是選擇性的。 此元素沒有屬性和子項目。'
title: 'folderType 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba9d0163a00ab525fb0a52267c1226b6a48230a4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880864"
---
# <a name="foldertype-element-library-schema"></a>folderType 元素 (程式庫架構) 

&lt;FolderType &gt; 元素會指定資料夾類型的 GUID。 如果 &lt; templateInfo 元素存在，則需要這個元素 &gt; ，否則它是選擇性的。 此元素沒有屬性和子項目。

## <a name="syntax"></a>Syntax


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                           | 子元素 |
|--------------------------------------------------------------------------|----------------|
| [templateInfo 元素 (程式庫架構) ](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>備註

設定資料夾類型會決定預設會出現在 Windows 檔案總管中的資料行和詳細資料。 資料夾類型識別碼 ([**FOLDERTYPEID**](foldertypeid.md)) 是在 Shlguid 中定義的 guid。 下表列出一般資料夾類型的 Guid。



| 資料夾類型      | GUID                                   |
|------------------|----------------------------------------|
| 一般程式庫  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| 使用者程式庫  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| 檔資料夾 | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| 圖片資料夾  | {B3690E58-E961-423B-B687-386EBFD83239} |
| 影片資料夾    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| 遊戲資料夾     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| 音樂資料夾     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| 連絡人         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[iconReference 元素 (程式庫架構) ](schema-library-iconreference.md)
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

 

 



