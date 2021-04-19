---
description: 以下是顯示和相關的文字處理方式選項，可支援精細的印刷效果或複雜的腳本： Text functionsEdit controlsRich edit controlsUniscribe
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: 複雜的腳本處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e4be6295bff949c8e29036ef3af496c673575e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977349"
---
# <a name="complex-script-processing"></a><span data-ttu-id="a8c3e-103">複雜的腳本處理</span><span class="sxs-lookup"><span data-stu-id="a8c3e-103">Complex Script Processing</span></span>

<span data-ttu-id="a8c3e-104">以下是顯示和相關的文字處理方式的選項，可支援精細的印刷效果或複雜的腳本：</span><span class="sxs-lookup"><span data-stu-id="a8c3e-104">The following are options for display and related processing of text to support fine typography effects or complex scripts:</span></span>

-   <span data-ttu-id="a8c3e-105">文字函數</span><span class="sxs-lookup"><span data-stu-id="a8c3e-105">Text functions</span></span>
-   <span data-ttu-id="a8c3e-106">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="a8c3e-106">Edit controls</span></span>
-   <span data-ttu-id="a8c3e-107">Rich edit 控制項</span><span class="sxs-lookup"><span data-stu-id="a8c3e-107">Rich edit controls</span></span>
-   <span data-ttu-id="a8c3e-108">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="a8c3e-108">Uniscribe</span></span>

<span data-ttu-id="a8c3e-109">您選擇的選項取決於下列因素：</span><span class="sxs-lookup"><span data-stu-id="a8c3e-109">The options you choose depend on the following factors:</span></span>

-   <span data-ttu-id="a8c3e-110">文字或腳本的類型。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-110">The type of text or scripts.</span></span>
-   <span data-ttu-id="a8c3e-111">執行模型，例如，應用程式所中斷的文字配置和處理。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-111">The implementation model, for example, the text layout and handling of line breaking by the application.</span></span>
-   <span data-ttu-id="a8c3e-112">更新現有的應用程式，而不是建立新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-112">Update of an existing application versus creation of a new application.</span></span>

<span data-ttu-id="a8c3e-113">一般情況下，執行相當簡單之腳本處理的應用程式可以選擇處理複雜字集的任何選項。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-113">In general, an application that does relatively simple script processing can choose any option for processing complex scripts.</span></span> <span data-ttu-id="a8c3e-114">但是，若要完整控制複雜的腳本處理，建議使用 Uniscribe。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-114">However, for the most complete control of complex script processing, Uniscribe is recommended.</span></span>

## <a name="complex-script-processing-using-text-functions"></a><span data-ttu-id="a8c3e-115">使用文字函數處理複雜的腳本</span><span class="sxs-lookup"><span data-stu-id="a8c3e-115">Complex Script Processing Using Text Functions</span></span>

<span data-ttu-id="a8c3e-116">使用的應用程式大多是純文字，也就是使用相同字樣、權數、色彩等的文字，在傳統上是使用標準文字函式（例如 [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta)、 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)、 [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)、 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)和 [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa)）來撰寫文字和測量的行長度。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-116">Applications that use mostly plain text, that is, text that uses the same typeface, weight, color, and so on, have traditionally written text and measured line lengths using standard text functions, such as [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa).</span></span> <span data-ttu-id="a8c3e-117">這些函式支援處理複雜的腳本和精細的印刷樣式效果。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-117">These functions support processing for complex scripts and fine typography effects.</span></span> <span data-ttu-id="a8c3e-118">如需詳細資訊，請參閱字型 [和文字](../gdi/fonts-and-text.md)。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-118">For more information, see [Fonts and Text](../gdi/fonts-and-text.md).</span></span>

<span data-ttu-id="a8c3e-119">一般情況下，標準文字支援對處理複雜字集的應用程式而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-119">In general, the standard text support is transparent to applications processing complex scripts.</span></span> <span data-ttu-id="a8c3e-120">不過，您應該留意一些特定規則，以便在撰寫支援精細印刷樣式和處理複雜字集的應用程式時：</span><span class="sxs-lookup"><span data-stu-id="a8c3e-120">However, you should be aware of some specific rules to follow in writing applications that support fine typography and process complex scripts:</span></span>

-   <span data-ttu-id="a8c3e-121">您的應用程式應該將字元儲存在緩衝區中，並一次顯示整行文字，例如，在使用者輸入的每個字元上呼叫 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) 。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-121">Your application should save characters in a buffer and display a whole line of text at one time instead of, for example, calling [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) on each character as it is typed in by the user.</span></span> <span data-ttu-id="a8c3e-122">這種機制可讓 advanced text 成形模組使用內容， [以正確地](uniscribe-glossary.md) 重新排列和產生字元。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-122">This mechanism allows the advanced text shaping modules to use context to reorder and generate [glyphs](uniscribe-glossary.md) correctly.</span></span>
-   <span data-ttu-id="a8c3e-123">應用程式應該使用 [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) 來判斷行長度，而不是從快取的字元寬度計算行長度，因為圖像的寬度可能會因內容而異。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-123">The application should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length, instead of computing line lengths from cached character widths, since the width of a glyph can vary by context.</span></span>
-   <span data-ttu-id="a8c3e-124">應用程式應該選擇性地加入由右至左的讀取順序和靠右對齊的支援。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-124">The application should optionally add support for right-to-left reading order and right alignment.</span></span>
-   <span data-ttu-id="a8c3e-125">複雜字集或精細印刷所需的重新排列和內容處理，需要大幅增加簡單腳本的基本文字顯示處理。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-125">The reordering and contextual processing required for complex scripts or fine typography requires a significant increase in processing over basic text display for simple scripts.</span></span> <span data-ttu-id="a8c3e-126">因此，為了避免發生效能問題，您的應用程式在顯示結果並將控制權傳回給使用者之前，不應處理大量的文字。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-126">Therefore, to avoid performance issues, your application should not process large amounts of text before displaying results and returning control to the user.</span></span>

