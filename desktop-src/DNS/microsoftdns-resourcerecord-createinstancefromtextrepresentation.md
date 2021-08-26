---
title: MicrosoftDNS_ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法
description: CreateInstanceFromTextRepresentation 方法會具現化 MicrosoftDNS \_ ResourceRecord 物件。
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- CreateInstanceFromTextRepresentation 方法 DNS
- CreateInstanceFromTextRepresentation 方法 DNS，MicrosoftDNS_ResourceRecord 類別
- MicrosoftDNS_ResourceRecord 類別 DNS，CreateInstanceFromTextRepresentation 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8ee7f92db1185fe2762b0b308b4fbafdbdd80e7417c7b615939c72333f15e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104018"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>MicrosoftDNS ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法 \_

**CreateInstanceFromTextRepresentation** 方法會具現化 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)物件。

## <a name="syntax"></a>語法


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DnsServerName* \[在\]
</dt> <dd>

應該在其上建立 RR 的 DNS 伺服器名稱。

</dd> <dt>

*容器* \[在\]
</dt> <dd>

應放置新 RR 的容器名稱。

</dd> <dt>

*TextRepresentation* \[在\]
</dt> <dd>

要建立之 RR 實例的文字表示。

</dd> <dt>

*RR* \[out、ref\]
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

[**MicrosoftDNS ResourceRecord 類別的 GetObjectByTextRepresentation 方法 \_**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





