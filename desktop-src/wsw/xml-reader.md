---
title: XML 讀取器
description: XML 讀取器是 XML 輸入來源的資料指標。 在其核心中，XML 讀取器一次會讀取一個 XML 節點，但有其他協助程式 Api 可讓您更輕鬆地讀取一系列節點。
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- 適用于 Windows 的 XML 讀取器 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463933"
---
# <a name="xml-reader"></a><span data-ttu-id="f9c59-107">XML 讀取器</span><span class="sxs-lookup"><span data-stu-id="f9c59-107">XML Reader</span></span>

<span data-ttu-id="f9c59-108">XML 讀取器是 XML 輸入來源的資料指標。</span><span class="sxs-lookup"><span data-stu-id="f9c59-108">XML Reader is a cursor over an input source of XML.</span></span> <span data-ttu-id="f9c59-109">在其核心中，XML 讀取器一次會讀取一個 [XML 節點](xml-node.md) ，但有其他協助程式 api 可讓您更輕鬆地讀取一系列節點。</span><span class="sxs-lookup"><span data-stu-id="f9c59-109">At its core, an XML Reader reads one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make reading a sequence of nodes easier.</span></span>


<span data-ttu-id="f9c59-110">以下是支援的讀取器輸入類型：</span><span class="sxs-lookup"><span data-stu-id="f9c59-110">The following types of readers input are supported:</span></span>

