---
title: MicrosoftDNS_KEYType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化金鑰資源記錄。
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_KEYType 類別
- MicrosoftDNS_KEYType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315ef898a101b3a86fa5a3085e4a171edd8efa28972cf62c006cc0eb87e354b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913138"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a>MicrosoftDNS KEYType 類別的 CreateInstanceFromPropertyData 方法 \_

**CreateInstanceFromPropertyData** 方法會具現化金鑰資源記錄。

## <a name="syntax"></a>語法


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
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

*旗標* \[在\]
</dt> <dd>

用來指定對應的旗標，如 IETF RFC 2535 中所述。

</dd> <dt>

*通訊協定* \[在\]
</dt> <dd>

可以使用資源記錄中所指定金鑰的通訊協定。 指派的值如下表所示。



| 值                                                                                                    | 意義                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | 電子郵件<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | dnssec<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | 所有通訊協定<br/> |



 

</dd> <dt>

*演算法* \[在\]
</dt> <dd>

與資源記錄中指定的金鑰搭配使用的演算法。 指派的值如下表所示。



| 值                                                                                                | 意義                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537) <br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539) <br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536) <br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 橢圓曲線密碼編譯<br/> |



 

</dd> <dt>

*PublicKey* \[在\]
</dt> <dd>

公開金鑰，以基底64表示，如 RFC 2535 的附錄 A 所述。

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

[**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ KEYType 類別的方法**](microsoftdns-keytype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





