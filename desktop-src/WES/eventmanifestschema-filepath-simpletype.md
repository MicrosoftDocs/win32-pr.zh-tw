---
title: filePath 簡單類型
description: 定義包含檔案完整路徑的字串。
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- filePath simple type EventLog
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3929db5643ef7a68f2cd33f1d194c80b4dbc1e99e2f667b7c6e43dde8652dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343994"
---
# <a name="filepath-simple-type"></a>filePath 簡單類型

定義包含檔案完整路徑的字串。 路徑可以包含環境變數。

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





