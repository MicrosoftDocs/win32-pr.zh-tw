---
title: MicrosoftDNS_Zone 類別的 CreateZone 方法
description: CreateZone 方法會建立 DNS 區域。
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- CreateZone 方法 DNS
- CreateZone 方法 DNS，MicrosoftDNS_Zone 類別
- MicrosoftDNS_Zone 類別 DNS，CreateZone 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025272"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>MicrosoftDNS 區域類別的 CreateZone 方法 \_

**CreateZone** 方法會建立 DNS 區域。

## <a name="syntax"></a>語法


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ZoneName* \[在\]
</dt> <dd>

代表區功能變數名稱稱的字串。

</dd> <dt>

*ZoneType* \[在\]
</dt> <dd>

區欄位型別。 有效的值如下：



| 值                                                                        | 意義                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | AD 整合。<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | 次要區域。<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | 虛設常式區域。<br/> **Windows Server 2003：** 此區欄位型別是在 Windows Server 2003 中引進。<br/>      |
| <dl> <dt>4</dt> </dl> | 區域轉寄站。<br/> **Windows Server 2003：** 此區欄位型別是在 Windows Server 2003 中引進。<br/> |



 

</dd> <dt>

*DsIntegrated* \[在\]
</dt> <dd>

指出區域資料是否儲存在 Active Directory 或檔案中。 若為 TRUE，則會將資料儲存在 Active Directory;如果為 FALSE，則表示資料儲存在檔案中。

</dd> <dt>

*DataFileName* \[在中，選擇性\]
</dt> <dd>

與區域相關聯的資料檔案名稱。

</dd> <dt>

*IpAddr* \[在中，選擇性\]
</dt> <dd>

區域主要 DNS 伺服器的 IP 位址。

</dd> <dt>

*AdminEmailName* \[在中，選擇性\]
</dt> <dd>

負責區域之系統管理員的電子郵件地址。

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

**MicrosoftDns \_ 區域** 類型的 RR。

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

 

 





