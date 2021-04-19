---
title: XML 寫入器
description: XML 寫入器是發出 XML 的 API。 在其核心中，XML 寫入器會一次寫入一個 XML 節點，但還有其他協助程式 Api 可讓您更輕鬆地撰寫一系列節點。
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- 適用于 Windows 的 XML 寫入器 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106969740"
---
# <a name="xml-writer"></a><span data-ttu-id="cd308-107">XML 寫入器</span><span class="sxs-lookup"><span data-stu-id="cd308-107">XML Writer</span></span>

<span data-ttu-id="cd308-108">XML 寫入器是發出 XML 的 API。</span><span class="sxs-lookup"><span data-stu-id="cd308-108">XML Writer is an API for emitting XML.</span></span> <span data-ttu-id="cd308-109">在其核心中，XML 寫入器會一次寫入一個 [XML 節點](xml-node.md) ，但還有其他協助程式 api 可讓您更輕鬆地撰寫一系列節點。</span><span class="sxs-lookup"><span data-stu-id="cd308-109">At its core, an XML Writer writes one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make writing a sequence of nodes easier.</span></span>


<span data-ttu-id="cd308-110">支援下列類型的寫入器輸出：</span><span class="sxs-lookup"><span data-stu-id="cd308-110">The following types of writer output are supported:</span></span>

