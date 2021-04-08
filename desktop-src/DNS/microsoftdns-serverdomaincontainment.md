---
title: MicrosoftDNS_ServerDomainContainment 類別
description: MicrosoftDNS \_ 伺服器關聯 WMI 類別的每個實例都可以包含多個 MicrosoftDNS \_ 網域類別的實例。
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment 類別 DNS
- MicrosoftDNS_ServerDomainContainment 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685599"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>MicrosoftDNS \_ ServerDomainContainment 類別

[**MicrosoftDNS \_ 伺服器**](microsoftdns-server.md)關聯 WMI 類別的每個實例都可以包含多個 [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)類別的實例。 **MicrosoftDNS \_ 網域** 類別的每個實例都屬於 **MicrosoftDNS \_ 伺服器** 類別的單一實例，且定義為該伺服器的弱式。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ ServerDomainContainment** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MicrosoftDNS \_ ServerDomainContainment** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **MicrosoftDNS \_ Server**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

限定詞： Key、Override ( "GroupComponent" ) 、Min (1) 、Max (1) 

描述： DNS 伺服器。

繼承自 **CIM \_ 元件**。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **MicrosoftDNS \_ 網域**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

限定詞： Key、Override ( "PartComponent" ) 

描述： DNS 伺服器所管理的網域、區域、快取或 RootHints。

繼承自 **CIM \_ 元件**。

</dd> </dl>

## <a name="remarks"></a>備註

**MicrosoftDNS \_ ServerDomainContainment** 類別衍生自 **CIM \_ 元件** 類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





