---
title: 如何使用 Rich Edit 控制項通知碼
description: Rich edit 控制項的父視窗可以處理通知碼來監視影響控制項的事件。 Rich edit 控制項支援與編輯控制項搭配使用的所有通知碼，以及數個其他專案。
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103933029"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a><span data-ttu-id="d4871-104">如何使用 Rich Edit 控制項通知碼</span><span class="sxs-lookup"><span data-stu-id="d4871-104">How to Use Rich Edit Control Notification Codes</span></span>

<span data-ttu-id="d4871-105">Rich edit 控制項的父視窗可以處理通知碼來監視影響控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="d4871-105">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="d4871-106">Rich edit 控制項支援與編輯控制項搭配使用的所有通知碼，以及數個其他專案。</span><span class="sxs-lookup"><span data-stu-id="d4871-106">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d4871-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d4871-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d4871-108">技術</span><span class="sxs-lookup"><span data-stu-id="d4871-108">Technologies</span></span>

-   [<span data-ttu-id="d4871-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d4871-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d4871-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="d4871-110">Prerequisites</span></span>

-   <span data-ttu-id="d4871-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d4871-111">C/C++</span></span>
-   <span data-ttu-id="d4871-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d4871-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d4871-113">指示</span><span class="sxs-lookup"><span data-stu-id="d4871-113">Instructions</span></span>

### <a name="use-a-rich-edit-control-notification-code"></a><span data-ttu-id="d4871-114">使用 Rich Edit 控制項通知碼</span><span class="sxs-lookup"><span data-stu-id="d4871-114">Use a Rich Edit Control Notification Code</span></span>

<span data-ttu-id="d4871-115">您可以藉由設定其事件遮罩，判斷 rich edit 控制項傳送其父視窗的通知碼。</span><span class="sxs-lookup"><span data-stu-id="d4871-115">You can determine which notification codes a rich edit control sends its parent window by setting its event mask.</span></span> <span data-ttu-id="d4871-116">若要設定 rich edit 控制項的事件遮罩，請使用 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d4871-116">To set the event mask for a rich edit control, use the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="d4871-117">您可以使用 [**EM \_ GETEVENTMASK**](em-geteventmask.md) 訊息來取得 rich edit 控制項的目前事件遮罩。</span><span class="sxs-lookup"><span data-stu-id="d4871-117">You can retrieve the current event mask for a rich edit control by using the [**EM\_GETEVENTMASK**](em-geteventmask.md) message.</span></span> <span data-ttu-id="d4871-118">如需事件遮罩旗標的清單，請參閱 [Rich Edit 控制項事件遮罩旗標](rich-edit-control-event-mask-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="d4871-118">For a list of event mask flags, see [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span></span>

<span data-ttu-id="d4871-119">Rich edit 控制項的父視窗可以藉由處理 [ \_ MSGFILTER](en-msgfilter.md) 通知程式碼，來篩選控制項的所有鍵盤和滑鼠輸入。</span><span class="sxs-lookup"><span data-stu-id="d4871-119">A rich edit control's parent window can filter all keyboard and mouse input to the control by processing the [EN\_MSGFILTER](en-msgfilter.md) notification code.</span></span> <span data-ttu-id="d4871-120">父視窗可以防止鍵盤或滑鼠訊息被處理，或是藉由修改指定的 [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) 結構來變更訊息。</span><span class="sxs-lookup"><span data-stu-id="d4871-120">The parent window can prevent the keyboard or mouse message from being processed or can change the message by modifying the specified [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure.</span></span>

<span data-ttu-id="d4871-121">應用程式可以處理 [En-us \_ 受保護](en-protected.md) 的通知碼，以偵測使用者何時嘗試修改受保護的文字。</span><span class="sxs-lookup"><span data-stu-id="d4871-121">An application can process the [EN\_PROTECTED](en-protected.md) notification code to detect when the user attempts to modify protected text.</span></span> <span data-ttu-id="d4871-122">若要將某個範圍的文字標示為受保護，您可以設定受保護的字元效果。</span><span class="sxs-lookup"><span data-stu-id="d4871-122">To mark a range of text as protected, you can set the protected character effect.</span></span>

<span data-ttu-id="d4871-123">您可以藉由處理 [ \_ DROPFILES](en-dropfiles.md) 通知程式碼，讓使用者在 rich edit 控制項中放置檔案。</span><span class="sxs-lookup"><span data-stu-id="d4871-123">You can enable the user to drop files in a rich edit control by processing the [EN\_DROPFILES](en-dropfiles.md) notification code.</span></span> <span data-ttu-id="d4871-124">指定的 [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) 結構包含要卸載之檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d4871-124">The specified [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure contains information about the files that are being dropped.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4871-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4871-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4871-126">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="d4871-126">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d4871-127">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d4871-127">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




