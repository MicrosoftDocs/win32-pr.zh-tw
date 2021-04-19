---
title: 如何使用單字和換行資訊
description: Rich edit 控制項會呼叫稱為斷詞程式的函式，以找出單字之間的中斷，以及判斷它可以中斷行的位置。
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969939"
---
# <a name="how-to-use-word-and-line-break-information"></a><span data-ttu-id="33803-103">如何使用單字和換行資訊</span><span class="sxs-lookup"><span data-stu-id="33803-103">How to Use Word and Line Break Information</span></span>

<span data-ttu-id="33803-104">Rich edit 控制項會呼叫稱為斷詞程式的函式，以找出單字之間的中斷，以及判斷它可以中斷行的位置。</span><span class="sxs-lookup"><span data-stu-id="33803-104">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="33803-105">控制項在執行自動換行作業時，以及處理 CTRL + 向左鍵和 CTRL + 向右鍵按鍵組合時，會使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="33803-105">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="33803-106">應用程式可以傳送訊息至 Rich Edit 控制項來取代預設斷字程序、擷取斷字資訊，以及決定指定的字元落在哪一行的位置。</span><span class="sxs-lookup"><span data-stu-id="33803-106">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="33803-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="33803-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="33803-108">技術</span><span class="sxs-lookup"><span data-stu-id="33803-108">Technologies</span></span>

-   [<span data-ttu-id="33803-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="33803-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="33803-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="33803-110">Prerequisites</span></span>

-   <span data-ttu-id="33803-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="33803-111">C/C++</span></span>
-   <span data-ttu-id="33803-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="33803-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="33803-113">指示</span><span class="sxs-lookup"><span data-stu-id="33803-113">Instructions</span></span>

### <a name="use-word-and-line-break-information"></a><span data-ttu-id="33803-114">使用單字和換行資訊</span><span class="sxs-lookup"><span data-stu-id="33803-114">Use Word and Line Break Information</span></span>

<span data-ttu-id="33803-115">Rich edit 控制項的斷詞程式與編輯控制項的斷詞程式很類似，但有其他功能：這兩種控制項的斷詞程式都可以判斷字元是否為分隔符號，並可在指定的位置之前或之後找到最接近的單字分隔符號。</span><span class="sxs-lookup"><span data-stu-id="33803-115">Word-break procedures for rich edit controls are similar to those for edit controls, but they have additional capabilities: word-break procedures for both kinds of controls can determine whether a character is a delimiter and can find the nearest word break before or after the specified position.</span></span> <span data-ttu-id="33803-116">分隔符號是標示單字結尾的字元，例如空格。</span><span class="sxs-lookup"><span data-stu-id="33803-116">A delimiter is a character that marks the end of a word, such as a space.</span></span> <span data-ttu-id="33803-117">通常，在編輯控制項中，只會在分隔符號後出現斷字。</span><span class="sxs-lookup"><span data-stu-id="33803-117">Usually, in an edit control, a word break occurs only after delimiters.</span></span> <span data-ttu-id="33803-118">不過，不同的規則適用于大部分的亞洲語言。</span><span class="sxs-lookup"><span data-stu-id="33803-118">However, different rules apply to most Asian languages.</span></span>

<span data-ttu-id="33803-119">Rich edit 控制項的斷詞程式也會將字元分組到字元類別，每個字元類別都是由0x00 到0x0F 範圍中的值所識別。</span><span class="sxs-lookup"><span data-stu-id="33803-119">Word-break procedures for rich edit controls also group characters into character classes, each identified by a value in the range 0x00 through 0x0F.</span></span> <span data-ttu-id="33803-120">在不同類別的分隔符號或字元之間進行中斷。</span><span class="sxs-lookup"><span data-stu-id="33803-120">Breaks occur either after delimiters or between characters of different classes.</span></span> <span data-ttu-id="33803-121">因此，有不同類別的英數位元和標點符號字元的斷詞程式，會在) 期間之前和之後的字串 "Win.doc (" 中找到兩個分行符號。</span><span class="sxs-lookup"><span data-stu-id="33803-121">Thus, a word-break procedure with different classes for alphanumeric and punctuation characters would find two word breaks in the string "Win.doc" (before and after the period).</span></span>

<span data-ttu-id="33803-122">字元的類別可以與零或多個文字分隔旗標結合，以形成8位值。</span><span class="sxs-lookup"><span data-stu-id="33803-122">A character's class can be combined with zero or more word-break flags to form an 8-bit value.</span></span> <span data-ttu-id="33803-123">執行自動換行作業時，rich edit 控制項會使用斷詞旗標來判斷它可以中斷的位置。</span><span class="sxs-lookup"><span data-stu-id="33803-123">When performing word-wrap operations, a rich edit control uses word-break flags to determine where it can break lines.</span></span> <span data-ttu-id="33803-124">Rich Edit 會使用下列文字分隔旗標。</span><span class="sxs-lookup"><span data-stu-id="33803-124">Rich Edit uses the following word-break flags.</span></span>



