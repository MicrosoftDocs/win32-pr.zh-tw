---
title: Modify MicrosoftDNS_AAAAType 類別的方法
description: Modify 方法會 (AAAA) 資源記錄來更新 IPv6 位址。
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_AAAAType 類別
- MicrosoftDNS_AAAAType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417275b9e5fdf1c499f34fd49af3c40f8e208d43673a5d53dc9ba4c3b1ef2c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967399"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a>Modify MicrosoftDNS \_ AAAAType 類別的方法

**Modify** 方法會 (AAAA) 資源記錄來更新 IPv6 位址。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*IPv6Address* \[在中，選擇性\]
</dt> <dd>

主機的 IPv6 位址。

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

[**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)
</dt> <dt>

[**MicrosoftDNS AAAAType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





