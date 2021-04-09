---
title: 如何自動調整 Rich Edit 控制項的大小
description: 應用程式可以視需要調整 rich edit 控制項的大小，使其大小一律與內容相同。
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024184"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a><span data-ttu-id="48d6b-103">如何自動調整 Rich Edit 控制項的大小</span><span class="sxs-lookup"><span data-stu-id="48d6b-103">How to Automatically Resize Rich Edit Controls</span></span>

<span data-ttu-id="48d6b-104">應用程式可以視需要調整 rich edit 控制項的大小，使其大小一律與內容相同。</span><span class="sxs-lookup"><span data-stu-id="48d6b-104">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="48d6b-105">Rich edit 控制項支援這種所謂的 *無底邊* 功能，方法是在控制項內容的大小變更時，傳送一個 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知碼給其父視窗。</span><span class="sxs-lookup"><span data-stu-id="48d6b-105">A rich edit control supports this so-called *bottomless* functionality by sending its parent window an [EN\_REQUESTRESIZE](en-requestresize.md) notification code whenever the size of the control's content changes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="48d6b-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="48d6b-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="48d6b-107">技術</span><span class="sxs-lookup"><span data-stu-id="48d6b-107">Technologies</span></span>

-   [<span data-ttu-id="48d6b-108">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="48d6b-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="48d6b-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="48d6b-109">Prerequisites</span></span>

-   <span data-ttu-id="48d6b-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="48d6b-110">C/C++</span></span>
-   <span data-ttu-id="48d6b-111">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="48d6b-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="48d6b-112">指示</span><span class="sxs-lookup"><span data-stu-id="48d6b-112">Instructions</span></span>

### <a name="automatically-resize-a-rich-edit-control"></a><span data-ttu-id="48d6b-113">自動調整 Rich Edit 控制項的大小</span><span class="sxs-lookup"><span data-stu-id="48d6b-113">Automatically Resize a Rich Edit Control</span></span>

<span data-ttu-id="48d6b-114">處理 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知程式碼時，應用程式應該將控制項的大小調整為指定之 [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) 結構中的維度。</span><span class="sxs-lookup"><span data-stu-id="48d6b-114">When processing the [EN\_REQUESTRESIZE](en-requestresize.md) notification code, an application should resize the control to the dimensions in the specified [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure.</span></span> <span data-ttu-id="48d6b-115">應用程式也可能會移動接近控制項的任何資訊，以容納控制項的高度變更。</span><span class="sxs-lookup"><span data-stu-id="48d6b-115">An application might also move any information that is near the control to accommodate the control's change in height.</span></span> <span data-ttu-id="48d6b-116">若要調整控制項的大小，您可以使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函數。</span><span class="sxs-lookup"><span data-stu-id="48d6b-116">To resize the control, you can use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function.</span></span>

<span data-ttu-id="48d6b-117">您可以使用 [**EM \_ REQUESTRESIZE**](em-requestresize.md)訊息來強制無底邊 rich Edit 控制項傳送 [EN \_ REQUESTRESIZE](en-requestresize.md)通知碼。</span><span class="sxs-lookup"><span data-stu-id="48d6b-117">You can force a bottomless rich edit control to send an [EN\_REQUESTRESIZE](en-requestresize.md) notification code by using the [**EM\_REQUESTRESIZE**](em-requestresize.md) message.</span></span> <span data-ttu-id="48d6b-118">此訊息在處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息時可能很有用。</span><span class="sxs-lookup"><span data-stu-id="48d6b-118">This message can be useful when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

## <a name="remarks"></a><span data-ttu-id="48d6b-119">備註</span><span class="sxs-lookup"><span data-stu-id="48d6b-119">Remarks</span></span>

<span data-ttu-id="48d6b-120">若要接收 [EN \_ REQUESTRESIZE](en-requestresize.md) 通知碼，您必須使用 [EM \_ SETEVENTMASK](em-seteventmask.md) 訊息來啟用通知。</span><span class="sxs-lookup"><span data-stu-id="48d6b-120">To receive [EN\_REQUESTRESIZE](en-requestresize.md) notification codes, you must enable the notification by using the [EM\_SETEVENTMASK](em-seteventmask.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48d6b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="48d6b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48d6b-122">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="48d6b-122">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="48d6b-123">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="48d6b-123">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 