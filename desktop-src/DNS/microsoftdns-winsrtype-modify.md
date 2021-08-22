---
title: Modify MicrosoftDNS_WINSRType 類別的方法
description: Modify 方法會將 WINS 反向查閱 (WINSR) 資源記錄。
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_WINSRType 類別
- MicrosoftDNS_WINSRType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db7865110b0e79642dc91671094c06dfbd10e07cd89684dab58623a9456cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076662"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Modify MicrosoftDNS \_ WINSRType 類別的方法

**Modify** 方法會將 WINS 反向查閱 (WINSR) 資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*MappingFlag* \[在中，選擇性\]
</dt> <dd>

WINSR 對應旗標，指定是否必須將記錄包含在區域複寫中。 它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。

</dd> <dt>

*LookupTimeout* \[在中，選擇性\]
</dt> <dd>

使用 WINS 反向查閱之 DNS 伺服器的超時時間（以秒為單位）。

</dd> <dt>

*CacheTimeout* \[在中，選擇性\]
</dt> <dd>

使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。

</dd> <dt>

*ResultDomain* \[在中，選擇性\]
</dt> <dd>

要附加至所傳回 NetBIOS 名稱的功能變數名稱。

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

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**MicrosoftDNS WINSRType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





