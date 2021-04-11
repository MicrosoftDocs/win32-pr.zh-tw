---
title: MicrosoftDNS_Domain 類別
description: MicrosoftDNS \_ 網域類別代表 DNS 階層中的網域。
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain 類別 DNS
- MicrosoftDNS_Domain 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103709"
---
# <a name="microsoftdns_domain-class"></a>MicrosoftDNS \_ 網域類別

**MicrosoftDNS \_ 網域** 類別代表 DNS 階層中的網域。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ 網域** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ 網域** 類別具有這些方法。



| 方法                   | 描述                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **GetDistinguishedName** | 取得區域的 DS 分辨名稱。 <br/> 限定詞：實作為<br/> |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ 網域** 類別具有這些屬性。

<dl> <dt>

**容器**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

網域的容器名稱，可能是區域、快取或 RootHints。

如果容器是 ([**MicrosoftDNS \_ 區域**](microsoftdns-zone.md) 類別實例的區域) ，此屬性就會包含區域的 FQDN。

如果容器是根區域，則 \\ 應使用字串。 \\

如果容器是資源記錄的 DNS 快取 ([**MicrosoftDNS \_ cache**](microsoftdns-cache.md) 類別的實例) ，這個屬性會設定 \\ 為字串。快取 \\ 。

如果 RootHints 容器 ([**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)) 類別的實例，則此屬性應該設定為 \\ 。RootHints \\ 。

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含網域之 DNS 伺服器的 FQDN 或 IP 位址。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

網域的 FQDN。

若為 DNS 快取或 RootHints 的實例，則為字串 \\ 。快取 \\ 和 \\ .。。\\ 應分別使用 RootHints。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS 網域類別的 GetDistinguishedName 方法 \_**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





