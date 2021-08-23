---
title: Modify MicrosoftDNS_MINFOType 類別的方法
description: Modify 方法會更新郵件資訊 (MINFO) 資源記錄。
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MINFOType 類別
- MicrosoftDNS_MINFOType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954015ffdb01a8655a7762d3c364abe3440a8cfd19ec7eabf5ad8db5cf11c8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692558"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Modify MicrosoftDNS \_ MINFOType 類別的方法

**Modify** 方法會更新郵件資訊 (MINFO) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*ResponsibleMailbox* \[在中，選擇性\]
</dt> <dd>

FQDN，指定負責記錄的擁有者名稱中所指定之郵寄清單或信箱的信箱。

</dd> <dt>

*ErrorMailbox* \[在中，選擇性\]
</dt> <dd>

FQDN，指定信箱以接收與郵寄清單相關的錯誤訊息，或 MINFO 記錄的擁有者名稱所指定的信箱。

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

修改過之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

任何未指定的參數在修改過的記錄中都會保持不變。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**MicrosoftDNS MINFOType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





