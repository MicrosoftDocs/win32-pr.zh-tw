---
title: Media-Type 協商
description: 許多應用層網際網路通訊協定是以簡單、彈性的格式（稱為多用途網際網路郵件延伸 (MIME) ）作為基礎來交換訊息。
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb145fa3a76da6574172ddd24888f3b5da7ad85e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382978"
---
# <a name="media-type-negotiation"></a><span data-ttu-id="6cb75-103">Media-Type 協商</span><span class="sxs-lookup"><span data-stu-id="6cb75-103">Media-Type Negotiation</span></span>

<span data-ttu-id="6cb75-104">許多應用層網際網路通訊協定是以簡單、彈性的格式（稱為多用途網際網路郵件延伸 (MIME) ）作為基礎來交換訊息。</span><span class="sxs-lookup"><span data-stu-id="6cb75-104">Many application-layer Internet protocols are based on the exchange of messages in a simple, flexible format called Multipurpose Internet Mail Extensions (MIME).</span></span> <span data-ttu-id="6cb75-105">雖然 MIME 是以交換電子郵件訊息的標準來產生的，但目前由各種不同的應用程式使用，以指定以 MIME 或媒體類型表示的相互理解資料格式。</span><span class="sxs-lookup"><span data-stu-id="6cb75-105">Although MIME originated as a standard for exchanging electronic mail messages, it is used today by a wide variety of applications to specify mutually understood data formats as MIME, or media, types.</span></span> <span data-ttu-id="6cb75-106">此程式稱為 *媒體類型的協商*。</span><span class="sxs-lookup"><span data-stu-id="6cb75-106">The process is called *media-type negotiation*.</span></span>

<span data-ttu-id="6cb75-107">媒體類型是表示類型和子類型 (的簡單字串，例如 "text/純文字" 或 "text/HTML" ) 。</span><span class="sxs-lookup"><span data-stu-id="6cb75-107">Media types are simple strings that denote a type and subtype (such as "text/plain" or "text/HTML").</span></span> <span data-ttu-id="6cb75-108">它們可用來標記資料或限定要求。</span><span class="sxs-lookup"><span data-stu-id="6cb75-108">They are used to label data or qualify a request.</span></span> <span data-ttu-id="6cb75-109">例如，網頁瀏覽器（例如，HTTP 要求資料或要求資訊的一部分）指定要求「影像/gif」或「影像/jpeg」媒體類型，而網頁伺服器會藉由傳回適當的媒體類型來回應該媒體類型，如果呼叫是要求的資料，則是要求格式的資料本身。</span><span class="sxs-lookup"><span data-stu-id="6cb75-109">A Web browser, for example, as part of an HTTP request-for-data or request-for-info, specifies that it is requesting "image/gif" or "image/jpeg" Media Types, to which a web server responds by returning the appropriate media type and, if the call was a request-for-data, the data itself in the requested format.</span></span>

<span data-ttu-id="6cb75-110">媒體類型的協商通常類似于現有的桌面應用程式如何與系統剪貼簿協調，以決定當使用者在拖放作業期間，于接收 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 指標時選擇編輯/貼上或查詢格式時要貼上的資料格式。</span><span class="sxs-lookup"><span data-stu-id="6cb75-110">Media-type negotiation is often similar to how existing desktop applications negotiate with the system clipboard to determine which data format to paste when a user chooses Edit/Paste or queries for formats when receiving an [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) pointer during a drag-and-drop operation.</span></span> <span data-ttu-id="6cb75-111">HTTP 媒體型別協商的微妙差異在於，用戶端事先不知道伺服器可以使用的格式。</span><span class="sxs-lookup"><span data-stu-id="6cb75-111">The subtle difference in HTTP media-type negotiation is that the client does not know ahead of time which formats the server has available.</span></span> <span data-ttu-id="6cb75-112">因此，用戶端會以最精確的精確度來指定支援的媒體類型，而伺服器會以最佳的可用格式來回應。</span><span class="sxs-lookup"><span data-stu-id="6cb75-112">Therefore, the client specifies up-front the media types it supports, in order of greatest fidelity, and the server responds with the best available format.</span></span>