| <span data-ttu-id="33803-125">旗標</span><span class="sxs-lookup"><span data-stu-id="33803-125">Flag</span></span>            | <span data-ttu-id="33803-126">描述</span><span class="sxs-lookup"><span data-stu-id="33803-126">Description</span></span>                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33803-127">WBF \_ >BREAKAFTER</span><span class="sxs-lookup"><span data-stu-id="33803-127">WBF\_BREAKAFTER</span></span> | <span data-ttu-id="33803-128">行可能會在字元之後中斷。</span><span class="sxs-lookup"><span data-stu-id="33803-128">Lines may be broken after the character.</span></span>                                                                                          |
| <span data-ttu-id="33803-129">WBF \_ BREAKLINE</span><span class="sxs-lookup"><span data-stu-id="33803-129">WBF\_BREAKLINE</span></span>  | <span data-ttu-id="33803-130">字元是分隔符號。</span><span class="sxs-lookup"><span data-stu-id="33803-130">The character is a delimiter.</span></span> <span data-ttu-id="33803-131">分隔符號標示單字的結尾。</span><span class="sxs-lookup"><span data-stu-id="33803-131">Delimiters mark the ends of words.</span></span> <span data-ttu-id="33803-132">行可能會在分隔符號之後中斷。</span><span class="sxs-lookup"><span data-stu-id="33803-132">Lines may be broken after delimiters.</span></span>                            |
| <span data-ttu-id="33803-133">WBF \_ ISWHITE</span><span class="sxs-lookup"><span data-stu-id="33803-133">WBF\_ISWHITE</span></span>    | <span data-ttu-id="33803-134">字元是空白字元。</span><span class="sxs-lookup"><span data-stu-id="33803-134">The character is a white-space character.</span></span> <span data-ttu-id="33803-135">換行時，尾端的空白字元不會包含在行的長度中。</span><span class="sxs-lookup"><span data-stu-id="33803-135">Trailing white-space characters are not included in the length of a line when wrapping.</span></span> |



 

<span data-ttu-id="33803-136">WBF \_ >breakafter 值是用來允許在未標示單字結尾的字元之後換行，例如連字號。</span><span class="sxs-lookup"><span data-stu-id="33803-136">The WBF\_BREAKAFTER value is used to allow wrapping after a character that does not mark the end of a word, such as a hyphen.</span></span>

<span data-ttu-id="33803-137">您可以使用 [**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md) 訊息，將 rich edit 控制項的預設斷詞程式取代為您自己的程式。</span><span class="sxs-lookup"><span data-stu-id="33803-137">You can replace the default word-break procedure for a rich edit control with your own procedure by using the [**EM\_SETWORDBREAKPROC**](em-setwordbreakproc.md) message.</span></span> <span data-ttu-id="33803-138">如需有關斷詞程式的詳細資訊，請參閱 [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) 函數的描述。</span><span class="sxs-lookup"><span data-stu-id="33803-138">For more information about word-break procedures, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="33803-139">由於多語系斷詞的複雜度，因此不建議 Microsoft Rich Edit 2.0 和更新版本使用此取代。</span><span class="sxs-lookup"><span data-stu-id="33803-139">This replacement is not recommended for Microsoft Rich Edit 2.0 and later, due to the complexity of multilingual word breaking.</span></span>

 

<span data-ttu-id="33803-140">針對 Microsoft Rich Edit 1.0，您可以使用 [**EM \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) 訊息，以 [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) 函式取代預設的擴充字組分隔程式。</span><span class="sxs-lookup"><span data-stu-id="33803-140">For Microsoft Rich Edit 1.0, you can use the [**EM\_SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) message to replace the default extended word-break procedure with an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function.</span></span> <span data-ttu-id="33803-141">此函式會提供文字的其他相關資訊，例如字元集。</span><span class="sxs-lookup"><span data-stu-id="33803-141">This function provides additional information about the text, such as the character set.</span></span> <span data-ttu-id="33803-142">您可以使用 [**EM \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) 訊息來取出目前擴充的斷詞程式的位址。</span><span class="sxs-lookup"><span data-stu-id="33803-142">You can use the [**EM\_GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) message to retrieve the address of the current extended word-break procedure.</span></span> <span data-ttu-id="33803-143">請注意，Microsoft Rich Edit 2.0 和更新版本不支援 *EditWordBreakProcEx*、 **Em \_ GETWORDBREAKPROCEX** 和 **EM \_ SETWORDBREAKPROCEX**。</span><span class="sxs-lookup"><span data-stu-id="33803-143">Note that Microsoft Rich Edit 2.0 and later do not support *EditWordBreakProcEx*, **EM\_GETWORDBREAKPROCEX**, and **EM\_SETWORDBREAKPROCEX**.</span></span>

<span data-ttu-id="33803-144">您可以使用 [**EM \_ FINDWORDBREAK**](em-findwordbreak.md) 訊息來尋找斷詞，或判斷字元的類別和斷詞旗標。</span><span class="sxs-lookup"><span data-stu-id="33803-144">You can use the [**EM\_FINDWORDBREAK**](em-findwordbreak.md) message to find word breaks or to determine a character's class and word-break flags.</span></span> <span data-ttu-id="33803-145">接著，控制項會呼叫它的斷詞程式來取得要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="33803-145">In turn, the control calls its word-break procedure to get the requested information.</span></span>

<span data-ttu-id="33803-146">若要判斷指定字元落在哪個行上，您可以使用 [**EM \_ EXLINEFROMCHAR**](em-exlinefromchar.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="33803-146">To determine which line a given character falls on, you can use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33803-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="33803-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33803-148">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="33803-148">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="33803-149">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="33803-149">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 