---
title: Modify MicrosoftDNS_MGType 類別的方法
description: Modify 方法會更新郵件群組 (MG) 資源記錄。
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_MGType 類別
- MicrosoftDNS_MGType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db26f33e56ecc8553af1e34513a085b6eb6666ca99e2f91ec19383756094d6f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874908"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a>Modify MicrosoftDNS \_ MGType 類別的方法

**Modify** 方法會更新郵件群組 (MG) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*MGMailbox* \[在中，選擇性\]
</dt> <dd>

FQDN，指定隸屬于記錄擁有者名稱所指定之郵件群組成員的信箱。

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

[**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)
</dt> <dt>

[**MicrosoftDNS MGType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





