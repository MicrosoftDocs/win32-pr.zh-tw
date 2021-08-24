---
title: MicrosoftDNS_TXTType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化文字 (TXT) 資源記錄。
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_TXTType 類別
- MicrosoftDNS_TXTType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb0d1282f5a9bedac25d808455907ac3faa8e001da58447506123b4b5f5b78a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655298"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a>MicrosoftDNS TXTType 類別的 CreateInstanceFromPropertyData 方法 \_

**CreateInstanceFromPropertyData** 方法會具現化文字 (TXT) 資源記錄。

## <a name="syntax"></a>語法


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
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

包含此 RR 之區域、快取或 RootHints 實例的容器名稱。

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

*DescriptiveText* \[在\]
</dt> <dd>

描述性文字，相依于擁有者網域的語法。

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

[**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ TXTType 類別的方法**](microsoftdns-txttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





