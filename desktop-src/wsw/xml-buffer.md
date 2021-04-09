---
title: XML 緩衝區
description: XML 緩衝區可為任意 XML 資料提供有效率的記憶體內部儲存體。
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- 適用于 Windows 的 XML 緩衝區 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933731"
---
# <a name="xml-buffer"></a><span data-ttu-id="f2ee8-106">XML 緩衝區</span><span class="sxs-lookup"><span data-stu-id="f2ee8-106">XML Buffer</span></span>

<span data-ttu-id="f2ee8-107">XML 緩衝區可為任意 XML 資料提供有效率的記憶體內部儲存體。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-107">An XML Buffer provides efficient in-memory storage for arbitrary XML data.</span></span>


<span data-ttu-id="f2ee8-108">若要從 XML 緩衝區讀取資料，請使用 [Xml 讀取器](xml-reader.md) ，並使用 xml 緩衝區來呼叫 [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) 。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-108">To read data from an XML Buffer, use a [XML Reader](xml-reader.md) and call [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="f2ee8-109">讀取器將位於檔的開頭。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-109">The reader will be positioned at the start of the document.</span></span>

<span data-ttu-id="f2ee8-110">若要將資料插入緩衝區，請使用 [Xml 寫入器](xml-writer.md) ，並使用 xml 緩衝區來呼叫 [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) 。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-110">To insert data into a buffer, use a [XML Writer](xml-writer.md) and call [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="f2ee8-111">寫入器將位於檔結尾。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-111">The writer will be positioned at the end of the document.</span></span>

<span data-ttu-id="f2ee8-112">一旦將讀取器設定為 XML 緩衝區，除了所有的 XML 讀取器 Api 之外， [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) 可以用來透過檔流覽讀取器。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-112">Once a reader has been set to an XML Buffer, in addition to all of the XML Reader APIs, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) may be used to navigate the reader through the document.</span></span> <span data-ttu-id="f2ee8-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) 和 [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) 也可以用來記錄檔中的位置，並于稍後返回。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) and [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) may also be used to record a position in the document and return to it later.</span></span>

<span data-ttu-id="f2ee8-114">一旦將寫入器設定為 XML 緩衝區，除了所有的 XML 寫入器 Api 之外， [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) 可以用來透過檔導覽寫入器。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-114">Once a writer has been set to an XML Buffer, in addition to all of the XML Writer APIs, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) may be used to navigate the writer through the document.</span></span> <span data-ttu-id="f2ee8-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) 和 [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) 也可以用來記錄檔中的位置，並于稍後返回。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) may also be used to record a position in the document and return to it later.</span></span> <span data-ttu-id="f2ee8-116">寫入器一律會在其所在的節點之前插入資料。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-116">The writer always inserts data before the node to which it is positioned.</span></span>

<span data-ttu-id="f2ee8-117">您可以從 XML 緩衝區中刪除節點，方法是取得使用 [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) 或 [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) 的節點位置，然後使用該位置來呼叫 [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) 。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-117">Nodes may be deleted from the XML Buffer by obtaining the position of the node using [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) or [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and then calling [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) with that position.</span></span> <span data-ttu-id="f2ee8-118">若為元素，這將會刪除專案（其所有子系，包括其相符的 end 元素）。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-118">For elements, this will delete the element, all its children including its matching end element.</span></span>

<span data-ttu-id="f2ee8-119">位置由值 [**WS \_ XML \_ 節點 \_ 位置**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)表示。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-119">A position is represented by the value [**WS\_XML\_NODE\_POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span></span> <span data-ttu-id="f2ee8-120">位置是特定 XML 緩衝區專屬的，而且只要 XML 緩衝區有效，就會有效。</span><span class="sxs-lookup"><span data-stu-id="f2ee8-120">Positions are specific to a particular XML Buffer, and are only valid as long as the XML Buffer is valid.</span></span>

<span data-ttu-id="f2ee8-121">下列列舉適用于 XML 緩衝區：</span><span class="sxs-lookup"><span data-stu-id="f2ee8-121">The following enumerations are used with XML buffers:</span></span>

-   [<span data-ttu-id="f2ee8-122">**WS \_ 移 \_ 至**</span><span class="sxs-lookup"><span data-stu-id="f2ee8-122">**WS\_MOVE\_TO**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="f2ee8-123">**WS \_ XML \_ 緩衝區 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f2ee8-123">**WS\_XML\_BUFFER\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="f2ee8-124">下列函式適用于 XML 緩衝區：</span><span class="sxs-lookup"><span data-stu-id="f2ee8-124">The following functions are used with XML buffers:</span></span>

-   [<span data-ttu-id="f2ee8-125">**WsCreateXmlBuffer**</span><span class="sxs-lookup"><span data-stu-id="f2ee8-125">**WsCreateXmlBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [<span data-ttu-id="f2ee8-126">**WsRemoveNode**</span><span class="sxs-lookup"><span data-stu-id="f2ee8-126">**WsRemoveNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

<span data-ttu-id="f2ee8-127">下列控制碼用於 XML 緩衝區：</span><span class="sxs-lookup"><span data-stu-id="f2ee8-127">The following handle is used with XML buffers:</span></span>

-   [<span data-ttu-id="f2ee8-128">WS \_ XML \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="f2ee8-128">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)

<span data-ttu-id="f2ee8-129">下列結構適用于 XML 緩衝區：</span><span class="sxs-lookup"><span data-stu-id="f2ee8-129">The following structures are used with XML buffers:</span></span>

-   [<span data-ttu-id="f2ee8-130">**WS \_ XML \_ 緩衝區 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="f2ee8-130">**WS\_XML\_BUFFER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [<span data-ttu-id="f2ee8-131">**WS \_ XML \_ 節點 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="f2ee8-131">**WS\_XML\_NODE\_POSITION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




