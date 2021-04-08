---
description: 使用字型回復
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: 使用字型回復
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9afb073a01cc1c5b90d4a4861a973846d3ae9ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695631"
---
# <a name="using-font-fallback"></a><span data-ttu-id="e52ad-103">使用字型回復</span><span class="sxs-lookup"><span data-stu-id="e52ad-103">Using Font Fallback</span></span>

> [!Note]  
> <span data-ttu-id="e52ad-104">在本主題中，所有關于 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 的備註都同樣適用于 [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)。</span><span class="sxs-lookup"><span data-stu-id="e52ad-104">In this topic, all remarks about [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) apply equally to [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).</span></span>

 

<span data-ttu-id="e52ad-105">如果字型中不支援字串中的某些字元，或如果應用程式使用字型不支援的 [複雜字集](uniscribe-glossary.md) ，則您的應用程式必須在文字顯示期間使用字型回復。</span><span class="sxs-lookup"><span data-stu-id="e52ad-105">Your application must use font fallback during text display if some characters in a string are not supported in the font, or if the application uses a [complex script](uniscribe-glossary.md) not supported by the font.</span></span> <span data-ttu-id="e52ad-106">當應用程式呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 函式時，會在文字的版面配置程式期間偵測到字型回復的需求。</span><span class="sxs-lookup"><span data-stu-id="e52ad-106">The requirement for font fallback is detected during the layout process for text, when the application calls the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) function.</span></span> <span data-ttu-id="e52ad-107">如需文字顯示的詳細資訊，請參閱 [使用 Uniscribe 來顯示文字](displaying-text-with-uniscribe.md)。</span><span class="sxs-lookup"><span data-stu-id="e52ad-107">For information about text display, see [Displaying Text with Uniscribe](displaying-text-with-uniscribe.md).</span></span>

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a><span data-ttu-id="e52ad-108">判斷支援的字元是否需要字型回復</span><span class="sxs-lookup"><span data-stu-id="e52ad-108">Determine the Need for Font Fallback for Unsupported Characters</span></span>

<span data-ttu-id="e52ad-109">如果要求的字型不支援字串中的某些字元，則 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 的應用程式呼叫會成功。</span><span class="sxs-lookup"><span data-stu-id="e52ad-109">If some of the characters in a string are not supported in a requested font, an application call to [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) succeeds.</span></span> <span data-ttu-id="e52ad-110">不過，應用程式必須掃描圖像輸出緩衝區是否有遺漏的圖像。</span><span class="sxs-lookup"><span data-stu-id="e52ad-110">However, the application must scan the glyph output buffer for the presence of missing glyphs.</span></span> <span data-ttu-id="e52ad-111">您可以藉由呼叫 [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)，判斷特定字型的圖像索引。</span><span class="sxs-lookup"><span data-stu-id="e52ad-111">The glyph index of the missing glyph can be determined for a specific font by calling [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties).</span></span> <span data-ttu-id="e52ad-112">如果無法使用特定的圖像，應用程式必須切換回圖像的不同字型，或轉譯表示沒有可用字元的圖形符號。</span><span class="sxs-lookup"><span data-stu-id="e52ad-112">If a particular glyph is unavailable, the application must either fall back to a different font for a glyph or render a graphic symbol that indicates that no glyph is available.</span></span>

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a><span data-ttu-id="e52ad-113">針對不支援的複雜字集，判斷字型回復的需求</span><span class="sxs-lookup"><span data-stu-id="e52ad-113">Determine the Need for Font Fallback for Unsupported Complex Scripts</span></span>

<span data-ttu-id="e52ad-114">應用程式慣用的顯示字型可能不支援文字所需的複雜字集。</span><span class="sxs-lookup"><span data-stu-id="e52ad-114">The font that an application prefers for display might not support a complex script that is required by the text.</span></span> <span data-ttu-id="e52ad-115">在此情況下，對 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 的應用程式呼叫會失敗，並出現錯誤碼 E \_ 腳本的 \_ 非 \_ \_ 字型。</span><span class="sxs-lookup"><span data-stu-id="e52ad-115">In this case, the application call to [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) fails with the error code E\_SCRIPT\_NOT\_IN\_FONT.</span></span>

## <a name="assign-a-fallback-font"></a><span data-ttu-id="e52ad-116">指派回復字型</span><span class="sxs-lookup"><span data-stu-id="e52ad-116">Assign a Fallback Font</span></span>

