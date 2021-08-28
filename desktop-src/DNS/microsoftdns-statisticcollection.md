---
title: MicrosoftDNS_StatisticCollection
description: MicrosoftDNS \_ StatisticCollection 類別代表相關 DNS 伺服器統計資料的集合。
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fda276433290ab2b151b4b6a34abae7a0113ee3db75054f6c66c0536009dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109088"
---
# <a name="microsoftdns_statisticcollection"></a>MicrosoftDNS \_ StatisticCollection

MicrosoftDNS \_ StatisticCollection 類別代表相關 DNS 伺服器統計資料的集合。

以下是從 MOF 程式碼簡化的語法。

``` syntax
class MicrosoftDNS_StatisticCollection : CIM_LogicalElement
{
  string Name;
  uint32 StatId;
  MicrosoftDNS_Statistic Statistics[];
};
```

## <a name="properties"></a>屬性

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**
</dt> <dd>

統計資料集合的名稱。

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**StatId**
</dt> <dd>

統計資料集合的數值標記法。

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**MicrosoftDNS \_ 統計資料統計資料\[\]**
</dt> <dd>

與統計資料相關聯的值陣列。

</dd> </dl>

## <a name="methods"></a>方法

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>這個類別沒有任何方法。
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MicrosoftDNS \_ 統計資料**](microsoftdns-statistic.md)
</dt> </dl>

 

 




