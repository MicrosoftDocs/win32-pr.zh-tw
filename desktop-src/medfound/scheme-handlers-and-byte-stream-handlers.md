---
description: 本主題說明來源解析程式如何建立媒體來源的內部詳細資料。
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: 配置處理常式和 Byte-Stream 處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998263"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a><span data-ttu-id="181ac-103">配置處理常式和 Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="181ac-103">Scheme Handlers and Byte-Stream Handlers</span></span>

<span data-ttu-id="181ac-104">本主題說明來源解析程式如何建立媒體來源的內部詳細資料。</span><span class="sxs-lookup"><span data-stu-id="181ac-104">This topic describes the internal details of how the source resolver creates a media source.</span></span> <span data-ttu-id="181ac-105">如果您要為媒體基礎執行自訂媒體來源，而且想要透過來源解析程式將媒體來源提供給應用程式，請閱讀本主題。</span><span class="sxs-lookup"><span data-stu-id="181ac-105">Read this topic if you are implementing a custom media source for Media Foundation, and you want the media source to be available to applications via the source resolver.</span></span>

<span data-ttu-id="181ac-106">來源解析程式可以從 URL 或位元組資料流程建立媒體來源 (也就是 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 指標) 。</span><span class="sxs-lookup"><span data-stu-id="181ac-106">The source resolver can create a media source from a URL or from a byte stream (that is, an [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) pointer).</span></span> <span data-ttu-id="181ac-107">若要這樣做，它會使用稱為 *處理常式* 的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="181ac-107">To do so, it uses helper objects called *handlers*.</span></span> <span data-ttu-id="181ac-108">針對 Url，來源解析程式會使用 *配置處理常式*。</span><span class="sxs-lookup"><span data-stu-id="181ac-108">For URLs, the source resolver uses *scheme handlers*.</span></span> <span data-ttu-id="181ac-109">若為位元組資料流程，它會使用 *位元組資料流程處理常式*。</span><span class="sxs-lookup"><span data-stu-id="181ac-109">For byte streams, it uses *byte-stream handlers*.</span></span>

<span data-ttu-id="181ac-110">配置處理常式會使用 URL 做為輸入，並建立媒體來源或位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="181ac-110">A scheme handler takes a URL as input and creates either a media source or a byte stream.</span></span> <span data-ttu-id="181ac-111">如果建立位元組資料流程，來源解析程式會將它傳遞至位元組資料流程處理常式，該處理常式會建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="181ac-111">If it creates a byte stream, the source resolver will pass that to a byte-stream handler, which creates the media source.</span></span> <span data-ttu-id="181ac-112">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="181ac-112">The following image illustrates this process.</span></span>

![顯示來源解析流程的圖表](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a><span data-ttu-id="181ac-114">配置處理常式</span><span class="sxs-lookup"><span data-stu-id="181ac-114">Scheme Handlers</span></span>

<span data-ttu-id="181ac-115">當應用程式呼叫 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 或它的非同步對等專案 [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)時，會使用配置處理常式。</span><span class="sxs-lookup"><span data-stu-id="181ac-115">Scheme handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) or its asynchronous equivalent, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

<span data-ttu-id="181ac-116">來源解析程式會在登錄中查看配置處理常式。</span><span class="sxs-lookup"><span data-stu-id="181ac-116">The source resolver looks up scheme handlers in the registry.</span></span> <span data-ttu-id="181ac-117">配置處理常式會依 URL 配置列在下列機碼底下：</span><span class="sxs-lookup"><span data-stu-id="181ac-117">Scheme handlers are listed by URL scheme, under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="181ac-118">其中 *<scheme>* 是處理常式設計來剖析的 URL 配置。</span><span class="sxs-lookup"><span data-stu-id="181ac-118">where *<scheme>* is the URL scheme that the handler is designed to parse.</span></span> <span data-ttu-id="181ac-119">配置包含尾端的 '： ' 字元;例如，"HTTP："。</span><span class="sxs-lookup"><span data-stu-id="181ac-119">The scheme includes the trailing ':' character; for example, "http:".</span></span>

<span data-ttu-id="181ac-120">若要註冊新的配置處理常式，請新增名稱為配置處理常式 CLSID 的專案，其名稱為標準字串格式： `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` 。</span><span class="sxs-lookup"><span data-stu-id="181ac-120">To register a new scheme handler, add an entry whose name is the CLSID of the scheme handler, in canonical string form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="181ac-121">專案的值是字串 (REG \_ SZ) 包含處理常式的簡短描述，例如「我的配置處理常式」。</span><span class="sxs-lookup"><span data-stu-id="181ac-121">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Scheme Handler."</span></span> <span data-ttu-id="181ac-122">專案的重要部分是 CLSID。</span><span class="sxs-lookup"><span data-stu-id="181ac-122">The important part of the entry is the CLSID.</span></span> <span data-ttu-id="181ac-123">來源解析程式會使用此 CLSID 呼叫 **CoCreateInstance** 來建立處理常式。</span><span class="sxs-lookup"><span data-stu-id="181ac-123">The source resolver creates the handler by calling **CoCreateInstance** with this CLSID.</span></span>

