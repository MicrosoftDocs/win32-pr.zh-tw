---
title: Modify MicrosoftDNS_SOAType 類別的方法
description: Modify 方法會更新 (SOA) 資源記錄的授權啟動。
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_SOAType 類別
- MicrosoftDNS_SOAType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74785804ebed8266443f0dd708a5d122e350a6cf88b91f228d2ce266481dffaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825078"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Modify MicrosoftDNS \_ SOAType 類別的方法

**Modify** 方法會更新 (SOA) 資源記錄的授權啟動。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*SerialNumber* \[在中，選擇性\]
</dt> <dd>

SOA 序號，代表區域已更新的次數， [*次要伺服器*](s-gly.md) 會使用這些序號來判斷是否需要進列區域轉送。

</dd> <dt>

*>Primaryserver* \[在中，選擇性\]
</dt> <dd>

主伺服器的名稱。

</dd> <dt>

*ResponsibleParty* \[在中，選擇性\]
</dt> <dd>

負責任之合作物件的信箱位址（以別名的形式），例如 xyz.microsoft.com。 請注意，使用句點而不是 at 符號 ( @ ) 。

</dd> <dt>

*RefreshInterval* \[在中，選擇性\]
</dt> <dd>

應重新整理包含此記錄之區域之前的時間（以秒為單位）。

</dd> <dt>

*RetryDelay* \[在中，選擇性\]
</dt> <dd>

DNS 伺服器應該在名稱解析嘗試之間延遲的時間（以秒為單位）。

</dd> <dt>

*ExpireLimit* \[在中，選擇性\]
</dt> <dd>

次要伺服器在將其區域檔案的複本捨棄為無效之前，應該等候主伺服器回應的時間（以秒為單位）。

</dd> <dt>

*MinimumTTL* \[在中，選擇性\]
</dt> <dd>

TTL 時間（以秒為單位），套用至區域中未指定其專屬 TTL 的資源記錄。

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

修改過之物件的參考

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

[**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