<span data-ttu-id="e52ad-117">一旦判斷出需要字型回復之後，應用程式就必須指派回復字型。</span><span class="sxs-lookup"><span data-stu-id="e52ad-117">Once it has determined that font fallback is required, the application must assign a fallback font.</span></span> <span data-ttu-id="e52ad-118">應用程式可以嘗試下列技術：</span><span class="sxs-lookup"><span data-stu-id="e52ad-118">The application can try the following techniques:</span></span>

-   <span data-ttu-id="e52ad-119">針對字型清單中的每個字型呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ，直到一個呼叫具有可接受的傳回。</span><span class="sxs-lookup"><span data-stu-id="e52ad-119">Call [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) for each font in a font list until one call has an acceptable return.</span></span>
-   <span data-ttu-id="e52ad-120">使用清單中的每個字型來呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ，直到判斷任何字型都不會成功為止。</span><span class="sxs-lookup"><span data-stu-id="e52ad-120">Call [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) with each font in a list until it can be determined that no font will succeed.</span></span> <span data-ttu-id="e52ad-121">如果錯誤碼一律為 E \_ SCRIPT \_ not \_ \_ 字型，字型就不支援複雜的腳本。</span><span class="sxs-lookup"><span data-stu-id="e52ad-121">If the error code is always E\_SCRIPT\_NOT\_IN\_FONT, a complex script is not supported by the fonts.</span></span> <span data-ttu-id="e52ad-122">轉譯圖形符號，指出沒有任何可用的圖像，或將腳本重新指定為未定義 (沒有腳本處理) ，然後重新開機。</span><span class="sxs-lookup"><span data-stu-id="e52ad-122">Either render a graphic symbol that indicates that no glyph is available, or re-specify the script as undefined (no script processing) and start again.</span></span> <span data-ttu-id="e52ad-123">若要將腳本設定為未定義，請將 [**腳本 \_ 分析**](/windows/win32/api/usp10/ns-usp10-script_analysis)結構的 **eScript** 成員設定為 \_ 未定義腳本。</span><span class="sxs-lookup"><span data-stu-id="e52ad-123">To set the script as undefined, set the **eScript** member of the [**SCRIPT\_ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) structure to SCRIPT\_UNDEFINED.</span></span>
-   <span data-ttu-id="e52ad-124">使用清單中的每個字型來呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ，直到判斷任何字型都不會成功為止。</span><span class="sxs-lookup"><span data-stu-id="e52ad-124">Call [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) with each font in a list until it can be determined that no font will succeed.</span></span> <span data-ttu-id="e52ad-125">如果錯誤碼指出某些字元是對應至遺失的字元，請將字串分解為較小的範圍。</span><span class="sxs-lookup"><span data-stu-id="e52ad-125">If the error code indicates that some of the characters are mapping to missing glyphs, break up the string into smaller ranges.</span></span> <span data-ttu-id="e52ad-126">您可以將不同的字型指派給子範圍，讓更多的字元可以呈現。</span><span class="sxs-lookup"><span data-stu-id="e52ad-126">Different fonts can be assigned to subranges so that more of the characters can be rendered.</span></span>

## <a name="generate-glyph-information"></a><span data-ttu-id="e52ad-127">產生符號資訊</span><span class="sxs-lookup"><span data-stu-id="e52ad-127">Generate Glyph Information</span></span>

<span data-ttu-id="e52ad-128">一旦應用程式指派了成功呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)的字型之後，就可以呼叫 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) ，從 **ScriptShape** 的輸出產生圖像前進寬度和二維位移資訊。</span><span class="sxs-lookup"><span data-stu-id="e52ad-128">Once the application has assigned a font that succeeds in calls to [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), it can make calls to [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) to generate glyph advance width and two-dimensional offset information from the output of **ScriptShape**.</span></span> <span data-ttu-id="e52ad-129">在這些呼叫中，字型應該會成功。</span><span class="sxs-lookup"><span data-stu-id="e52ad-129">The font should succeed in these calls.</span></span> <span data-ttu-id="e52ad-130">在 **ScriptShape** 呼叫成功後呼叫 **ScriptPlace** 的字型失敗，表示有不正確字型。</span><span class="sxs-lookup"><span data-stu-id="e52ad-130">A font failure in a call to **ScriptPlace** after success in a **ScriptShape** call indicates a broken font.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e52ad-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="e52ad-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e52ad-132">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="e52ad-132">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



