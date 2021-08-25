---
title: MicrosoftDNS_DomainResourceRecordContainment 類別
description: MicrosoftDNS \_ DomainResourceRecordContainment 類別可用於 RR 內含專案; MicrosoftDNS 網域的每個實例 \_ 可能包含多個 MicrosoftDNS \_ ResourceRecord 類別的實例。
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment 類別 DNS
- MicrosoftDNS_DomainResourceRecordContainment 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498d9b953895ebece94dc77edb587045d1cfdd45c29f04c202756bd1080dc9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795608"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>MicrosoftDNS \_ DomainResourceRecordContainment 類別

**MicrosoftDNS \_ DomainResourceRecordContainment** 類別可用於 RR 內含專案; [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)的每個實例可能包含多個 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)類別的實例。 **MicrosoftDNS \_ ResourceRecord** 類別的每個實例都屬於 **MicrosoftDNS \_ 網域** 類別的單一實例，且定義為該實例的弱式。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ DomainResourceRecordContainment** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MicrosoftDNS \_ DomainResourceRecordContainment** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **MicrosoftDNS \_ 網域**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

限定詞： Key、Override ( "GroupComponent" ) 

描述：直接包含資源記錄的區域、快取、RootHints 或網域。

繼承自 CIM \_ 元件

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

限定詞： Key、Override ( "PartComponent" ) 

描述：網域、區域、快取或 RootHints 中包含的資源記錄。

繼承自 CIM \_ 元件。

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

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





