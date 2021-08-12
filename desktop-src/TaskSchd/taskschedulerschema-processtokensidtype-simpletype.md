---
title: processTokenSidType 簡單類型
description: 定義 ProcessTokenSidType (principalType) 元素的可能值。
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- processTokenSidType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 505f8abe340af36c25792ec97a5a465a166eedb74921c800d2a568d10a5cce0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611900"
---
# <a name="processtokensidtype-simple-type"></a>processTokenSidType 簡單類型

定義 [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) 元素的可能值。

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**ProcessTokenSidType** 簡單類型會定義下列值。



| 值        | 描述                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 無         | 工作會在不包含處理常式權杖 SID 的進程中執行， (進程權杖群組清單) 不會進行任何變更。<br/> |
| 不受限制 | 工作 SID 將衍生自完整的工作路徑，並新增至 [處理權杖群組] 清單。<br/>                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





