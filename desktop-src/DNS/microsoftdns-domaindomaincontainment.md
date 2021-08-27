---
title: MicrosoftDNS_DomainDomainContainment 類別
description: MicrosoftDNS \_ DomainDomainContainment 類別用於定義域內含專案;DNS 網域可能包含其他 DNS 網域。
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment 類別 DNS
- MicrosoftDNS_DomainDomainContainment 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f96d03f007af463fb4c4f672eb0d1374867636f4a4224469589563b9c5882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084748"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>MicrosoftDNS \_ DomainDomainContainment 類別

**MicrosoftDNS \_ DomainDomainContainment** 類別用於定義域內含專案;DNS 網域可能包含其他 DNS 網域。 [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)類別的每個實例都可以包含多個 **MicrosoftDNS \_ 網域** 的其他實例。 **MicrosoftDNS \_ 網域** 物件的實例直接包含在一個以上的較高層級 **MicrosoftDNS \_ 網域** 中。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ DomainDomainContainment** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MicrosoftDNS \_ DomainDomainContainment** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **MicrosoftDNS \_ 網域**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

限定詞：索引鍵、最大 (1) 、覆寫 ( "GroupComponent" ) 

描述：較高層級的網域、區域、快取或 RootHints。

繼承自 CIM \_ 元件

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **MicrosoftDNS \_ 網域**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

限定詞： Key、Override ( "PartComponent" ) 

描述：較高層級網域、區域、快取或 RootHints 所包含的網域。

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

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





