---
title: Modify MicrosoftDNS_RPType 類別的方法
description: Modify 方法會將負責任的人員 (RP) 資源記錄來更新。
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_RPType 類別
- MicrosoftDNS_RPType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d237879b883e21c3c6289542e4eae7b9703be64931af788f042b6cdbec2ca49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587488"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Modify MicrosoftDNS \_ RPType 類別的方法

**Modify** 方法會將負責任的人員 (RP) 資源記錄來更新。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*RPMailbox* \[在中，選擇性\]
</dt> <dd>

指定負責任人員信箱的 FQDN。

</dd> <dt>

*TXTDomainName* \[在中，選擇性\]
</dt> <dd>

存在 TXT 資源記錄的 FQDN。

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

[**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)
</dt> <dt>

[**MicrosoftDNS RPType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





