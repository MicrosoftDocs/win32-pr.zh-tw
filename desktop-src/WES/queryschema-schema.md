---
title: 查詢架構
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 深入瞭解：查詢架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194160"
---
# <a name="query-schema"></a><span data-ttu-id="3ffba-103">查詢架構</span><span class="sxs-lookup"><span data-stu-id="3ffba-103">Query Schema</span></span>

<span data-ttu-id="3ffba-104">查詢架構會定義下列專案和類型，您可用來撰寫結構化 XML 查詢，以從通道或記錄檔抓取事件：</span><span class="sxs-lookup"><span data-stu-id="3ffba-104">The Query Schema defines the following elements and types that you can use to write a structured XML query to retrieve events from a channel or log file:</span></span>

-   [<span data-ttu-id="3ffba-105">QuerySchema 元素</span><span class="sxs-lookup"><span data-stu-id="3ffba-105">QuerySchema Elements</span></span>](queryschema-elements.md)
-   [<span data-ttu-id="3ffba-106">QuerySchema 複雜類型</span><span class="sxs-lookup"><span data-stu-id="3ffba-106">QuerySchema Complex Types</span></span>](queryschema-complex-types.md)

<span data-ttu-id="3ffba-107">Elements 區段包含您在查詢中使用的元素名稱;不過，若要取得每個專案的詳細資料，請參閱包含元素的複雜類型。</span><span class="sxs-lookup"><span data-stu-id="3ffba-107">The elements section contains the names of the elements that you use in your query; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="3ffba-108">查詢可包含一或多個用來在查詢結果集中包含或排除事件的 XPath 運算式。</span><span class="sxs-lookup"><span data-stu-id="3ffba-108">A query can contain one or more XPath expressions that are used to include or exclude event in the query result set.</span></span> <span data-ttu-id="3ffba-109">您可以從多個通道或記錄檔查詢事件，但是不能混用通道和記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3ffba-109">You can query for events from multiple channels or log files but you cannot mix channels and log files.</span></span> <span data-ttu-id="3ffba-110">您可以在任何採用 XPath (的函式中使用查詢，例如， [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 或 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函數) 。</span><span class="sxs-lookup"><span data-stu-id="3ffba-110">You can use a query in any function that takes an XPath (for example, the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions).</span></span> <span data-ttu-id="3ffba-111">您指定的每個 XPath 都會限制為32個運算式。</span><span class="sxs-lookup"><span data-stu-id="3ffba-111">Each XPath that you specify is limited to 32 expressions.</span></span> <span data-ttu-id="3ffba-112">如需範例，請參閱 [使用事件](consuming-events.md)。</span><span class="sxs-lookup"><span data-stu-id="3ffba-112">For an example, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="3ffba-113">Windows SDK 包括 \\ Include 查詢 .xsd 檔中的架構 \\ 。</span><span class="sxs-lookup"><span data-stu-id="3ffba-113">The Windows SDK includes the schema in the \\Include\\Query.xsd file.</span></span>

<span data-ttu-id="3ffba-114">除了查詢架構之外，Windows 事件記錄檔也會定義下列架構：</span><span class="sxs-lookup"><span data-stu-id="3ffba-114">In addition to the Query schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="3ffba-115">[EventManifest 架構](eventmanifestschema-schema.md)：定義用來寫入檢測資訊清單的元素和類型。</span><span class="sxs-lookup"><span data-stu-id="3ffba-115">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="3ffba-116">[事件架構](eventschema-schema.md)：定義用來呈現事件的元素和類型。</span><span class="sxs-lookup"><span data-stu-id="3ffba-116">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ffba-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ffba-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ffba-118">使用事件</span><span class="sxs-lookup"><span data-stu-id="3ffba-118">Consuming Events</span></span>](consuming-events.md)
</dt> </dl>

 

 




