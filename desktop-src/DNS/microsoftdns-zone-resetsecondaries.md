---
title: MicrosoftDNS_Zone 類別的 ResetSecondaries 方法
description: ResetSecondaries 方法會重設區域中次要 DNS 伺服器的 IP 位址。
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- ResetSecondaries 方法 DNS
- ResetSecondaries 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，ResetSecondaries 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934695"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_

**ResetSecondaries** 方法會重設區域中次要 DNS 伺服器的 IP 位址。

## <a name="syntax"></a>語法


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SecondaryServers* \[在\]
</dt> <dd>

次要 DNS 伺服器的 IP 位址陣列。

</dd> <dt>

*SecureSecondaries* \[在\]
</dt> <dd>

指定要套用的安全性，而且必須是下列其中一項：

-   區域 \_ SECSECURE \_ 無 \_ 安全性
-   \_ \_ 僅限區域 SECSECURE NS \_
-   \_ \_ 僅限區域 SECSECURE 清單 \_
-   區域 \_ SECSECURE \_ 沒有 \_ XFR

</dd> <dt>

*NotifyServers* \[在\]
</dt> <dd>

當區域變更時要通知的 DNS 伺服器 IP 位址。

</dd> <dt>

*通知* \[在\]
</dt> <dd>

通知設定，必須是下列其中一項：

-   區域 \_ 通知 \_ 關閉
-   區域 \_ 通知 \_ 所有 \_ 次要資料庫
-   \_ \_ 僅限區域通知清單 \_

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

[**MicrosoftDNS \_ 區域**](microsoftdns-zone.md)類型的 RR。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS \_ 區域**](microsoftdns-zone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 CreateZone 方法 \_**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 PauseZone 方法 \_**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





