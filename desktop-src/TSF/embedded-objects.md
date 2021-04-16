---
title: '内嵌物件 (文字服務架構) '
description: 文字服務架構可讓文字服務將物件內嵌在應用程式文字資料流程中。
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- 文字服務架構 (TSF) 的内嵌物件
- TSF (文字服務架構) ，内嵌物件
- 啟用 TSF 的應用程式，内嵌物件
- 內嵌物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104556833"
---
# <a name="embedded-objects-text-services-framework"></a><span data-ttu-id="0240f-107">内嵌物件 (文字服務架構) </span><span class="sxs-lookup"><span data-stu-id="0240f-107">Embedded Objects (Text Services Framework)</span></span>

<span data-ttu-id="0240f-108">文字服務架構可讓文字服務將物件內嵌在應用程式文字資料流程中。</span><span class="sxs-lookup"><span data-stu-id="0240f-108">Text Services Framework enables a text service to embed objects in an application text stream.</span></span> <span data-ttu-id="0240f-109">内嵌物件會使用值 [TS \_ 字元 \_ 內嵌](ts-char--constants.md)來插入文字資料流程中。</span><span class="sxs-lookup"><span data-stu-id="0240f-109">Embedded objects are inserted into the text stream using the value [TS\_CHAR\_EMBEDDED](ts-char--constants.md).</span></span> <span data-ttu-id="0240f-110">這個值會使用十六進位標記法解析為 Unicode 物件取代字元 U + fffc。</span><span class="sxs-lookup"><span data-stu-id="0240f-110">This value resolves to the Unicode object replacement character U+fffc, using hexadecimal notation.</span></span> <span data-ttu-id="0240f-111">例如，下圖顯示的是代表日文漢字（ *hi*）的内嵌物件轉譯，結合 Unicode 字元序列（代表 "Sun" 的英文翻譯）。</span><span class="sxs-lookup"><span data-stu-id="0240f-111">For example, the following illustration shows the rendering of an embedded object that represents the Japanese ideograph *hi*, in combination with the sequence of Unicode characters that represent the English translation of "Sun."</span></span>

![内嵌物件的字元編碼](images/emb-obj.gif)

<span data-ttu-id="0240f-113">圖頂端的資料列包含翻譯的文字，其中包含 "Sun" 一 *字，後面* 接著 Sun 的日文字元。</span><span class="sxs-lookup"><span data-stu-id="0240f-113">The top row of the figure contains the translated text, consisting of the word "Sun" followed by the Japanese character for sun, *hi*.</span></span> <span data-ttu-id="0240f-114">此圖的中間資料列會顯示 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="0240f-114">The center row of the figure shows the Unicode character.</span></span> <span data-ttu-id="0240f-115">在 U + fffc 的案例中，這是物件取代字元。</span><span class="sxs-lookup"><span data-stu-id="0240f-115">In the case of U+fffc, this is the object replacement character.</span></span> <span data-ttu-id="0240f-116">圖底部的資料列顯示每個字元的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="0240f-116">The bottom row of the figure shows the hexadecimal value of each character.</span></span>

## <a name="supporting-embedded-objects-in-an-application"></a><span data-ttu-id="0240f-117">支援應用程式中的内嵌物件</span><span class="sxs-lookup"><span data-stu-id="0240f-117">Supporting Embedded Objects in an Application</span></span>

<span data-ttu-id="0240f-118">TSF manager 會針對 ACP 型應用程式呼叫 [ITextStoreACP：： InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) ，將内嵌物件插入至文字資料流程，或針對錨點應用程式呼叫 [ITextStoreAnchor：： InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) 。</span><span class="sxs-lookup"><span data-stu-id="0240f-118">The TSF manager inserts an embedded object into the text stream by calling [ITextStoreACP::InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) for an ACP-based application, or [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) for an anchor-based application.</span></span> <span data-ttu-id="0240f-119">插入内嵌物件時，應用程式應該將 **TS \_ 字元 \_ 內嵌** 值放在 IDataObject 物件的字元 (位置，或錨點位置) ，並儲存與内嵌物件相關聯的。</span><span class="sxs-lookup"><span data-stu-id="0240f-119">When an embedded object is inserted, the application should place the **TS\_CHAR\_EMBEDDED** value at the character position (or anchor location) where the object is embedded and store the IDataObject associated with the embedded object.</span></span> <span data-ttu-id="0240f-120">當呼叫 [ITextStoreACP：： GetText](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) 或 [ITextStoreAnchor：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) ，且内嵌物件包含在取得的文字內時， **TS \_ 字元 \_ 內嵌** 值會指出内嵌物件的存在和位置。</span><span class="sxs-lookup"><span data-stu-id="0240f-120">When [ITextStoreACP::GetText](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) is called and an embedded object is contained within the text obtained, the **TS\_CHAR\_EMBEDDED** value indicates the presence and location of the embedded object.</span></span> <span data-ttu-id="0240f-121">若要取得内嵌物件，請以内嵌物件的字元位置呼叫 [ITextStoreACP：： GetEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) ，或使用内嵌物件的錨點位置來呼叫 [ITextStoreAnchor：： GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) 。</span><span class="sxs-lookup"><span data-stu-id="0240f-121">To obtain the embedded object, call [ITextStoreACP::GetEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) with the character position of the embedded object, or [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) with the anchor location of the embedded object.</span></span>

<span data-ttu-id="0240f-122">應用程式通常不會辨識内嵌物件的內容。</span><span class="sxs-lookup"><span data-stu-id="0240f-122">The application does not normally recognize the embedded object contents.</span></span> <span data-ttu-id="0240f-123">應用程式可以嘗試從物件本身取得顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="0240f-123">The application can attempt to obtain display information from the object itself.</span></span> <span data-ttu-id="0240f-124">如果内嵌物件可以提供應用程式可辨識的格式資料，例如 CF \_ UNICODETEXT 或 cf \_ 點陣圖，則應用程式可以顯示物件所提供的圖形資訊。</span><span class="sxs-lookup"><span data-stu-id="0240f-124">If the embedded object can supply data in a format that the application recognizes, such as CF\_UNICODETEXT or CF\_BITMAP, the application can display graphic information supplied by the object.</span></span>

## <a name="inserting-embedded-objects"></a><span data-ttu-id="0240f-125">插入內嵌物件</span><span class="sxs-lookup"><span data-stu-id="0240f-125">Inserting Embedded Objects</span></span>

<span data-ttu-id="0240f-126">文字服務會藉由呼叫 [ITfRange：： InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) 或 [ITfInsertAtSelection：： InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)，將内嵌物件插入內容中。</span><span class="sxs-lookup"><span data-stu-id="0240f-126">A text service inserts an embedded object into a context by calling [ITfRange::InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) or [ITfInsertAtSelection::InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection).</span></span> <span data-ttu-id="0240f-127">文字服務必須提供內嵌的 IDataObject。</span><span class="sxs-lookup"><span data-stu-id="0240f-127">The text service must supply the embedded IDataObject.</span></span>

 

 
