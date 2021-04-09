---
title: 如何使用 Rich Edit 剪貼簿作業
description: 應用程式可以使用最適合的剪貼簿格式或特定的剪貼簿格式，將剪貼簿的內容貼入 rich edit 控制項。
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933661"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a><span data-ttu-id="65bc7-103">如何使用 Rich Edit 剪貼簿作業</span><span class="sxs-lookup"><span data-stu-id="65bc7-103">How to Use Rich Edit Clipboard Operations</span></span>

<span data-ttu-id="65bc7-104">應用程式可以使用最適合的剪貼簿格式或特定的剪貼簿格式，將剪貼簿的內容貼入 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="65bc7-104">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="65bc7-105">您也可以判斷 rich edit 控制項是否能夠貼上剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="65bc7-105">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="65bc7-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="65bc7-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="65bc7-107">技術</span><span class="sxs-lookup"><span data-stu-id="65bc7-107">Technologies</span></span>

-   [<span data-ttu-id="65bc7-108">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="65bc7-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="65bc7-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="65bc7-109">Prerequisites</span></span>

-   <span data-ttu-id="65bc7-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="65bc7-110">C/C++</span></span>
-   <span data-ttu-id="65bc7-111">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="65bc7-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="65bc7-112">指示</span><span class="sxs-lookup"><span data-stu-id="65bc7-112">Instructions</span></span>

### <a name="use-a-rich-edit-clipboard-operation"></a><span data-ttu-id="65bc7-113">使用 Rich Edit 剪貼簿操作</span><span class="sxs-lookup"><span data-stu-id="65bc7-113">Use a Rich Edit Clipboard Operation</span></span>

<span data-ttu-id="65bc7-114">如同編輯控制項，您可以使用 [**wm \_ 複製**](/windows/desktop/dataxchg/wm-copy) 或 [**wm \_ 剪**](/windows/desktop/dataxchg/wm-cut) 下訊息來複製或剪下目前選取範圍的內容。</span><span class="sxs-lookup"><span data-stu-id="65bc7-114">As with an edit control, you can copy or cut the contents of the current selection by using the [**WM\_COPY**](/windows/desktop/dataxchg/wm-copy) or [**WM\_CUT**](/windows/desktop/dataxchg/wm-cut) message.</span></span> <span data-ttu-id="65bc7-115">同樣地，您可以使用 [**WM \_ 貼**](/windows/desktop/dataxchg/wm-paste) 上訊息，將剪貼簿的內容貼入 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="65bc7-115">Similarly, you can paste the contents of the clipboard into a rich edit control by using the [**WM\_PASTE**](/windows/desktop/dataxchg/wm-paste) message.</span></span> <span data-ttu-id="65bc7-116">控制項會先貼上其所辨識的第一個可用的格式，這大概會是最具描述性的格式。</span><span class="sxs-lookup"><span data-stu-id="65bc7-116">The control pastes the first available format that it recognizes, which presumably is the most descriptive format.</span></span>

<span data-ttu-id="65bc7-117">若要貼上特定的剪貼簿格式，您可以使用 [**EM \_ PASTESPECIAL**](em-pastespecial.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="65bc7-117">To paste a specific clipboard format, you can use the [**EM\_PASTESPECIAL**](em-pastespecial.md) message.</span></span> <span data-ttu-id="65bc7-118">這則訊息適用于具有 [貼上] **特殊** 命令的應用程式，可讓使用者選取 [剪貼簿] 格式。</span><span class="sxs-lookup"><span data-stu-id="65bc7-118">This message is useful for applications with a **Paste Special** command that enables the user to select the clipboard format.</span></span> <span data-ttu-id="65bc7-119">您可以使用 [**EM \_ CANPASTE**](em-canpaste.md) 訊息來判斷控制項是否能辨識指定的格式。</span><span class="sxs-lookup"><span data-stu-id="65bc7-119">You can use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether a given format is recognized by the control.</span></span>

<span data-ttu-id="65bc7-120">您也可以使用 [**EM \_ CANPASTE**](em-canpaste.md) 訊息來判斷 rich edit 控制項是否能辨識任何可用的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="65bc7-120">You can also use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether any available clipboard format is recognized by a rich edit control.</span></span> <span data-ttu-id="65bc7-121">此訊息在處理 [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) 訊息時很有用。</span><span class="sxs-lookup"><span data-stu-id="65bc7-121">This message is useful when processing the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message.</span></span> <span data-ttu-id="65bc7-122">應用程式可能會根據控制項是否可以貼上任何可用的格式，來啟用或使其 **貼** 上命令變成灰色。</span><span class="sxs-lookup"><span data-stu-id="65bc7-122">An application might enable or gray its **Paste** command depending on whether the control can paste any available format.</span></span>

<span data-ttu-id="65bc7-123">Rich edit 控制項會註冊兩個剪貼簿格式：</span><span class="sxs-lookup"><span data-stu-id="65bc7-123">Rich edit controls register two clipboard formats:</span></span>

-   <span data-ttu-id="65bc7-124">Rich Text 格式</span><span class="sxs-lookup"><span data-stu-id="65bc7-124">Rich Text Format</span></span>
-   <span data-ttu-id="65bc7-125">沒有物件的 Rich Text 格式</span><span class="sxs-lookup"><span data-stu-id="65bc7-125">Rich Text Format Without Objects</span></span>
-   <span data-ttu-id="65bc7-126">RichEdit 文字和物件</span><span class="sxs-lookup"><span data-stu-id="65bc7-126">RichEdit Text and Objects</span></span>

<span data-ttu-id="65bc7-127">應用程式可以使用 [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) 函式來註冊這些格式，指定 cf \_ RTF、CF \_ RTFNOOBJS 和 cf \_ RETEXTOBJ 值。</span><span class="sxs-lookup"><span data-stu-id="65bc7-127">An application can register these formats by using the [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) function, specifying the CF\_RTF, CF\_RTFNOOBJS, and CF\_RETEXTOBJ values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65bc7-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="65bc7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65bc7-129">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="65bc7-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="65bc7-130">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="65bc7-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 