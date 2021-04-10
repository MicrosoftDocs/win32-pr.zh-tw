---
description: 以字母 P 開頭的網路監視器詞彙的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: 'P (網路監視器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026321"
---
# <a name="p-network-monitor"></a><span data-ttu-id="6cff0-103">P (網路監視器) </span><span class="sxs-lookup"><span data-stu-id="6cff0-103">P (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="6cff0-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**包**</span><span class="sxs-lookup"><span data-stu-id="6cff0-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**packet**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-105">請參閱 [*框架*](f.md)。</span><span class="sxs-lookup"><span data-stu-id="6cff0-105">See [*frame*](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cff0-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**解析 器**</span><span class="sxs-lookup"><span data-stu-id="6cff0-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-107">此元件會在延遲的捕獲中偵測特定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6cff0-107">A component that detects a specific protocol in a delayed capture.</span></span> <span data-ttu-id="6cff0-108">每個剖析器都可以偵測到一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6cff0-108">Each parser can detect one protocol.</span></span> <span data-ttu-id="6cff0-109">不過，一個剖析器 DLL 可能包含多個剖析器。</span><span class="sxs-lookup"><span data-stu-id="6cff0-109">However, one parser DLL may contain multiple parsers.</span></span> <span data-ttu-id="6cff0-110">也稱為通訊協定剖析器。</span><span class="sxs-lookup"><span data-stu-id="6cff0-110">Also called a protocol parser.</span></span>

</dd> <dt>

<span data-ttu-id="6cff0-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span><span class="sxs-lookup"><span data-stu-id="6cff0-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-112">網路監視器初始化檔，其中包含所有已安裝之剖析器的清單。</span><span class="sxs-lookup"><span data-stu-id="6cff0-112">A Network Monitor initialization file that contains a list of all the installed parsers.</span></span> <span data-ttu-id="6cff0-113">每個剖析器都有一個描述剖析器的批註字串、剖析器的後面一組，以及任何與剖析器相關聯的說明檔。</span><span class="sxs-lookup"><span data-stu-id="6cff0-113">For each parser there is a comment string that describes the parser, the follow set of the parser, and any Help file associated with the parser.</span></span> <span data-ttu-id="6cff0-114">當網路監視器呼叫 **ParserAutoInstallInfo** 或剖析器 DLL 呼叫 **CreateHandoffTable** 時，會更新剖析器 INI 檔。</span><span class="sxs-lookup"><span data-stu-id="6cff0-114">The parser INI file is updated when Network Monitor calls **ParserAutoInstallInfo**, or when the parser DLL calls **CreateHandoffTable**.</span></span>

</dd> <dt>

<span data-ttu-id="6cff0-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**監控**</span><span class="sxs-lookup"><span data-stu-id="6cff0-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-116">一種軟體工具，可讓您查看網路效能相關的變數，以識別進程的活動。</span><span class="sxs-lookup"><span data-stu-id="6cff0-116">A software tool that allows you to view network performance-related variables that identify the activity of a process.</span></span>

</dd> <dt>

<span data-ttu-id="6cff0-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**混合模式**</span><span class="sxs-lookup"><span data-stu-id="6cff0-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**promiscuous mode**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-118">一種狀態，其中網路介面卡會複製通過網路的所有框架，不論本機緩衝區的目的地位址為何。</span><span class="sxs-lookup"><span data-stu-id="6cff0-118">A state in which a network adapter card copies all the frames that pass over the network, regardless of the destination address to a local buffer.</span></span> <span data-ttu-id="6cff0-119">此模式可讓網路監視器捕捉和顯示所有網路流量。</span><span class="sxs-lookup"><span data-stu-id="6cff0-119">This mode enables Network Monitor to capture and display all network traffic.</span></span>

</dd> <dt>

<span data-ttu-id="6cff0-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**財產**</span><span class="sxs-lookup"><span data-stu-id="6cff0-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-121">剖析器中的通訊協定元素，描述使用該通訊協定傳送之框架內的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="6cff0-121">A protocol element in a parser that describes a data field within a frame that is sent by using that protocol.</span></span>

</dd> <dt>

<span data-ttu-id="6cff0-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**屬性資料庫**</span><span class="sxs-lookup"><span data-stu-id="6cff0-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**property database**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-123">定義特定通訊協定所支援之所有屬性的內部資料庫。</span><span class="sxs-lookup"><span data-stu-id="6cff0-123">An internal database that defines all the properties that a specific protocol supports.</span></span> <span data-ttu-id="6cff0-124">屬性資料庫包含剖析器所定義之每個屬性的 **PROPERTYINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="6cff0-124">The property database contains a **PROPERTYINFO** structure for each property that the parser defines.</span></span> <span data-ttu-id="6cff0-125">網路監視器使用資料庫中的資訊，將屬性定義附加至屬性的實例，以及其格式化在網路監視器 UI 的詳細資料窗格中顯示的屬性資料時。</span><span class="sxs-lookup"><span data-stu-id="6cff0-125">Network Monitor uses the information in the database when it attaches a property definition to an instance of the property, and when it formats the property data that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="6cff0-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**通訊協定層級**</span><span class="sxs-lookup"><span data-stu-id="6cff0-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**protocol level**</span></span>
</dt> <dd>

<span data-ttu-id="6cff0-127">通訊協定屬性的邏輯群組。</span><span class="sxs-lookup"><span data-stu-id="6cff0-127">A logical grouping of protocol properties.</span></span>

</dd> </dl>

 

 



