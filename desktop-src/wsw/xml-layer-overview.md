---
title: XML 層總覽
description: WWSAPI 中的 XML API 是以 XML 讀取器和 XML 寫入器物件為基礎，允許以順向方式讀取或寫入 XML 檔。 XML 層可讓應用程式完整存取和控制訊息的內容。
ms.assetid: 938ca257-fbb8-4569-b791-2148abb1a5a5
keywords:
- XML 層級總覽 Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d062754adea7b48bd42a6a501ce17d0e332b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673339"
---
# <a name="xml-layer-overview"></a><span data-ttu-id="af243-107">XML 層總覽</span><span class="sxs-lookup"><span data-stu-id="af243-107">XML Layer Overview</span></span>

<span data-ttu-id="af243-108">WWSAPI 中的 XML API 是以 [Xml 讀取器](xml-reader.md) 和 [xml 寫入器](xml-writer.md) 物件為基礎，允許以順向方式讀取或寫入 xml 檔。</span><span class="sxs-lookup"><span data-stu-id="af243-108">The XML API in WWSAPI is based on the [XML Reader](xml-reader.md) and [XML Writer](xml-writer.md) objects, which allow reading or writing of XML documents in a forward only fashion.</span></span> <span data-ttu-id="af243-109">XML 層可讓應用程式完整存取和控制訊息的內容。</span><span class="sxs-lookup"><span data-stu-id="af243-109">The XML Layer give the application full access to and control over the content of messages.</span></span>

## <a name="encoding"></a><span data-ttu-id="af243-110">編碼</span><span class="sxs-lookup"><span data-stu-id="af243-110">Encoding</span></span>

<span data-ttu-id="af243-111">XML API 支援編碼為的檔：</span><span class="sxs-lookup"><span data-stu-id="af243-111">The XML API supports documents encoded as:</span></span>

-   <span data-ttu-id="af243-112">文字 (UTF-8、UTF-16 UTF-16LE、UTF-16) </span><span class="sxs-lookup"><span data-stu-id="af243-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span></span>
-   <span data-ttu-id="af243-113">Binary</span><span class="sxs-lookup"><span data-stu-id="af243-113">Binary</span></span>
-   <span data-ttu-id="af243-114">MTOM</span><span class="sxs-lookup"><span data-stu-id="af243-114">MTOM</span></span>

## <a name="storage"></a><span data-ttu-id="af243-115">儲存體</span><span class="sxs-lookup"><span data-stu-id="af243-115">Storage</span></span>

<span data-ttu-id="af243-116">XML API 支援處理儲存為的檔：</span><span class="sxs-lookup"><span data-stu-id="af243-116">The XML API supports processing documents stored as:</span></span>

-   <span data-ttu-id="af243-117">編碼位元組的記憶體中緩衝區</span><span class="sxs-lookup"><span data-stu-id="af243-117">An in-memory buffer of encoded bytes</span></span>
-   <span data-ttu-id="af243-118">資料流程</span><span class="sxs-lookup"><span data-stu-id="af243-118">A stream</span></span>
-   <span data-ttu-id="af243-119">[XML 緩衝區](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="af243-119">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="af243-120">[Xml 緩衝區](xml-buffer.md)是 xml 檔的結構化記憶體中標記法。</span><span class="sxs-lookup"><span data-stu-id="af243-120">An [XML Buffer](xml-buffer.md) is a structured in-memory representation of an XML document.</span></span> <span data-ttu-id="af243-121">這是比編碼為位元組的檔更有效率的標記法。</span><span class="sxs-lookup"><span data-stu-id="af243-121">This is a more efficient representation than a document encoded as bytes.</span></span> <span data-ttu-id="af243-122">您可以流覽、讀取或寫入儲存在 XML 緩衝區中的 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="af243-122">An XML document stored in an An XML Buffer can be navigated, read, or written.</span></span>

## <a name="io"></a><span data-ttu-id="af243-123">I/O</span><span class="sxs-lookup"><span data-stu-id="af243-123">I/O</span></span>

<span data-ttu-id="af243-124">除非特別要求，否則 XML API 永遠不會執行 i/o。</span><span class="sxs-lookup"><span data-stu-id="af243-124">The XML API will never perform I/O unless specifically requested.</span></span> <span data-ttu-id="af243-125">此外，任何 i/o 都可能以非同步方式起始。</span><span class="sxs-lookup"><span data-stu-id="af243-125">Furthermore, any I/O may be initiated in an asynchronous fashion.</span></span> <span data-ttu-id="af243-126">如需有關使用 XML API 進行非同步處理的詳細資訊，請參閱 [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) 和 [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) 。</span><span class="sxs-lookup"><span data-stu-id="af243-126">See [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) and [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) for details on asynchronous processing with the XML API.</span></span>

## <a name="processing"></a><span data-ttu-id="af243-127">Processing</span><span class="sxs-lookup"><span data-stu-id="af243-127">Processing</span></span>

<span data-ttu-id="af243-128">XML API 有三個不同的層級，可處理檔。</span><span class="sxs-lookup"><span data-stu-id="af243-128">The XML API has three distinct levels at which the document may be processed.</span></span>

<span data-ttu-id="af243-129">一次可以處理一個 [**節點**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) 的檔。</span><span class="sxs-lookup"><span data-stu-id="af243-129">A document may be processed a [**node**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) at a time.</span></span> <span data-ttu-id="af243-130">這可提供最精細的 XML 內容處理，並提供檔完整的資料精確度。</span><span class="sxs-lookup"><span data-stu-id="af243-130">This offers the most fine-grained handling of the XML content, and provides complete fidelity of data from the document.</span></span> <span data-ttu-id="af243-131">在此層級，將會使用 [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) 和 [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) 和 [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) 函式。</span><span class="sxs-lookup"><span data-stu-id="af243-131">At this level, the functions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) and [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) and [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) would be used.</span></span>