-   [<span data-ttu-id="cd308-111">**編碼位元組的記憶體中緩衝區**</span><span class="sxs-lookup"><span data-stu-id="cd308-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="cd308-112">**資料流程**</span><span class="sxs-lookup"><span data-stu-id="cd308-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   <span data-ttu-id="cd308-113">[XML 緩衝區](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="cd308-113">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="cd308-114">下列回呼適用于 XML 寫入器：</span><span class="sxs-lookup"><span data-stu-id="cd308-114">The following callbacks are used with the XML writer:</span></span>

-   [<span data-ttu-id="cd308-115">**WS \_ 動態 \_ 字串 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cd308-115">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="cd308-116">**WS \_ 提取 \_ 位元組 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cd308-116">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="cd308-117">**WS \_ PUSH \_ BYTES \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cd308-117">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="cd308-118">**WS \_ 寫入 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cd308-118">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

<span data-ttu-id="cd308-119">下列列舉適用于 XML 寫入器：</span><span class="sxs-lookup"><span data-stu-id="cd308-119">The following enumerations are used with the XML writer:</span></span>

-   [<span data-ttu-id="cd308-120">**WS \_ 字元集**</span><span class="sxs-lookup"><span data-stu-id="cd308-120">**WS\_CHARSET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [<span data-ttu-id="cd308-121">**WS \_ XML \_ 寫入器 \_ 編碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="cd308-121">**WS\_XML\_WRITER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="cd308-122">**WS \_ XML \_ 寫入器 \_ 輸出 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="cd308-122">**WS\_XML\_WRITER\_OUTPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [<span data-ttu-id="cd308-123">**WS \_ XML \_ 寫入器 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="cd308-123">**WS\_XML\_WRITER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

<span data-ttu-id="cd308-124">下列函式會搭配 XML 寫入器使用：</span><span class="sxs-lookup"><span data-stu-id="cd308-124">The following functions are used with the XML writer:</span></span>

-   [<span data-ttu-id="cd308-125">**WsCopyNode**</span><span class="sxs-lookup"><span data-stu-id="cd308-125">**WsCopyNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [<span data-ttu-id="cd308-126">**WsCreateWriter**</span><span class="sxs-lookup"><span data-stu-id="cd308-126">**WsCreateWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [<span data-ttu-id="cd308-127">**WsFlushWriter**</span><span class="sxs-lookup"><span data-stu-id="cd308-127">**WsFlushWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [<span data-ttu-id="cd308-128">**WsFreeWriter**</span><span class="sxs-lookup"><span data-stu-id="cd308-128">**WsFreeWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [<span data-ttu-id="cd308-129">**WsGetPrefixFromNamespace**</span><span class="sxs-lookup"><span data-stu-id="cd308-129">**WsGetPrefixFromNamespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [<span data-ttu-id="cd308-130">**WsGetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="cd308-130">**WsGetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [<span data-ttu-id="cd308-131">**WsGetWriterProperty**</span><span class="sxs-lookup"><span data-stu-id="cd308-131">**WsGetWriterProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [<span data-ttu-id="cd308-132">**WsMoveWriter**</span><span class="sxs-lookup"><span data-stu-id="cd308-132">**WsMoveWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [<span data-ttu-id="cd308-133">**WsPullBytes**</span><span class="sxs-lookup"><span data-stu-id="cd308-133">**WsPullBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [<span data-ttu-id="cd308-134">**WsPushBytes**</span><span class="sxs-lookup"><span data-stu-id="cd308-134">**WsPushBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [<span data-ttu-id="cd308-135">**WsSetOutput**</span><span class="sxs-lookup"><span data-stu-id="cd308-135">**WsSetOutput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [<span data-ttu-id="cd308-136">**WsSetOutputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd308-136">**WsSetOutputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [<span data-ttu-id="cd308-137">**WsSetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="cd308-137">**WsSetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [<span data-ttu-id="cd308-138">**WsWriteArray**</span><span class="sxs-lookup"><span data-stu-id="cd308-138">**WsWriteArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [<span data-ttu-id="cd308-139">**WsWriteBytes**</span><span class="sxs-lookup"><span data-stu-id="cd308-139">**WsWriteBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [<span data-ttu-id="cd308-140">**WsWriteChars**</span><span class="sxs-lookup"><span data-stu-id="cd308-140">**WsWriteChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [<span data-ttu-id="cd308-141">**WsWriteCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="cd308-141">**WsWriteCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [<span data-ttu-id="cd308-142">**WsWriteEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="cd308-142">**WsWriteEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [<span data-ttu-id="cd308-143">**WsWriteEndCData**</span><span class="sxs-lookup"><span data-stu-id="cd308-143">**WsWriteEndCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [<span data-ttu-id="cd308-144">**WsWriteEndElement**</span><span class="sxs-lookup"><span data-stu-id="cd308-144">**WsWriteEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [<span data-ttu-id="cd308-145">**WsWriteNode**</span><span class="sxs-lookup"><span data-stu-id="cd308-145">**WsWriteNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [<span data-ttu-id="cd308-146">**WsWriteQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="cd308-146">**WsWriteQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [<span data-ttu-id="cd308-147">**WsWriteStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="cd308-147">**WsWriteStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [<span data-ttu-id="cd308-148">**WsWriteStartCData**</span><span class="sxs-lookup"><span data-stu-id="cd308-148">**WsWriteStartCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [<span data-ttu-id="cd308-149">**WsWriteStartElement**</span><span class="sxs-lookup"><span data-stu-id="cd308-149">**WsWriteStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [<span data-ttu-id="cd308-150">**WsWriteText**</span><span class="sxs-lookup"><span data-stu-id="cd308-150">**WsWriteText**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [<span data-ttu-id="cd308-151">**WsWriteValue**</span><span class="sxs-lookup"><span data-stu-id="cd308-151">**WsWriteValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [<span data-ttu-id="cd308-152">**WsWriteXmlnsAttribute**</span><span class="sxs-lookup"><span data-stu-id="cd308-152">**WsWriteXmlnsAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

<span data-ttu-id="cd308-153">下列控制碼會搭配 XML 寫入器使用：</span><span class="sxs-lookup"><span data-stu-id="cd308-153">The following handle is used with the XML writer:</span></span>

-   [<span data-ttu-id="cd308-154">WS \_ XML \_ 寫入器</span><span class="sxs-lookup"><span data-stu-id="cd308-154">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)

<span data-ttu-id="cd308-155">下列結構適用于 XML 寫入器：</span><span class="sxs-lookup"><span data-stu-id="cd308-155">The following structures are used with the XML writer:</span></span>

-   [<span data-ttu-id="cd308-156">**WS \_ XML \_ 寫入器 \_ 二進位 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="cd308-156">**WS\_XML\_WRITER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [<span data-ttu-id="cd308-157">**WS \_ XML \_ 寫入器 \_ 緩衝區 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="cd308-157">**WS\_XML\_WRITER\_BUFFER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="cd308-158">**WS \_ XML \_ 寫入器 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="cd308-158">**WS\_XML\_WRITER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [<span data-ttu-id="cd308-159">**WS \_ XML \_ 寫入器 \_ MTOM \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="cd308-159">**WS\_XML\_WRITER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [<span data-ttu-id="cd308-160">**WS \_ XML \_ 寫入器 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="cd308-160">**WS\_XML\_WRITER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [<span data-ttu-id="cd308-161">**WS \_ XML \_ 寫入器 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="cd308-161">**WS\_XML\_WRITER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [<span data-ttu-id="cd308-162">**WS \_ XML \_ 寫入器 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="cd308-162">**WS\_XML\_WRITER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [<span data-ttu-id="cd308-163">**WS \_ XML \_ 寫入器 \_ 資料流程 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="cd308-163">**WS\_XML\_WRITER\_STREAM\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [<span data-ttu-id="cd308-164">**WS \_ XML \_ 寫入器 \_ 文字 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="cd308-164">**WS\_XML\_WRITER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