## <a name="complex-script-processing-using-edit-controls"></a><span data-ttu-id="a8c3e-127">使用編輯控制項的複雜字集處理</span><span class="sxs-lookup"><span data-stu-id="a8c3e-127">Complex Script Processing Using Edit Controls</span></span>

<span data-ttu-id="a8c3e-128">標準的 Windows 編輯控制項已經過擴充，可支援多語系文字和複雜的腳本。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-128">The standard Windows edit controls have been extended to support multilingual text and complex scripts.</span></span> <span data-ttu-id="a8c3e-129">延伸支援包括輸入和顯示，以及透過字元叢集的正確資料指標移動，例如泰文和梵文腳本。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-129">The extended support includes input and display, as well as correct cursor movement over character clusters, for example, in Thai and Devanagari scripts.</span></span> <span data-ttu-id="a8c3e-130">如需詳細資訊，請參閱 [編輯控制項](../controls/edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-130">For more information, see [Edit Controls](../controls/edit-controls.md).</span></span>

## <a name="complex-script-processing-using-rich-edit-controls"></a><span data-ttu-id="a8c3e-131">使用 Rich Edit 控制項進行複雜的腳本處理</span><span class="sxs-lookup"><span data-stu-id="a8c3e-131">Complex Script Processing Using Rich Edit Controls</span></span>

<span data-ttu-id="a8c3e-132">Rich Edit 3.0 是更高層級的介面集合，利用 Uniscribe 來防止文字版面配置應用程式與特定腳本的複雜度。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-132">Rich Edit 3.0 is a higher-level collection of interfaces that takes advantage of Uniscribe to insulate text layout applications from the complexities of certain scripts.</span></span> <span data-ttu-id="a8c3e-133">Rich Edit 是讓應用程式顯示覆雜腳本的最簡單方式，即使它們的主要用途不一定是文字配置也是一樣。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-133">Rich Edit is the simplest way for applications to display complex scripts even though their primary purpose is not necessarily text layout.</span></span> <span data-ttu-id="a8c3e-134">Rich Edit 可提供快速、多功能的豐富 Unicode 多語系文字和簡單純文字編輯。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-134">Rich Edit provides fast, versatile editing of rich Unicode multilingual text and simple plain text.</span></span> <span data-ttu-id="a8c3e-135">它包含廣泛的訊息和 COM 介面、文字編輯、格式化、換行、簡單的資料表配置、垂直文字配置、雙向文字配置、印度文和泰文支援、編輯使用者介面，就像 Microsoft Word 和 Text 物件模型介面一樣。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-135">It includes extensive message and COM interfaces, text editing, formatting, line breaking, simple table layout, vertical text layout, bidirectional text layout, Indic and Thai support, an editing user interface much like Microsoft Word, and Text Object Model interfaces.</span></span>

<span data-ttu-id="a8c3e-136">除了 Rich Edit 介面，應用程式還可以使用 Rich Edit [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) 函式來自動剖析、成形、定位和分隔線條。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-136">Along with the Rich Edit interfaces, applications can use the Rich Edit [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) function to automatically parse, shape, position, and break lines.</span></span> <span data-ttu-id="a8c3e-137">如需詳細資訊，請參閱 [Rich Edit 控制項](../controls/rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-137">For more information, see [Rich Edit Controls](../controls/rich-edit-controls.md).</span></span>

## <a name="complex-script-processing-using-uniscribe"></a><span data-ttu-id="a8c3e-138">使用 Uniscribe 進行複雜的腳本處理</span><span class="sxs-lookup"><span data-stu-id="a8c3e-138">Complex Script Processing Using Uniscribe</span></span>

<span data-ttu-id="a8c3e-139">[Uniscribe](uniscribe.md) 提供最廣泛的處理文字處理，包括精細的印刷效果和複雜的腳本。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-139">[Uniscribe](uniscribe.md) provides the most extensive support for processing of text involving fine typography effects and complex scripts.</span></span> <span data-ttu-id="a8c3e-140">它支援在阿拉伯文、梵文和泰文等腳本中找到的複雜規則。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-140">It supports the complex rules found in scripts such as Arabic, Devanagari, and Thai.</span></span> <span data-ttu-id="a8c3e-141">它會處理由右至左撰寫的腳本，例如阿拉伯文和希伯來文，並支援混合腳本。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-141">It handles scripts written from right to left, such as Arabic and Hebrew, and supports the mixing of scripts.</span></span> <span data-ttu-id="a8c3e-142">Uniscribe 也會公開 [OpenType](opentype-font-format.md) 字型功能，可供應用程式用來控制精細的印刷效果。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-142">Uniscribe also exposes [OpenType](opentype-font-format.md) font features that can be used by applications to control fine typography effects.</span></span> <span data-ttu-id="a8c3e-143">如需詳細資訊，請參閱 [處理複雜的腳本](processing-complex-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="a8c3e-143">For more information, see [Processing Complex Scripts](processing-complex-scripts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8c3e-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8c3e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8c3e-145">關於 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="a8c3e-145">About Uniscribe</span></span>](about-uniscribe.md)
</dt> <dt>

[<span data-ttu-id="a8c3e-146">處理複雜的腳本</span><span class="sxs-lookup"><span data-stu-id="a8c3e-146">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
</dt> </dl>

 

 
