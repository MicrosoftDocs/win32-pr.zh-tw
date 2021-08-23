---
description: 以字母 P 開頭的網路監視器詞彙的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: 'P (網路監視器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de258a4394ae13ca71a62d90fd9ee9218862ab7845c7300fcfe509a3a286f34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555468"
---
# <a name="p-network-monitor"></a>P (網路監視器) 

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**包**
</dt> <dd>

請參閱 [*框架*](f.md)。

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**解析 器**
</dt> <dd>

此元件會在延遲的捕獲中偵測特定的通訊協定。 每個剖析器都可以偵測到一個通訊協定。 不過，一個剖析器 DLL 可能包含多個剖析器。 也稱為通訊協定剖析器。

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

網路監視器初始化檔，其中包含所有已安裝之剖析器的清單。 每個剖析器都有一個描述剖析器的批註字串、剖析器的後面一組，以及任何與剖析器相關聯的說明檔。 當網路監視器呼叫 **ParserAutoInstallInfo** 或剖析器 DLL 呼叫 **CreateHandoffTable** 時，會更新剖析器 INI 檔。

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**監控**
</dt> <dd>

一種軟體工具，可讓您查看網路效能相關的變數，以識別進程的活動。

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**混合模式**
</dt> <dd>

一種狀態，其中網路介面卡會複製通過網路的所有框架，不論本機緩衝區的目的地位址為何。 此模式可讓網路監視器捕捉和顯示所有網路流量。

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**財產**
</dt> <dd>

剖析器中的通訊協定元素，描述使用該通訊協定傳送之框架內的資料欄位。

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**屬性資料庫**
</dt> <dd>

定義特定通訊協定所支援之所有屬性的內部資料庫。 屬性資料庫包含剖析器所定義之每個屬性的 **PROPERTYINFO** 結構。 網路監視器使用資料庫中的資訊，將屬性定義附加至屬性的實例，以及其格式化在網路監視器 UI 的詳細資料窗格中顯示的屬性資料時。

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**通訊協定層級**
</dt> <dd>

通訊協定屬性的邏輯群組。

</dd> </dl>

 

 