<span data-ttu-id="6cb75-113">URL 標記可支援媒體類型的協商，讓網際網路用戶端和伺服器同意在 [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 作業中下載資料時使用的格式。</span><span class="sxs-lookup"><span data-stu-id="6cb75-113">URL monikers support media-type negotiation as a way for Internet clients and servers to agree upon formats to be used when downloading data in [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operations.</span></span> <span data-ttu-id="6cb75-114">為了支援媒體類型的協商，用戶端會執行 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) 介面，並呼叫 [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) 函式來向系結內容註冊。</span><span class="sxs-lookup"><span data-stu-id="6cb75-114">To support media-type negotiation, a client implements the [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) interface and calls the [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) function to register it with the bind context.</span></span> <span data-ttu-id="6cb75-115">格式列舉值會列出用戶端可以接受的格式。</span><span class="sxs-lookup"><span data-stu-id="6cb75-115">The format enumerator lists the formats the client can accept.</span></span> <span data-ttu-id="6cb75-116">當系結至 HTTP Url 時，URL 標記會將這些格式轉譯為媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb75-116">A URL moniker translates these formats into media types when binding to HTTP URLs.</span></span>

<span data-ttu-id="6cb75-117">用戶端要求的可能媒體類型會透過系結內容上呼叫端所註冊之 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc)列舉值中所提供的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構，向 URL 名字值表示：每個 **FORMATETC** 都會指定可識別媒體類型的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="6cb75-117">The possible media types requested by the client are represented to URL monikers through [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structures available from the [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) enumerator registered by the caller on the bind context: Each **FORMATETC** specifies a clipboard format identifying the media type.</span></span> <span data-ttu-id="6cb75-118">例如，下列程式碼片段會將媒體類型指定為 PostScript。</span><span class="sxs-lookup"><span data-stu-id="6cb75-118">For example, the following code fragment specifies that the media type is PostScript.</span></span>

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

<span data-ttu-id="6cb75-119">用戶端可以將剪貼簿格式設定為特殊媒體類型 CF \_ Null，以指出應抓取 URL 所指向之資源的預設媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb75-119">A client can set the clipboard format to the special media type CF\_NULL to indicate that the default media type of the resource pointed to by the URL should be retrieved.</span></span> <span data-ttu-id="6cb75-120">這種格式通常是用戶端感興趣的最後一種格式。</span><span class="sxs-lookup"><span data-stu-id="6cb75-120">This format is usually the last one in which the client is interested.</span></span> <span data-ttu-id="6cb75-121">如果沒有向系結內容註冊列舉值，URL 的名字會像是包含具有 **cfFormat**= CF Null 之單一 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)的列舉值 \_ 可供使用，並自動下載預設媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb75-121">When no enumerator is registered with the bind context, a URL moniker works as if an enumerator containing a single [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) with **cfFormat**=CF\_NULL is available, automatically downloading the default media-type.</span></span>

<span data-ttu-id="6cb75-122">無論使用哪種類型的媒體類型，用戶端都會透過其 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))方法上的 *pformatetc* 引數來通知選擇。</span><span class="sxs-lookup"><span data-stu-id="6cb75-122">Whatever media type is to be used, the client is notified of the choice by means of the *pformatetc* argument on its [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) method.</span></span> <span data-ttu-id="6cb75-123">回呼會發生在用戶端呼叫 [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage)的內容中。</span><span class="sxs-lookup"><span data-stu-id="6cb75-123">The callback occurs within the context of the client's call to [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).</span></span>

> [!Note]  
> <span data-ttu-id="6cb75-124">如果接收的內容是無法辨識的媒體類型，用戶端會自動呼叫 [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) 來註冊新的類型。</span><span class="sxs-lookup"><span data-stu-id="6cb75-124">If received content is of an unrecognized media-type, the client automatically calls [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) to register the new type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6cb75-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="6cb75-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb75-126">URL 的名字</span><span class="sxs-lookup"><span data-stu-id="6cb75-126">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 