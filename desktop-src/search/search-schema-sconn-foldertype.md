---
description: <folderType>元素指定資料夾類型的 GUID。 如果元素存在，則需要這個元素 <templateInfo> 。 它沒有屬性和子項目。
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: 'folderType 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6b9d5682a85126a467c051b9f1103a4ac10f2f6936cc24dd4438a5f8c75d44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862597"
---
# <a name="foldertype-element-search-connector-schema"></a>folderType 元素 (搜尋連接器架構) 

<folderType>元素指定資料夾類型的 GUID。 如果元素存在，則需要這個元素 <templateInfo> 。 它沒有屬性和子項目。

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



| Parent 項目                                                                         | 子元素 |
|----------------------------------------------------------------------------------------|----------------|
| [templateInfo 元素 (搜尋連接器架構) ](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>備註

預設 GUID 是 {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}，這是同盟搜尋 (OpenSearch) 連接器的一般資料夾類型。

## <a name="example-of-a-foldertype-element"></a>FolderType 元素範例


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



