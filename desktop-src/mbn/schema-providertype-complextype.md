---
description: 指定行動電話網路的相關資訊。
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: " (行動寬頻) 的 providerType 複雜類型"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972648"
---
# <a name="providertype-complex-type"></a>providerType 複雜類型

**ProviderType** 複雜類型會指定行動電話通訊網路的相關資訊。

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                          | 類型                                                           | Description               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [**ProviderID**](schema-providerid-providertype-element.md)     | [**providerIdType**](schema-provideridtype-simpletype.md)     | 提供者識別碼。<br/>   |
| [**ProviderName**](schema-providername-providertype-element.md) | [**providerNameType**](schema-providernametype-simpletype.md) | 提供者名稱。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



 

 




