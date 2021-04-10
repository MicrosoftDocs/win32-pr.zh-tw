---
title: 如何與目前的選取範圍互動
description: 使用者可以使用滑鼠或鍵盤選取 rich edit 控制項中的文字。
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103681603"
---
# <a name="how-to-interact-with-the-current-selection"></a><span data-ttu-id="98891-103">如何與目前的選取範圍互動</span><span class="sxs-lookup"><span data-stu-id="98891-103">How to Interact with the Current Selection</span></span>

<span data-ttu-id="98891-104">使用者可以使用滑鼠或鍵盤選取 rich edit 控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="98891-104">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="98891-105">*目前的選取* 範圍是選定字元的範圍，或者，如果未選取任何字元，則為插入點的位置。</span><span class="sxs-lookup"><span data-stu-id="98891-105">The *current selection* is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="98891-106">應用程式可以取得目前選取範圍的相關資訊、設定它、判斷其變更時間，以及顯示或隱藏選取專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="98891-106">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="98891-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="98891-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="98891-108">技術</span><span class="sxs-lookup"><span data-stu-id="98891-108">Technologies</span></span>

-   [<span data-ttu-id="98891-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="98891-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="98891-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="98891-110">Prerequisites</span></span>

-   <span data-ttu-id="98891-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="98891-111">C/C++</span></span>
-   <span data-ttu-id="98891-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="98891-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="98891-113">指示</span><span class="sxs-lookup"><span data-stu-id="98891-113">Instructions</span></span>

### <a name="interact-with-the-current-selection"></a><span data-ttu-id="98891-114">與目前的選取範圍互動</span><span class="sxs-lookup"><span data-stu-id="98891-114">Interact with the Current Selection</span></span>

<span data-ttu-id="98891-115">若要判斷 rich edit 控制項中目前的選取範圍，請使用 [**EM \_ EXGETSEL**](em-exgetsel.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="98891-115">To determine the current selection in a rich edit control, use the [**EM\_EXGETSEL**](em-exgetsel.md) message.</span></span> <span data-ttu-id="98891-116">若要設定目前的選取範圍，請使用 [**EM \_ EXSETSEL**](em-exsetsel.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="98891-116">To set the current selection, use the [**EM\_EXSETSEL**](em-exsetsel.md) message.</span></span> <span data-ttu-id="98891-117">[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)結構會與這兩個訊息一起使用，並指定字元範圍。</span><span class="sxs-lookup"><span data-stu-id="98891-117">The [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure is used with both messages and specifies a range of characters.</span></span> <span data-ttu-id="98891-118">若要取得目前選取範圍內容的相關資訊，您可以使用 [**EM \_ SELECTIONTYPE**](em-selectiontype.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="98891-118">To retrieve information about the contents of the current selection, you can use the [**EM\_SELECTIONTYPE**](em-selectiontype.md) message.</span></span>

<span data-ttu-id="98891-119">應用程式可以藉由處理 [ \_ SELCHANGE](en-selchange.md) 通知程式碼，來偵測目前的選取專案變更的時間。</span><span class="sxs-lookup"><span data-stu-id="98891-119">An application can detect when the current selection changes by processing the [EN\_SELCHANGE](en-selchange.md) notification code.</span></span> <span data-ttu-id="98891-120">通知碼會指定 [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) 結構，其中包含新選取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98891-120">The notification code specifies a [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that contains information about the new selection.</span></span> <span data-ttu-id="98891-121">只有當您使用 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息來啟用時，rich edit 控制項才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="98891-121">A rich edit control sends this notification code only if you enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="98891-122">根據預設，rich edit 控制項會在取得並失去焦點時，顯示並隱藏選取專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="98891-122">By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus.</span></span> <span data-ttu-id="98891-123">您可以使用 [**EM \_ HIDESELECTION**](em-hideselection.md) 訊息，隨時顯示或隱藏選取專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="98891-123">You can show or hide the selection highlight at any time by using the [**EM\_HIDESELECTION**](em-hideselection.md) message.</span></span> <span data-ttu-id="98891-124">例如，應用程式可能會提供搜尋對話方塊來尋找 rich edit 控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="98891-124">For example, an application might provide a Search dialog box to find text in a rich edit control.</span></span> <span data-ttu-id="98891-125">應用程式可能會在不關閉對話方塊的情況下選取相符的文字，在這種情況下，它必須使用 **EM \_ HIDESELECTION** 訊息來反白顯示選取範圍。</span><span class="sxs-lookup"><span data-stu-id="98891-125">The application might select matching text without closing the dialog box, in which case it must use the **EM\_HIDESELECTION** message to highlight the selection.</span></span>

<span data-ttu-id="98891-126">如同編輯控制項，您可以指定 [**ES \_ NOHIDESEL**](edit-control-styles.md) 視窗樣式，以防止 rich edit 控制項在失去焦點時隱藏選取專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="98891-126">As with edit controls, you can specify the [**ES\_NOHIDESEL**](edit-control-styles.md) window style to prevent a rich edit control from hiding the selection highlight when it loses the focus.</span></span>

<span data-ttu-id="98891-127">除了使用 [**em \_ EXGETSEL**](em-exgetsel.md) 和 [**em \_ EXSETSEL**](em-exsetsel.md) 訊息以外，您還可以使用 [**em \_ GETSEL**](em-getsel.md) 和 [**em \_ SETSEL**](em-setsel.md) 編輯控制訊息來取得和設定目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="98891-127">As an alternative to using the [**EM\_EXGETSEL**](em-exgetsel.md) and [**EM\_EXSETSEL**](em-exsetsel.md) messages, you can retrieve and set the current selection by using the [**EM\_GETSEL**](em-getsel.md) and [**EM\_SETSEL**](em-setsel.md) edit control messages.</span></span> <span data-ttu-id="98891-128">**EM \_ GETSEL** 訊息會將 2 16 位字元索引封裝至其32位的傳回值，因此只適用于完全落在第一個64k 內的選取專案。</span><span class="sxs-lookup"><span data-stu-id="98891-128">The **EM\_GETSEL** message packs two 16-bit character indexes into its 32-bit return value and therefore, works only for selections that fall entirely within the first 64K.</span></span> <span data-ttu-id="98891-129">但是，除非您使用 [**em \_ LIMITTEXT**](em-limittext.md) 或 [**em \_ EXLIMITTEXT**](em-exlimittext.md) 訊息來延長此限制，否則 rich Edit 控制項絕不會包含超過32k 個字元的文字。</span><span class="sxs-lookup"><span data-stu-id="98891-129">However, a rich edit control will never contain more than 32K characters of text, unless you extend this limit by using the [**EM\_LIMITTEXT**](em-limittext.md) or [**EM\_EXLIMITTEXT**](em-exlimittext.md) message.</span></span> <span data-ttu-id="98891-130">對於延伸超過前 64 KB 文字的選項， **EM \_ GETSEL** 訊息會傳回–1。</span><span class="sxs-lookup"><span data-stu-id="98891-130">For selections that extend beyond the first 64 KB of text, the **EM\_GETSEL** message returns –1.</span></span> <span data-ttu-id="98891-131">在這種情況下，您仍然可以使用 *wParam* 和 *lParam* 中傳回的值來尋找選取專案的開頭和結尾字元。</span><span class="sxs-lookup"><span data-stu-id="98891-131">In such a case you can still use the values that are returned in *wParam* and *lParam* to find the start and end characters of the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98891-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="98891-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98891-133">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="98891-133">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="98891-134">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="98891-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




