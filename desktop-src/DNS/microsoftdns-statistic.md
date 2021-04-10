---
title: MicrosoftDNS_Statistic 類別
description: MicrosoftDNS \_ 統計資料類別代表單一 DNS 伺服器統計資料。
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- MicrosoftDNS_Statistic 類別 DNS
- MicrosoftDNS_Statistic 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025372"
---
# <a name="microsoftdns_statistic-class"></a>MicrosoftDNS \_ 統計資料類別

**MicrosoftDNS \_ 統計** 資料類別代表單一 DNS 伺服器統計資料。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ 統計** 資料類別有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MicrosoftDNS \_ 統計** 資料類別具有這些屬性。

<dl> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**CollectionName** 的數值標記法。

</dd> <dt>

**CollectionName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

統計資料所屬集合的名稱。

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出包含統計資料之 DNS 伺服器的 FQDN 或 IP 位址。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

統計資料的名稱。

</dd> <dt>

**StringValue**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

統計資料的字串值，只有在統計資料值未表示為 DWORD 時才會使用。

</dd> <dt>

**值**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

統計資料的數值，以 DWORD 表示。

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

[MicrosoftDNS \_ StatisticCollection](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





