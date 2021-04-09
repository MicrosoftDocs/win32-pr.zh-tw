---
title: 事件結構描述
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 深入瞭解：事件架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849221"
---
# <a name="event-schema"></a><span data-ttu-id="6e3d2-103">事件結構描述</span><span class="sxs-lookup"><span data-stu-id="6e3d2-103">Event Schema</span></span>

<span data-ttu-id="6e3d2-104">事件架構會定義下列專案和類型，以識別已記錄事件的元素和屬性：</span><span class="sxs-lookup"><span data-stu-id="6e3d2-104">The Event schema defines the following elements and types that identify the elements and attributes of a logged event:</span></span>

-   [<span data-ttu-id="6e3d2-105">EventSchema 元素</span><span class="sxs-lookup"><span data-stu-id="6e3d2-105">EventSchema Elements</span></span>](eventschema-elements.md)
-   [<span data-ttu-id="6e3d2-106">EventSchema 簡單類型</span><span class="sxs-lookup"><span data-stu-id="6e3d2-106">EventSchema Simple Types</span></span>](eventschema-simple-types.md)
-   [<span data-ttu-id="6e3d2-107">EventSchema 複雜類型</span><span class="sxs-lookup"><span data-stu-id="6e3d2-107">EventSchema Complex Types</span></span>](eventschema-complex-types.md)

<span data-ttu-id="6e3d2-108">Elements 區段包含您會在記錄的事件中尋找的元素名稱;不過，若要取得每個專案的詳細資料，請參閱包含元素的複雜類型。</span><span class="sxs-lookup"><span data-stu-id="6e3d2-108">The elements section contains the names of the elements that you would find in a logged events; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="6e3d2-109">Windows SDK 包含 \\ include 事件 .xsd 檔中的架構 \\ 。</span><span class="sxs-lookup"><span data-stu-id="6e3d2-109">The Windows SDK includes the schema in the \\Include\\Event.xsd file.</span></span>

<span data-ttu-id="6e3d2-110">您可以在呼叫 [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) 函式以轉譯事件的特定區段或屬性時，使用此架構來識別元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="6e3d2-110">You can use this schema to identify the elements and attributes when calling the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to render specific sections or properties of the event.</span></span> <span data-ttu-id="6e3d2-111">如需顯示如何在轉譯事件時使用這個架構的範例，請參閱轉譯 [事件](rendering-events.md)。</span><span class="sxs-lookup"><span data-stu-id="6e3d2-111">For an example that shows how to use this schema when rendering events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="6e3d2-112">除了事件架構之外，Windows 事件記錄檔也會定義下列架構：</span><span class="sxs-lookup"><span data-stu-id="6e3d2-112">In addition to the Event schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="6e3d2-113">[EventManifest 架構](eventmanifestschema-schema.md)：定義用來寫入檢測資訊清單的元素和類型。</span><span class="sxs-lookup"><span data-stu-id="6e3d2-113">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="6e3d2-114">[查詢架構](queryschema-schema.md)：定義用來撰寫查詢以從一或多個通道取出事件的元素和類型。</span><span class="sxs-lookup"><span data-stu-id="6e3d2-114">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




