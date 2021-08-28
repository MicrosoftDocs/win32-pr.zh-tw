---
title: MicrosoftDNS_Zone 類別的 AgeAllRecords 方法
description: AgeAllRecords 方法可讓區域中的部分或所有非 NS 和非 SOA 記錄過時。
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- AgeAllRecords 方法 DNS
- AgeAllRecords 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，AgeAllRecords 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed441bcc14ff3bbd32ac4fd46f3aa86f931f9c6887c1a3c1fc48abe89e778440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344008"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a>MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_

**AgeAllRecords** 方法可讓區域中的部分或所有非 NS 和非 SOA 記錄過時。

## <a name="syntax"></a>語法


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NodeName* \[在中，選擇性\]
</dt> <dd>

要存在之節點的名稱。

</dd> <dt>

*ApplyToSubtree* \[在中，選擇性\]
</dt> <dd>

指定是否要將過時套用至子樹中的所有記錄。 設定為 TRUE 會將過時套用至子樹中的所有記錄（以 NodeName 開頭）。

</dd> </dl>

## <a name="return-value"></a>傳回值

錯誤 \_ 成功表示已順利完成過時。 任何其他值都是錯誤碼。

## <a name="remarks"></a>備註

如果未指定 *NodeName* ，所有記錄都會受到過時和清除的規定。

如果指定了 *NodeName* ，且 *ApplyToSubtree* 未指定或設定為零，則指定節點上的記錄會被視為過時和清除。

如果指定了 *NodeName* ，且 *ApplyToSubtree* 設定為1，則從 *nodename* 開始的子樹狀結構的所有記錄都會被視為過時和清除。 時間戳記會設定為所有非 NS 和非 SOA Rr 的目前時間，其擁有者名稱 (s) 由輸入參數識別。

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

[**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





