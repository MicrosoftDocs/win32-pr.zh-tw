---
title: 如何格式化 Rich Edit 控制項中的文字
description: 應用程式可以將訊息傳送至 rich edit 控制項，以便格式化字元和段落，並取出格式資訊。
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103681604"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a><span data-ttu-id="d0614-103">如何格式化 Rich Edit 控制項中的文字</span><span class="sxs-lookup"><span data-stu-id="d0614-103">How to Format Text in Rich Edit Controls</span></span>

<span data-ttu-id="d0614-104">應用程式可以將訊息傳送至 rich edit 控制項，以便格式化字元和段落，並取出格式資訊。</span><span class="sxs-lookup"><span data-stu-id="d0614-104">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="d0614-105">段落格式化屬性包括對齊、索引標籤、縮排、編號和簡單的資料表。</span><span class="sxs-lookup"><span data-stu-id="d0614-105">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="d0614-106">若為字元，您可以指定字型名稱、大小、色彩和效果，例如粗體、斜體和 protected。</span><span class="sxs-lookup"><span data-stu-id="d0614-106">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d0614-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d0614-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d0614-108">技術</span><span class="sxs-lookup"><span data-stu-id="d0614-108">Technologies</span></span>

-   [<span data-ttu-id="d0614-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d0614-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d0614-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="d0614-110">Prerequisites</span></span>

-   <span data-ttu-id="d0614-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d0614-111">C/C++</span></span>
-   <span data-ttu-id="d0614-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d0614-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d0614-113">指示</span><span class="sxs-lookup"><span data-stu-id="d0614-113">Instructions</span></span>

### <a name="format-text-in-a-rich-edit-control"></a><span data-ttu-id="d0614-114">格式化 Rich Edit 控制項中的文字</span><span class="sxs-lookup"><span data-stu-id="d0614-114">Format Text in a Rich Edit Control</span></span>

<span data-ttu-id="d0614-115">您可以使用 [**EM \_ SETPARAFORMAT**](em-setparaformat.md) 訊息來套用段落格式。</span><span class="sxs-lookup"><span data-stu-id="d0614-115">You can apply paragraph formatting by using the [**EM\_SETPARAFORMAT**](em-setparaformat.md) message.</span></span> <span data-ttu-id="d0614-116">若要判斷所選取文字的目前段落格式，請使用 [**EM \_ GETPARAFORMAT**](em-getparaformat.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d0614-116">To determine the current paragraph formatting for the selected text, use the [**EM\_GETPARAFORMAT**](em-getparaformat.md) message.</span></span> <span data-ttu-id="d0614-117">[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)或 [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)結構會與這兩個訊息一起使用，以指定段落格式化屬性。</span><span class="sxs-lookup"><span data-stu-id="d0614-117">The [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) or [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure is used with both messages to specify paragraph formatting attributes.</span></span>

<span data-ttu-id="d0614-118">您可以使用 [**EM \_ SETCHARFORMAT**](em-setcharformat.md) 訊息來套用字元格式。</span><span class="sxs-lookup"><span data-stu-id="d0614-118">You can apply character formatting by using the [**EM\_SETCHARFORMAT**](em-setcharformat.md) message.</span></span> <span data-ttu-id="d0614-119">若要判斷所選取文字的目前字元格式，您可以使用 [**EM \_ GETCHARFORMAT**](em-getcharformat.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d0614-119">To determine the current character formatting for the selected text, you can use the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span> <span data-ttu-id="d0614-120">[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)或 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)結構會與這兩個訊息一起使用，以指定字元屬性。</span><span class="sxs-lookup"><span data-stu-id="d0614-120">The [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) or [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure is used with both messages to specify character attributes.</span></span>

<span data-ttu-id="d0614-121">您也可以使用 [**em \_ SETCHARFORMAT**](em-setcharformat.md) 和 [**em \_ GETCHARFORMAT**](em-getcharformat.md) 訊息來設定和取出插入點的字元格式，也就是套用至任何後續插入字元的格式。</span><span class="sxs-lookup"><span data-stu-id="d0614-121">You can also use [**EM\_SETCHARFORMAT**](em-setcharformat.md) and [**EM\_GETCHARFORMAT**](em-getcharformat.md) messages to set and retrieve the character formatting of the insertion point, which is the formatting that is applied to any subsequently inserted characters.</span></span> <span data-ttu-id="d0614-122">例如，如果應用程式將預設的字元格式設定為粗體，而使用者接著輸入字元，則該字元為粗體。</span><span class="sxs-lookup"><span data-stu-id="d0614-122">For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold.</span></span>

<span data-ttu-id="d0614-123">只有當目前的選取範圍是插入點) 時，才會將插入點的字元格式套用至新插入的文字 (。</span><span class="sxs-lookup"><span data-stu-id="d0614-123">The character formatting of the insertion point is applied to newly inserted text only if the current selection is empty (if the current selection is an insertion point).</span></span> <span data-ttu-id="d0614-124">否則，新的文字會假設它所取代之文字的字元格式。</span><span class="sxs-lookup"><span data-stu-id="d0614-124">Otherwise, the new text assumes the character formatting of the text it replaces.</span></span> <span data-ttu-id="d0614-125">如果選取範圍變更，則會變更預設的字元格式，以符合新選取範圍中的第一個字元。</span><span class="sxs-lookup"><span data-stu-id="d0614-125">If the selection changes, the default character formatting changes to match the first character in the new selection.</span></span>

<span data-ttu-id="d0614-126">受保護的字元效果是唯一的，因為它不會變更文字的外觀。</span><span class="sxs-lookup"><span data-stu-id="d0614-126">The protected character effect is unique in that it does not change the appearance of text.</span></span> <span data-ttu-id="d0614-127">如果使用者嘗試修改受保護的文字，rich edit 控制項會將 [ \_ 受保護](en-protected.md) 的通知碼傳送給其父視窗，讓父視窗允許或防止變更。</span><span class="sxs-lookup"><span data-stu-id="d0614-127">If the user attempts to modify protected text, a rich edit control sends its parent window an [EN\_PROTECTED](en-protected.md) notification code, allowing the parent window to allow or prevent the change.</span></span> <span data-ttu-id="d0614-128">若要接收此通知碼，您必須使用 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息來啟用它。</span><span class="sxs-lookup"><span data-stu-id="d0614-128">To receive this notification code, you must enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="d0614-129">前景色彩一律是字元屬性。</span><span class="sxs-lookup"><span data-stu-id="d0614-129">Foreground color is always a character attribute.</span></span> <span data-ttu-id="d0614-130">在 Microsoft Rich Edit 1.0 中，背景色彩只是 Rich edit 控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="d0614-130">In Microsoft Rich Edit 1.0, background color is only a property of the rich edit control.</span></span> <span data-ttu-id="d0614-131">若要設定預設的背景色彩，請使用 [**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d0614-131">To set the default background color, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span> <span data-ttu-id="d0614-132">請注意，Rich Edit 不支援 [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d0614-132">Note that Rich Edit does not support the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0614-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0614-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0614-134">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="d0614-134">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d0614-135">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d0614-135">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




