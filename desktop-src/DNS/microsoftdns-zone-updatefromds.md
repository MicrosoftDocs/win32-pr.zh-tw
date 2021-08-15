---
title: MicrosoftDNS_Zone 類別的 UpdateFromDS 方法
description: UpdateFromDS 方法會強制將區域從目錄服務更新 (DS) 。
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- UpdateFromDS 方法 DNS
- UpdateFromDS 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，UpdateFromDS 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca537c6440ae14d0e15dea28f62bdb919f3ed7e3348f3a64a2339e0668b5c8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957187"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_

**UpdateFromDS** 方法會強制將區域從目錄服務更新 (DS) 。

## <a name="syntax"></a>語法


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

為了順利執行此方法，ZoneType 必須為零，而且必須將區域儲存在 DS 上。

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

[**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





