---
title: 事件架構複雜類型
description: 以下是事件架構定義的複雜類型。
ms.assetid: bc995483-7e54-4224-a372-4e63b0dd764c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2844fef209aedf6819aeaa5a5b6b8a2d698b39a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976327"
---
# <a name="event-schema-complex-types"></a><span data-ttu-id="7be2b-103">事件架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="7be2b-103">Event Schema Complex Types</span></span>

<span data-ttu-id="7be2b-104">以下是事件架構定義的複雜類型。</span><span class="sxs-lookup"><span data-stu-id="7be2b-104">The following are the complex types that the Event schema defines.</span></span>



| <span data-ttu-id="7be2b-105">複雜類型</span><span class="sxs-lookup"><span data-stu-id="7be2b-105">Complex type</span></span>                                                                       | <span data-ttu-id="7be2b-106">Description</span><span class="sxs-lookup"><span data-stu-id="7be2b-106">Description</span></span>                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7be2b-107">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-107">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md)                 | <span data-ttu-id="7be2b-108">定義包含一或多個資料項目的結構。</span><span class="sxs-lookup"><span data-stu-id="7be2b-108">Defines a structure that contains one or more data items.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="7be2b-109">**資料類型**</span><span class="sxs-lookup"><span data-stu-id="7be2b-109">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)                          | <span data-ttu-id="7be2b-110">定義資料項目。</span><span class="sxs-lookup"><span data-stu-id="7be2b-110">Defines a data item.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="7be2b-111">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-111">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="7be2b-112">定義可以針對 Windows 軟體追蹤預處理器 (的 WPP) 事件記錄的資料。</span><span class="sxs-lookup"><span data-stu-id="7be2b-112">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="7be2b-113">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-113">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="7be2b-114">定義事件資料項目和包含事件資料的結構。</span><span class="sxs-lookup"><span data-stu-id="7be2b-114">Defines the event data items and structures that contains the event data.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="7be2b-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-115">**EventType**</span></span>](eventschema-eventtype-complextype.md)                             | <span data-ttu-id="7be2b-116">定義事件架構的根節點。</span><span class="sxs-lookup"><span data-stu-id="7be2b-116">Defines the root node of the Event schema.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="7be2b-117">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-117">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="7be2b-118">定義在轉譯事件的事件資料時所發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7be2b-118">Defines an error that occurred while rendering the event data for the event.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="7be2b-119">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-119">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="7be2b-120">定義事件的呈現訊息。</span><span class="sxs-lookup"><span data-stu-id="7be2b-120">Defines the rendered messages for the event.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="7be2b-121">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-121">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="7be2b-122">定義識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="7be2b-122">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/> |
| [<span data-ttu-id="7be2b-123">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="7be2b-123">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="7be2b-124">定義指定事件資料版面配置的 XML 片段。</span><span class="sxs-lookup"><span data-stu-id="7be2b-124">Defines an XML fragment that specifies the layout of the event data.</span></span><br/>                                                                                                                           |



 

 

 





