---
title: MicrosoftDNS_AFSDBType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_AFSDBType 類別
- MicrosoftDNS_AFSDBType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934386"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a>MicrosoftDNS AFSDBType 類別的 CreateInstanceFromPropertyData 方法 \_

**CreateInstanceFromPropertyData** 方法會具現化 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。

## <a name="syntax"></a>語法


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DnsServerName* \[在\]
</dt> <dd>

包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。

</dd> <dt>

*容器* \[在\]
</dt> <dd>

包含此 RR 之 Zone、Cache 或 RootHints 實例的容器名稱。

</dd> <dt>

*OwnerName* \[在\]
</dt> <dd>

RR 的擁有者名稱。

</dd> <dt>

*RecordClass* \[在中，選擇性\]
</dt> <dd>

RR 的類別。 預設值為 1。 下列是有效的值。



| 值                                                                                                | 意義                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 在 (網際網路) <br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET) <br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (混亂) <br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod) <br/>   |



 

</dd> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*子類型* \[在\]
</dt> <dd>

主機 AFS 伺服器的子類型。 針對子類型 1 (值 = 1) ，主機具有適用于已命名 AFS 資料格的 AFS 3.0 磁片區位置伺服器。 在子類型 2 (值 = 2) 的情況下，主機會有經過驗證的名稱伺服器，保留命名的 DCE/NCA 資料格的資料格根目錄節點。

</dd> <dt>

*ServerName* \[在\]
</dt> <dd>

FQDN 指定主機，該主機的擁有者名稱中指定的 AFS 資料格具有伺服器。

</dd> <dt>

*RR* \[out、ref\]
</dt> <dd>

新物件的參考。

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

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ AFSDBType 類別的方法**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