<span data-ttu-id="181ac-124">配置處理常式會公開 [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) 介面。</span><span class="sxs-lookup"><span data-stu-id="181ac-124">Scheme handlers expose the [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) interface.</span></span> <span data-ttu-id="181ac-125">如果來源解析程式找到符合 URL 配置的配置處理常式，來源解析程式就會呼叫 [**IMFSchemeHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)，並傳入原始 url。</span><span class="sxs-lookup"><span data-stu-id="181ac-125">If the source resolver finds a scheme handler that matches the URL scheme, the source resolver calls [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passing in the original URL.</span></span> <span data-ttu-id="181ac-126">配置處理常式會開啟 URL，並嘗試剖析內容。</span><span class="sxs-lookup"><span data-stu-id="181ac-126">The scheme handler will open the URL and attempt to parse the contents.</span></span> <span data-ttu-id="181ac-127">這時，配置處理常式有兩個選項：</span><span class="sxs-lookup"><span data-stu-id="181ac-127">At that point, the scheme handler has two options:</span></span>

-   <span data-ttu-id="181ac-128">建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="181ac-128">Create a media source.</span></span>
-   <span data-ttu-id="181ac-129">建立位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="181ac-129">Create a byte stream.</span></span>

<span data-ttu-id="181ac-130">如果它建立媒體來源，則來源解析程式會將媒體來源傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="181ac-130">If it creates a media source, the source resolver returns the media source to the application.</span></span> <span data-ttu-id="181ac-131">如果它建立位元組資料流程，來源解析程式會嘗試尋找適當的位元組資料流程處理常式，如下一節中所述。</span><span class="sxs-lookup"><span data-stu-id="181ac-131">If it creates a byte stream, the source resolver attempts to find an appropriate byte-stream handler, as described in the next section.</span></span>

## <a name="byte-stream-handlers"></a><span data-ttu-id="181ac-132">Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="181ac-132">Byte-Stream Handlers</span></span>

<span data-ttu-id="181ac-133">當應用程式呼叫 [**IMFSourceResolver：： CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) 或它的非同步對等專案 [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)時，會使用位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="181ac-133">Byte-stream handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) or its asynchronous equivalent, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span></span> <span data-ttu-id="181ac-134">如先前所述，當配置處理常式傳回位元組資料流程時，也會使用它們。</span><span class="sxs-lookup"><span data-stu-id="181ac-134">They are also used when a scheme handler returns a byte stream, as described previously.</span></span>

<span data-ttu-id="181ac-135">如同配置處理常式，位元組資料流程處理常式會列在登錄中。</span><span class="sxs-lookup"><span data-stu-id="181ac-135">As with scheme handlers, byte-stream handlers are listed in the registry.</span></span> <span data-ttu-id="181ac-136">它們會依副檔名或 MIME (類型（) ），在下列機碼底下列出：</span><span class="sxs-lookup"><span data-stu-id="181ac-136">They are listed either by file name extension or MIME type (or both), under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="181ac-137">其中 *<ExtensionOrMimeType>* 是檔案名副檔名或 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="181ac-137">where *<ExtensionOrMimeType>* is the file name extension or MIME type.</span></span> <span data-ttu-id="181ac-138">副檔名包含初始 '. ' 字元;例如，".wmv"。</span><span class="sxs-lookup"><span data-stu-id="181ac-138">File extensions include the initial '.' character; for example, ".wmv".</span></span>

<span data-ttu-id="181ac-139">副檔名是由應用程式提供的 URL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="181ac-139">The file name extension is part of the URL, provided by the application.</span></span> <span data-ttu-id="181ac-140">MIME 類型可透過位元組資料流程上的 [**MF \_ BYTESTREAM \_ 內容 \_ 類型**](mf-bytestream-content-type-attribute.md) 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="181ac-140">The MIME type might be available through the [**MF\_BYTESTREAM\_CONTENT\_TYPE**](mf-bytestream-content-type-attribute.md) attribute on the byte stream.</span></span>

<span data-ttu-id="181ac-141">若要註冊新的位元組資料流程處理常式，請以標準字串格式加入名稱為處理常式 CLSID 的專案。</span><span class="sxs-lookup"><span data-stu-id="181ac-141">To register a new byte-stream handler, add an entry whose name is the CLSID of the handler, in canonical string form.</span></span> <span data-ttu-id="181ac-142">專案的值是字串 (REG \_ SZ) 包含處理常式的簡短描述，例如「我的 Byte-Stream 處理常式」。</span><span class="sxs-lookup"><span data-stu-id="181ac-142">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Byte-Stream Handler."</span></span> <span data-ttu-id="181ac-143">來源解析程式會呼叫 **CoCreateInstance** 以從 CLSID 建立處理常式。</span><span class="sxs-lookup"><span data-stu-id="181ac-143">The source resolver calls **CoCreateInstance** to create the handler from the CLSID.</span></span> <span data-ttu-id="181ac-144">您可以在一個以上的延伸模組或 MIME 類型中註冊相同的處理常式。</span><span class="sxs-lookup"><span data-stu-id="181ac-144">You can register the same handler under more than one extension or MIME type.</span></span>

<span data-ttu-id="181ac-145">位元組資料流程處理常式會公開 [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) 介面。</span><span class="sxs-lookup"><span data-stu-id="181ac-145">Byte-stream handlers expose the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="181ac-146">如果來源解析程式找到相符的位元組資料流程處理常式，則會呼叫 [**IMFByteStreamHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject)。</span><span class="sxs-lookup"><span data-stu-id="181ac-146">If the source resolver finds a matching byte-stream handler, it calls [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="181ac-147">此方法的輸入是位元組資料流程的指標，以及原始的 URL （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="181ac-147">The input to this method is a pointer to the byte stream, plus the original URL, if available.</span></span> <span data-ttu-id="181ac-148">位元組資料流程處理常式會讀取位元組資料流程，直到它剖析足夠的資料來建立媒體來源為止。</span><span class="sxs-lookup"><span data-stu-id="181ac-148">The byte-stream handler reads from the byte stream until it parses enough data to create the media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="181ac-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="181ac-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="181ac-150">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="181ac-150">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



