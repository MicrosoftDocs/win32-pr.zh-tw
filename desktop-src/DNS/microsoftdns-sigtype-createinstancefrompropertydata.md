---
title: MicrosoftDNS_SIGType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化簽章 (SIG) 資源記錄。
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_SIGType 類別
- MicrosoftDNS_SIGType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90501af2f6e492e56d17f88fb6bc74cc72522503760688457832a2374918100e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076722"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>MicrosoftDNS SIGType 類別的 CreateInstanceFromPropertyData 方法 \_

**CreateInstanceFromPropertyData** 方法會具現化簽章 (SIG) 資源記錄。

## <a name="syntax"></a>語法


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
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

*TypeCovered* \[在\]
</dt> <dd>

此 SIG 所涵蓋的 RR 類型。

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

*標籤* \[在\]
</dt> <dd>

原始 SIG RR 擁有者名稱中的標籤計數（不帶正負號）。 此計數不包含根的 Null 標籤，也不包含任何初始萬用字元。

</dd> <dt>

*OriginalTTL* \[在\]
</dt> <dd>

由 SIG 簽署之 RR 集合的 TTL。

</dd> <dt>

*SignatureExpiration* \[在\]
</dt> <dd>

簽章到期日（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。

</dd> <dt>

*SignatureInception* \[在\]
</dt> <dd>

簽章變成有效的日期和時間（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。

</dd> <dt>

*KeyTag* \[在\]
</dt> <dd>

方法，用來選擇驗證 SIG 的索引鍵。 如需用來計算 KeyTag 的方法，請參閱 RFC 2535、附錄 C。

</dd> <dt>

*SignerName* \[在\]
</dt> <dd>

產生 SIG RR 之簽署者的功能變數名稱。

</dd> <dt>

簽章 \[在\]
</dt> <dd>

以 base 64 表示的簽章，格式如 RFC 2535 中所定義，附錄 A。

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

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ SIGType 類別的方法**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





