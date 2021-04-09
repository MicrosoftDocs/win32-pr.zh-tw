---
title: Modify MicrosoftDNS_KEYType 類別的方法
description: Modify 方法會更新金鑰資源記錄。
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_KEYType 類別
- MicrosoftDNS_KEYType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106127"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Modify MicrosoftDNS \_ KEYType 類別的方法

**Modify** 方法會更新金鑰資源記錄。

## <a name="syntax"></a>語法


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TTL* \[在中，選擇性\]
</dt> <dd>

DNS 解析程式可以快取 RR 的時間（以秒為單位）。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

用來指定對應的旗標，如 IETF RFC 2535 中所述。

</dd> <dt>

*通訊協定* \[在中，選擇性\]
</dt> <dd>

可使用在 RR 中指定之金鑰的通訊協定。 指派的值如下表所示。



| 值                                                                                                    | 意義                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | 電子郵件<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | dnssec<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | 所有通訊協定<br/> |



 

</dd> <dt>

*演算法* \[在中，選擇性\]
</dt> <dd>

與資源記錄中指定的金鑰搭配使用的演算法。 指派的值如下表所示。



| 值                                                                                                | 意義                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537) <br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539) <br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536) <br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 橢圓曲線密碼編譯<br/> |



 

</dd> <dt>

*PublicKey* \[在中，選擇性\]
</dt> <dd>

公開金鑰，以基底64表示，如 RFC 2535 的附錄 A 所述。

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

[**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**MicrosoftDNS KEYType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





