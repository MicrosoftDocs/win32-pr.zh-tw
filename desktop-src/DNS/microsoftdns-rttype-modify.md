---
title: Modify MicrosoftDNS_RTType 類別的方法
description: Modify 方法會透過 (RT) 資源記錄來更新路由。
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_RTType 類別
- MicrosoftDNS_RTType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2003f8e2840a2684f91a7a01b0341e2e8dcdf0ca88b6bf31fcf58b3a3c6f79bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692398"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Modify MicrosoftDNS \_ RTType 類別的方法

**Modify** 方法會透過 (RT) 資源記錄來更新路由。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*喜好* \[ 設定在中，選擇性\]
</dt> <dd>

在相同擁有者的其他專案中提供給此 RR 的喜好設定。 偏好較低的值。

</dd> <dt>

*IntermediateHost* \[在中，選擇性\]
</dt> <dd>

FQDN，指定主機做為中繼，以達到擁有者指定的主機。

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

新物件的參考。

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

[**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)
</dt> <dt>

[**MicrosoftDNS RTType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





