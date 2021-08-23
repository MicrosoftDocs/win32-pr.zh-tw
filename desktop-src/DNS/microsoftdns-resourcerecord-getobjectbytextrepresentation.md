---
title: MicrosoftDNS_ResourceRecord 類別的 GetObjectByTextRepresentation 方法
description: GetObjectByTextRepresentation 方法會捕獲 MicrosoftDNS ResourceRecord 類別的現有實例 \_ 。
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- GetObjectByTextRepresentation 方法 DNS
- GetObjectByTextRepresentation 方法 DNS，MicrosoftDNS_ResourceRecord 類別
- MicrosoftDNS_ResourceRecord 類別 DNS，GetObjectByTextRepresentation 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e3b824ccabe86e842d4ef6f61799b33110b5d28a58658a6d4cbedc824c134b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692418"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>MicrosoftDNS ResourceRecord 類別的 GetObjectByTextRepresentation 方法 \_

**GetObjectByTextRepresentation** 方法會捕獲 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)類別的現有實例。

## <a name="syntax"></a>語法


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DnsServerName* \[在\]
</dt> <dd>

應從中取出 RR 的 DNS 伺服器名稱。

</dd> <dt>

*容器* \[在\]
</dt> <dd>

應從中取得 RR 的容器名稱。

</dd> <dt>

*TextRepresentation* \[在\]
</dt> <dd>

要抓取之 RR 的文字標記法。

</dd> <dt>

*RR* \[擴展\]
</dt> <dd>

已具現化之 RR 的參考。

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法 \_**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