<span data-ttu-id="af243-132">下一個控制層級是 Api，例如 [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)、 [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) 和 [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)。</span><span class="sxs-lookup"><span data-stu-id="af243-132">The next level of control are APIs like [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) and [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span></span> <span data-ttu-id="af243-133">這些 Api 提供許多類型的驗證、略過空白字元和批註，以及將文字和 CDATA 標準化，讓取用者以更簡單的 xml 觀點呈現。</span><span class="sxs-lookup"><span data-stu-id="af243-133">These APIs provide numerous kinds of validation, skip whitespace and comments, and normalize text and CDATA to present the consumer with a simpler view of the xml.</span></span>

<span data-ttu-id="af243-134">最高層級的控制是使用序列化 API。</span><span class="sxs-lookup"><span data-stu-id="af243-134">The highest level of control is to use the Serialization API.</span></span> <span data-ttu-id="af243-135">這些 Api 是由 C 資料類型與 XML 之間的對應所驅動，而且可以使用單一函式（例如 [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) 和 [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)），將複雜的記憶體內部結構讀取或寫入至 xml。</span><span class="sxs-lookup"><span data-stu-id="af243-135">These APIs are driven off a mapping between C data types and XML, and can read or write a complex in-memory structure to xml and back with a single function like [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) and [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span></span>

<span data-ttu-id="af243-136">XML 正常化 Api 可用來產生標準格式的 XML，該格式可能會被用來透過 XML 內容產生密碼編譯簽章。</span><span class="sxs-lookup"><span data-stu-id="af243-136">The XML Canonicalization APIs may be used to generate a canonical form of XML which may in turn be used for generating cryptographic signatures over XML content.</span></span>

## <a name="creating-a-writer"></a><span data-ttu-id="af243-137">建立寫入器</span><span class="sxs-lookup"><span data-stu-id="af243-137">Creating a writer</span></span>

<span data-ttu-id="af243-138">若要建立並使用寫入器來寫入記憶體中的緩衝區：</span><span class="sxs-lookup"><span data-stu-id="af243-138">To create and use a writer to write to an in-memory buffer:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_BUFFER_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsGetWriterProperty(..., WS_XML_WRITER_PROPERTY_BYTES, ...)  // Get the generated bytes as a single byte array
// Use the generated bytes
WsFreeWriter                // Free the writer
```

<span data-ttu-id="af243-139">若要建立並使用寫入器寫入資料流程：</span><span class="sxs-lookup"><span data-stu-id="af243-139">To create and use a writer to write to a stream:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_STREAM_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsFlushWriter               // Force any buffered data to be written
WsFreeWriter                // Free the writer
```

<span data-ttu-id="af243-140">若要建立並使用寫入器來寫入 [WS \_ XML \_ 緩衝區](ws-xml-buffer.md)：</span><span class="sxs-lookup"><span data-stu-id="af243-140">To create and use a writer to write to a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateWriter              // Create an instance of a WS_XML_WRITER
WsSetOutputToBuffer         // Set the output buffer along with any other writer properties
// Write Elements
WsFreeWriter                // Free the writer
// The buffer has the generated document
```

<span data-ttu-id="af243-141">在所有情況下，可能會包含屬性 [**WS \_ xml \_ 寫入器 \_ 屬性 \_ 縮排**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) 來格式化 XML。</span><span class="sxs-lookup"><span data-stu-id="af243-141">In all cases, the property [**WS\_XML\_WRITER\_PROPERTY\_INDENT**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) may be included to format the xml.</span></span>

## <a name="writing-elements"></a><span data-ttu-id="af243-142">寫入項目</span><span class="sxs-lookup"><span data-stu-id="af243-142">Writing Elements</span></span>

<span data-ttu-id="af243-143">若要將元素寫入寫入器：</span><span class="sxs-lookup"><span data-stu-id="af243-143">To write an element to a writer:</span></span>

``` syntax
WsWriteStartElement          // Write a start element
for each attribute
{
// Write an attribute using either
WsWriteStartAttribute    // Write a start attribute
// Write Content
WsWriteEndAttribute      // Write an end attribute
// Or one of the following
WsWriteXmlnsAttribute    // Write an explicit xmlns attribute
}
// Write Elements or Content
WsWriteEndElement
```

<span data-ttu-id="af243-144">也可以使用下列各項：</span><span class="sxs-lookup"><span data-stu-id="af243-144">The following may also be used:</span></span>

``` syntax
WsWriteArray                 // Write an array of primitive values as a series of repeated elements
```

## <a name="writing-content"></a><span data-ttu-id="af243-145">寫入內容</span><span class="sxs-lookup"><span data-stu-id="af243-145">Writing Content</span></span>

<span data-ttu-id="af243-146">若要將內容寫入專案或屬性，您可以使用下列專案：</span><span class="sxs-lookup"><span data-stu-id="af243-146">To write content to an element or attribute, the following may be used:</span></span>

``` syntax
WsWriteChars                 // Write unicode characters from memory
WsWriteCharsUtf8             // Write UTF-8 encoded characters from memory
WsWriteBytes                 // Write binary data encoded as base64
WsPushBytes                  // Direct the writer to request that bytes be written
WsPullBytes                  // Direct the writer to read the bytes to be written
WsWriteValue                 // Write primitive values such as ints and BOOLs
WsWriteText                  // Write an WS_XML_TEXT
WsWriteQualifiedName         // Write a qualified name
```

<span data-ttu-id="af243-147">您可以使用下列程式寫入檔，但在屬性中時可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="af243-147">The following can be used to write to a document, but may not be used when within an attribute.</span></span>

``` syntax
WsWriteNode                  // Write a single WS_XML_NODE
WsCopyNode                   // Copy a single node, or an entire WS_XML_ELEMENT_NODE and children from an WS_XML_READER
```

<span data-ttu-id="af243-148">您可以使用下列內容在文字檔中撰寫 CDATA 區段：</span><span class="sxs-lookup"><span data-stu-id="af243-148">The following may be used to write a CDATA section in a text document:</span></span>

``` syntax
WsWriteStartCData            // Start a CDATA section in a text encoding
// Write Content
WsWriteEndCData              // End a CDATA section in text encoding
```

## <a name="miscellaneous"></a><span data-ttu-id="af243-149">其他</span><span class="sxs-lookup"><span data-stu-id="af243-149">Miscellaneous</span></span>

``` syntax
WsGetPrefixFromNamespace     // Find a prefix bound to a namespace
```

## <a name="creating-a-reader"></a><span data-ttu-id="af243-150">建立讀取器</span><span class="sxs-lookup"><span data-stu-id="af243-150">Creating a reader</span></span>

<span data-ttu-id="af243-151">若要建立並使用讀取器來讀取記憶體中的緩衝區：</span><span class="sxs-lookup"><span data-stu-id="af243-151">To create and use a reader to read from an in-memory buffer:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="af243-152">若要從資料流程建立讀取器並使用讀取器：</span><span class="sxs-lookup"><span data-stu-id="af243-152">To create and use a reader to reader from a stream:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_STREAM_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
WsFillReader                // Populate the reader with data from the underlying stream
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="af243-153">若要建立及使用讀取器來讀取 [WS \_ XML \_ 緩衝區](ws-xml-buffer.md)：</span><span class="sxs-lookup"><span data-stu-id="af243-153">To create and use a reader to read from a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateReader              // Create an instance of a WS_XML_READER
WsSetInputToBuffer          // Set the input buffer along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

## <a name="reading-elements"></a><span data-ttu-id="af243-154">讀取項目</span><span class="sxs-lookup"><span data-stu-id="af243-154">Reading Elements</span></span>

<span data-ttu-id="af243-155">從讀取器讀取元素：</span><span class="sxs-lookup"><span data-stu-id="af243-155">To read an element from a reader:</span></span>

``` syntax
WsReadToStartElement         // Skip whitespace and comments to position the reader on a specific element
for each attribute of interest
{
WsFindAttribute          // Try Locate the attribute
if (found)
{
WsReadStartAttribute // Set the reader to read the attribute
// Read Content
WsReadEndAttribute   // Return the reader to the element
}
}
WsReadStartElement           // Advance the reader past the current element
// Read Elements or Content
WsWriteEndElement            // Advance the reader past the corresponding end element
```

<span data-ttu-id="af243-156">也可以使用下列各項：</span><span class="sxs-lookup"><span data-stu-id="af243-156">The following may also be used:</span></span>

``` syntax
WsReadArray                  // Read an array of primitive values as a series of repeated elements
```

## <a name="reading-content"></a><span data-ttu-id="af243-157">讀取內容</span><span class="sxs-lookup"><span data-stu-id="af243-157">Reading Content</span></span>

<span data-ttu-id="af243-158">若要讀取元素或屬性中的內容，可以使用下列專案：</span><span class="sxs-lookup"><span data-stu-id="af243-158">To read content from an element or attribute, the following may be used:</span></span>

``` syntax
WsReadChars                 // Read characters to memory as unicode
WsReadCharsUtf8             // Read characters to memory encoded as UTF-8
WsReadBytes                 // Read binary data encoded as base64
WsReadValue                 // Read primitive values such as ints and BOOLs
WsReadQualifiedName         // Read a qualified name
```

<span data-ttu-id="af243-159">您可以使用下列程式來檢查讀取器所在的目前節點：</span><span class="sxs-lookup"><span data-stu-id="af243-159">The following may be used to inspect the current node the reader is positioned on:</span></span>

``` syntax
WsGetReaderNode             // Get the current node
```

## <a name="using-a-buffer"></a><span data-ttu-id="af243-160">使用緩衝區</span><span class="sxs-lookup"><span data-stu-id="af243-160">Using a buffer</span></span>

<span data-ttu-id="af243-161">寫入至 [WS \_ XML \_ 緩衝區](ws-xml-buffer.md) 時，可能會使用下列各項：</span><span class="sxs-lookup"><span data-stu-id="af243-161">When writing to a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetWriterPosition          // Get the current position of the writer in the document
WsSetWriterPosition          // Set the current position of the writer in the document
WsMoveWriter                 // Move relative to the current position in the document
WsRemoveNode                 // Delete an element or text from a document
```

<span data-ttu-id="af243-162">從 [WS \_ XML \_ 緩衝區](ws-xml-buffer.md) 讀取時，可能會使用下列各項：</span><span class="sxs-lookup"><span data-stu-id="af243-162">When reading from a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetReaderPosition          // Get the current position of the reader in the document
WsSetReaderPosition          // Set the current position of the reader in the document
WsMoveReader                 // Move relative to the current position in the document
```

<span data-ttu-id="af243-163">您可以使用下列來修改 [WS \_ XML \_ 緩衝區](ws-xml-buffer.md)：</span><span class="sxs-lookup"><span data-stu-id="af243-163">The following may be used to modify a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax

WsRemoveNode                 // Delete an element or text from a document
```

## <a name="other"></a><span data-ttu-id="af243-164">其他</span><span class="sxs-lookup"><span data-stu-id="af243-164">Other</span></span>

``` syntax
WsGetNamespaceFromPrefix     // Find a namespace bound to a prefix
WsGetXmlAttribute            // Find an "xml:space" or "xml:lang" attribute in scope
```

 

 




