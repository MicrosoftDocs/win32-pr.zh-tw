---
description: 定義型別，該型別定義 Content 專案日誌讀取器之 Type 屬性的有效值 \[ \] 。
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: ContentTypeType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026902"
---
# <a name="contenttypetype-simple-type"></a>ContentTypeType 簡單類型

定義型別，該型別定義 [Content 專案 \[ 日誌讀取 \] 器](content-element--journal-reader.md)之 *type* 屬性的有效值。

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**ContentTypeType** 簡單類型是以下列模式限制的字串：

-   `Normal|Inert`

## <a name="remarks"></a>備註

有效的值為 "Normal" 和 "惰性"。

如果類型是 "惰性"，則包含的內容會是記錄頁面，它是檔的唯讀/不可編輯的「背景」。 使用筆記本便箋寫入器印表機驅動程式建立檔時，就會發生這種情況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



 

 