-   [<span data-ttu-id="f9c59-111">**編碼位元組的記憶體中緩衝區**</span><span class="sxs-lookup"><span data-stu-id="f9c59-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="f9c59-112">**資料流程**</span><span class="sxs-lookup"><span data-stu-id="f9c59-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   <span data-ttu-id="f9c59-113">[XML 緩衝區](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="f9c59-113">An [XML Buffer](xml-buffer.md)</span></span>

### <a name="security"></a><span data-ttu-id="f9c59-114">安全性</span><span class="sxs-lookup"><span data-stu-id="f9c59-114">Security</span></span>

<span data-ttu-id="f9c59-115">讀取器將確認元素上的屬性是否為唯一的。</span><span class="sxs-lookup"><span data-stu-id="f9c59-115">The reader will verify that the attributes present on an element are unique.</span></span> <span data-ttu-id="f9c59-116">執行這項驗證所需的時間，是元素上的屬性數目的函式，可以和 [**WS \_ XML \_ 讀取器屬性的 \_ \_ 最大值 \_ 屬性**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)一樣大。</span><span class="sxs-lookup"><span data-stu-id="f9c59-116">The time required to perform this validation is a function of the number of attributes on the element which can be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="f9c59-117">因此，當 **WS \_ XML \_ 讀取器 \_ 屬性 \_ 最大值 \_ 屬性** 設定為大數值時，處理大型檔可能會造成阻絕服務攻擊的機會。</span><span class="sxs-lookup"><span data-stu-id="f9c59-117">Therefore, processing large documents when **WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES** is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="f9c59-118">讀取器會將前置詞對應至每個元素和屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f9c59-118">The reader will map prefixes to namespaces for each element and attributes.</span></span> <span data-ttu-id="f9c59-119">執行此對應所需的時間，是範圍中 xmlns 屬性數目的函式，可能會與 [**WS \_ XML \_ 讀取器屬性的 \_ \_ 最大 \_ 命名空間**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)相同。</span><span class="sxs-lookup"><span data-stu-id="f9c59-119">The time required to perform this mapping is a function of the number of xmlns attributes in scope which may be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="f9c59-120">因此，當這個屬性設定為大數值時，處理大型檔可能會造成阻絕服務攻擊的機會。</span><span class="sxs-lookup"><span data-stu-id="f9c59-120">Therefore, processing large documents when this property is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="f9c59-121">雖然讀取器會確定檔遵循 xml 的語法規格，而且其層面是在指定的配額內，但在來自不受信任的來源時，檔的內容仍然必須被視為不受信任。</span><span class="sxs-lookup"><span data-stu-id="f9c59-121">While the reader will ensure that the document follows the grammatical specification of xml and furthermore that its aspects are within the quotas specified, the content of the document must still be considered untrusted when coming from an untrusted source.</span></span> <span data-ttu-id="f9c59-122">讀者的使用者應該使用 [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)、 [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)或手動檢查 [**節點**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)來檢查所有專案和屬性名稱和命名空間。</span><span class="sxs-lookup"><span data-stu-id="f9c59-122">Users of the reader should check all element and attribute names and namespaces using [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), or by manually inspecting [**nodes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span></span>

<span data-ttu-id="f9c59-123">還有一些其他需要考慮的情況包括（但不限於）：</span><span class="sxs-lookup"><span data-stu-id="f9c59-123">Some other situations to consider include, but are not limited to:</span></span>

-   <span data-ttu-id="f9c59-124">可能遺漏了預期的元素</span><span class="sxs-lookup"><span data-stu-id="f9c59-124">Expected elements may be missing</span></span>
-   <span data-ttu-id="f9c59-125">可能出現未預期的元素</span><span class="sxs-lookup"><span data-stu-id="f9c59-125">Unexpected elements may appear</span></span>
-   <span data-ttu-id="f9c59-126">可能遺漏了預期的屬性</span><span class="sxs-lookup"><span data-stu-id="f9c59-126">Expected attributes may be missing</span></span>
-   <span data-ttu-id="f9c59-127">可能會出現非預期的屬性</span><span class="sxs-lookup"><span data-stu-id="f9c59-127">Unexpected attributes may appear</span></span>
-   <span data-ttu-id="f9c59-128">元素可能會顯示為空白元素</span><span class="sxs-lookup"><span data-stu-id="f9c59-128">Elements may appear as empty elements</span></span>
-   <span data-ttu-id="f9c59-129">空白字元可能出現在非預期的位置</span><span class="sxs-lookup"><span data-stu-id="f9c59-129">Whitespace may appear in unexpected places</span></span>

<span data-ttu-id="f9c59-130">讀者的使用者不應該只根據從檔讀取的值來配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="f9c59-130">Users of the reader should not allocate memory based simply on values read from the document.</span></span> <span data-ttu-id="f9c59-131">例如，請考慮下列 xml 檔：</span><span class="sxs-lookup"><span data-stu-id="f9c59-131">For example, consider the following xml document:</span></span>

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

<span data-ttu-id="f9c59-132">配置以陣列為基礎的 soley 時，假設有一些元素將會是潛在的攻擊向量。</span><span class="sxs-lookup"><span data-stu-id="f9c59-132">Allocating an array based soley on the assumption that some number of elements will follow would be a potential attack vector.</span></span> <span data-ttu-id="f9c59-133">在此情況下，讀取器的使用者應該改為在專案出現時以累加方式配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="f9c59-133">The user of the reader in this case should instead incrementally allocate the memory as the elements appear.</span></span>

<span data-ttu-id="f9c59-134">XML 讀取器不支援 DTD。</span><span class="sxs-lookup"><span data-stu-id="f9c59-134">XML reader does not support DTD.</span></span> <span data-ttu-id="f9c59-135">讀者的使用者不需要考慮 DTD 驗證。</span><span class="sxs-lookup"><span data-stu-id="f9c59-135">The user of the reader does not need to concern about DTD verification.</span></span>

<span data-ttu-id="f9c59-136">下列回呼適用于 XML 讀取器：</span><span class="sxs-lookup"><span data-stu-id="f9c59-136">The following callback is used with XML readers:</span></span>

-   [<span data-ttu-id="f9c59-137">**WS \_ 讀取 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="f9c59-137">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

<span data-ttu-id="f9c59-138">下列列舉適用于 XML 讀取器：</span><span class="sxs-lookup"><span data-stu-id="f9c59-138">The following enumerations are used with XML readers:</span></span>

-   [<span data-ttu-id="f9c59-139">**WS \_ XML \_ 讀取器 \_ 編碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f9c59-139">**WS\_XML\_READER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="f9c59-140">**WS \_ XML \_ 讀取器 \_ 輸入 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f9c59-140">**WS\_XML\_READER\_INPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [<span data-ttu-id="f9c59-141">**WS \_ XML \_ 讀取器 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f9c59-141">**WS\_XML\_READER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="f9c59-142">下列函式適用于 XML 讀取器：</span><span class="sxs-lookup"><span data-stu-id="f9c59-142">The following functions are used with XML readers:</span></span>

-   [<span data-ttu-id="f9c59-143">**WsCreateReader**</span><span class="sxs-lookup"><span data-stu-id="f9c59-143">**WsCreateReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [<span data-ttu-id="f9c59-144">**WsFillReader**</span><span class="sxs-lookup"><span data-stu-id="f9c59-144">**WsFillReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [<span data-ttu-id="f9c59-145">**WsFindAttribute**</span><span class="sxs-lookup"><span data-stu-id="f9c59-145">**WsFindAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [<span data-ttu-id="f9c59-146">**WsFreeReader**</span><span class="sxs-lookup"><span data-stu-id="f9c59-146">**WsFreeReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [<span data-ttu-id="f9c59-147">**WsGetNamespaceFromPrefix**</span><span class="sxs-lookup"><span data-stu-id="f9c59-147">**WsGetNamespaceFromPrefix**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [<span data-ttu-id="f9c59-148">**WsGetReaderNode**</span><span class="sxs-lookup"><span data-stu-id="f9c59-148">**WsGetReaderNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [<span data-ttu-id="f9c59-149">**WsGetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="f9c59-149">**WsGetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [<span data-ttu-id="f9c59-150">**WsGetReaderProperty**</span><span class="sxs-lookup"><span data-stu-id="f9c59-150">**WsGetReaderProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [<span data-ttu-id="f9c59-151">**WsGetXmlAttribute**</span><span class="sxs-lookup"><span data-stu-id="f9c59-151">**WsGetXmlAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [<span data-ttu-id="f9c59-152">**WsMoveReader**</span><span class="sxs-lookup"><span data-stu-id="f9c59-152">**WsMoveReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [<span data-ttu-id="f9c59-153">**WsReadArray**</span><span class="sxs-lookup"><span data-stu-id="f9c59-153">**WsReadArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [<span data-ttu-id="f9c59-154">**WsReadBytes**</span><span class="sxs-lookup"><span data-stu-id="f9c59-154">**WsReadBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [<span data-ttu-id="f9c59-155">**WsReadChars**</span><span class="sxs-lookup"><span data-stu-id="f9c59-155">**WsReadChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [<span data-ttu-id="f9c59-156">**WsReadCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="f9c59-156">**WsReadCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [<span data-ttu-id="f9c59-157">**WsReadEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="f9c59-157">**WsReadEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [<span data-ttu-id="f9c59-158">**WsReadEndElement**</span><span class="sxs-lookup"><span data-stu-id="f9c59-158">**WsReadEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [<span data-ttu-id="f9c59-159">**WsReadNode**</span><span class="sxs-lookup"><span data-stu-id="f9c59-159">**WsReadNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [<span data-ttu-id="f9c59-160">**WsReadQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="f9c59-160">**WsReadQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [<span data-ttu-id="f9c59-161">**WsReadStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="f9c59-161">**WsReadStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [<span data-ttu-id="f9c59-162">**WsReadStartElement**</span><span class="sxs-lookup"><span data-stu-id="f9c59-162">**WsReadStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [<span data-ttu-id="f9c59-163">**WsReadToStartElement**</span><span class="sxs-lookup"><span data-stu-id="f9c59-163">**WsReadToStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [<span data-ttu-id="f9c59-164">**WsReadValue**</span><span class="sxs-lookup"><span data-stu-id="f9c59-164">**WsReadValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [<span data-ttu-id="f9c59-165">**WsSetInput**</span><span class="sxs-lookup"><span data-stu-id="f9c59-165">**WsSetInput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [<span data-ttu-id="f9c59-166">**WsSetInputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="f9c59-166">**WsSetInputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [<span data-ttu-id="f9c59-167">**WsSetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="f9c59-167">**WsSetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [<span data-ttu-id="f9c59-168">**WsSkipNode**</span><span class="sxs-lookup"><span data-stu-id="f9c59-168">**WsSkipNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

<span data-ttu-id="f9c59-169">下列控制碼會搭配 XML 讀取器使用：</span><span class="sxs-lookup"><span data-stu-id="f9c59-169">The following handle is used with XML readers:</span></span>

-   [<span data-ttu-id="f9c59-170">WS \_ XML \_ 讀取器</span><span class="sxs-lookup"><span data-stu-id="f9c59-170">WS\_XML\_READER</span></span>](ws-xml-reader.md)

<span data-ttu-id="f9c59-171">下列結構適用于 XML 讀取器：</span><span class="sxs-lookup"><span data-stu-id="f9c59-171">The following structures are used with XML readers:</span></span>

-   [<span data-ttu-id="f9c59-172">**WS \_ XML \_ 讀取器 \_ 二進位 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="f9c59-172">**WS\_XML\_READER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [<span data-ttu-id="f9c59-173">**WS \_ XML \_ 讀取器 \_ 緩衝區 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="f9c59-173">**WS\_XML\_READER\_BUFFER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="f9c59-174">**WS \_ XML \_ 讀取器 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="f9c59-174">**WS\_XML\_READER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [<span data-ttu-id="f9c59-175">**WS \_ XML \_ 讀取器 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="f9c59-175">**WS\_XML\_READER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [<span data-ttu-id="f9c59-176">**WS \_ XML \_ 讀取器 \_ MTOM \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="f9c59-176">**WS\_XML\_READER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [<span data-ttu-id="f9c59-177">**WS \_ XML \_ 讀取器 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="f9c59-177">**WS\_XML\_READER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [<span data-ttu-id="f9c59-178">**WS \_ XML \_ 讀取器 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="f9c59-178">**WS\_XML\_READER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [<span data-ttu-id="f9c59-179">**WS \_ XML \_ 讀取器 \_ 資料流程 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="f9c59-179">**WS\_XML\_READER\_STREAM\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [<span data-ttu-id="f9c59-180">**WS \_ XML \_ 讀取器 \_ 文字 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="f9c59-180">**WS\_XML\_READER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




