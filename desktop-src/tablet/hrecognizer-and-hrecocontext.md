---
description: 您可以使用 HRECOGNIZER 控制碼和辨識器內容（HRECOCONTEXT 控制碼）來參考筆墨辨識器。辨識器動態連結程式庫 (DLL) 可以針對多個語言執行辨識器。
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER 和 HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992001"
---
# <a name="hrecognizer-and-hrecocontext"></a><span data-ttu-id="61dfe-103">HRECOGNIZER 和 HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="61dfe-103">HRECOGNIZER and HRECOCONTEXT</span></span>

<span data-ttu-id="61dfe-104">您可以使用 [HRECOGNIZER](hrecognizer-handle.md) 控制碼和辨識器內容（ [HRECOCONTEXT](hrecocontext-handle.md) 控制碼）來參考筆墨辨識器。</span><span class="sxs-lookup"><span data-stu-id="61dfe-104">You reference an ink recognizer with an [HRECOGNIZER](hrecognizer-handle.md) handle and a recognizer context as an [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="61dfe-105">辨識器動態連結程式庫 (DLL) 可以針對多個語言執行辨識器。</span><span class="sxs-lookup"><span data-stu-id="61dfe-105">A recognizer dynamic-link library (DLL) can implement recognizers for more than one language.</span></span> <span data-ttu-id="61dfe-106">如果是的話，在應用程式中建立 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件時，會使用所傳入的 CLSID 來選取每種語言。</span><span class="sxs-lookup"><span data-stu-id="61dfe-106">If so, each language is selected by a CLSID that is passed in when creating the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object in the application.</span></span> <span data-ttu-id="61dfe-107">此外，辨識器 DLL 可以在載入時建立多個辨識器控制碼，每個辨識的語言會有一或多個。</span><span class="sxs-lookup"><span data-stu-id="61dfe-107">In addition, a recognizer DLL can create multiple recognizer handles when it is loaded, one or more for each language recognized.</span></span>

<span data-ttu-id="61dfe-108">建立辨識器內容以表示辨識特定筆跡的事件。</span><span class="sxs-lookup"><span data-stu-id="61dfe-108">A recognizer context is created to represent the event of recognizing a specific piece of ink.</span></span> <span data-ttu-id="61dfe-109">建立內容時，會將相關聯的辨識器物件控制碼傳遞至 [**CreateCoNtext**](/windows/desktop/api/recapis/nf-recapis-createcontext) 函式。</span><span class="sxs-lookup"><span data-stu-id="61dfe-109">When the context is created, the associated recognizer objects handle is passed to the [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) function.</span></span> <span data-ttu-id="61dfe-110">這會使語言與辨識器內容產生關聯。</span><span class="sxs-lookup"><span data-stu-id="61dfe-110">This associates the language with the recognizer context.</span></span>

<span data-ttu-id="61dfe-111">辨識器內容可能代表電子郵件內文中所有筆墨的辨識、應用程式中單一欄位的筆墨，或 Tablet PC 輸入面板中書寫的單一文字行。</span><span class="sxs-lookup"><span data-stu-id="61dfe-111">A recognizer context may represent the recognition of all the ink in the body of an email, the ink of a single field within an application, or a single line of text written in the Tablet PC Input Panel.</span></span> <span data-ttu-id="61dfe-112">單一辨識器內容中的筆跡數量可能會因單一筆劃和整個頁面的不同而不同。</span><span class="sxs-lookup"><span data-stu-id="61dfe-112">The volume of ink in a single recognizer context may vary from a single stroke to a whole page or more.</span></span>

<span data-ttu-id="61dfe-113">辨識器內容是由的設定所定義：</span><span class="sxs-lookup"><span data-stu-id="61dfe-113">The recognizer context is defined by the settings of:</span></span>

-   <span data-ttu-id="61dfe-114">辨識指南。</span><span class="sxs-lookup"><span data-stu-id="61dfe-114">The recognition guide.</span></span>
-   <span data-ttu-id="61dfe-115">任何 factoids。</span><span class="sxs-lookup"><span data-stu-id="61dfe-115">Any factoids.</span></span>
-   <span data-ttu-id="61dfe-116">任何旗標。</span><span class="sxs-lookup"><span data-stu-id="61dfe-116">Any flags.</span></span>
-   <span data-ttu-id="61dfe-117">文字內容。</span><span class="sxs-lookup"><span data-stu-id="61dfe-117">The text context.</span></span>
-   <span data-ttu-id="61dfe-118">任何單字清單。</span><span class="sxs-lookup"><span data-stu-id="61dfe-118">Any word list.</span></span>
-   <span data-ttu-id="61dfe-119">字元自動完成模式。</span><span class="sxs-lookup"><span data-stu-id="61dfe-119">The character Autocomplete mode.</span></span>

<span data-ttu-id="61dfe-120">辨識器內容的控制碼會傳遞至所有使用這些設定的函式。</span><span class="sxs-lookup"><span data-stu-id="61dfe-120">The handle for the recognizer context is passed to all functions that use these settings.</span></span> <span data-ttu-id="61dfe-121">變更設定會變更辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="61dfe-121">Changing a setting changes the recognizer context.</span></span>

<span data-ttu-id="61dfe-122">應用程式可能會使用數個內容來辨識螢幕不同部分的筆墨。</span><span class="sxs-lookup"><span data-stu-id="61dfe-122">The application may use several contexts to recognize ink from different parts of the screen.</span></span> <span data-ttu-id="61dfe-123">個別內容可以辨識多行文字。</span><span class="sxs-lookup"><span data-stu-id="61dfe-123">An individual context can recognize multiple lines of text.</span></span> <span data-ttu-id="61dfe-124">不過，個別內容無法處理並排寫入的兩個段落，例如報紙文章中的多個資料行。</span><span class="sxs-lookup"><span data-stu-id="61dfe-124">However, an individual context cannot process two paragraphs written side by side, such as multiple columns in a newspaper article.</span></span>

<span data-ttu-id="61dfe-125">若要辨識新筆墨，請建立新的內容。</span><span class="sxs-lookup"><span data-stu-id="61dfe-125">To recognize new ink, create a new context.</span></span> <span data-ttu-id="61dfe-126">或者，您也可以使用 [**CloneCoNtext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) 函式來製作沒有筆墨和結果的內容複本，或使用 [**ResetCoNtext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) 函式來清除其筆跡和結果的內容。</span><span class="sxs-lookup"><span data-stu-id="61dfe-126">As an alternative, use the [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) function to make a copy of a context that does not have the ink and results, or the [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) function to clear a context of its ink and results.</span></span> <span data-ttu-id="61dfe-127">使用這些方法時，筆跡應用程式可以重複使用內容。</span><span class="sxs-lookup"><span data-stu-id="61dfe-127">With these approaches, an ink application can reuse a context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61dfe-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="61dfe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61dfe-129">**SetGuide 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-129">**SetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[<span data-ttu-id="61dfe-130">**GetGuide 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-130">**GetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[<span data-ttu-id="61dfe-131">**SetFactoid 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-131">**SetFactoid Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[<span data-ttu-id="61dfe-132">**SetFlags 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-132">**SetFlags Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[<span data-ttu-id="61dfe-133">**SetEnabledUnicodeRanges 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-133">**SetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="61dfe-134">**GetEnabledUnicodeRanges 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-134">**GetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="61dfe-135">**SetCACMode 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-135">**SetCACMode Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[<span data-ttu-id="61dfe-136">**SetTextCoNtext 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-136">**SetTextContext Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[<span data-ttu-id="61dfe-137">**SetWordList 函式**</span><span class="sxs-lookup"><span data-stu-id="61dfe-137">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



