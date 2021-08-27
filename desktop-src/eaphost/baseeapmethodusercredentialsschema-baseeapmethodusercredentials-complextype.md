---
title: BaseEapMethodUserCredentials 複雜類型
description: 瞭解 BaseEapMethodUserCredentials 複雜類型。 此類型是方法認證資料的預留位置元素。
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8102f095ca7d4b1ada6db3c21fbe55e73a98ed6d06d2d6b99032f1a21a344527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094418"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>BaseEapMethodUserCredentials 複雜類型

**BaseEapMethodUserCredentials** 複雜型別是方法認證資料的預留位置元素。

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>備註

EAP 方法會執行 **BaseEapMethodUserCredentials** 內容的架構驗證。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[baseeapmethodusercredentials 架構](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





