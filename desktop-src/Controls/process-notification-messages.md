---
title: 如何處理通知訊息
description: 屬性工作表會傳送 WM \_ 通知訊息，以從頁面中取出資訊，並通知頁面使用者動作。
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103681602"
---
# <a name="how-to-process-notification-messages"></a><span data-ttu-id="a9643-103">如何處理通知訊息</span><span class="sxs-lookup"><span data-stu-id="a9643-103">How to Process Notification Messages</span></span>

<span data-ttu-id="a9643-104">屬性工作表會傳送 [**WM \_ 通知**](wm-notify.md) 訊息，以從頁面中取出資訊，並通知頁面使用者動作。</span><span class="sxs-lookup"><span data-stu-id="a9643-104">A property sheet sends [**WM\_NOTIFY**](wm-notify.md) messages to retrieve information from the pages and to notify the pages of user actions.</span></span>

<span data-ttu-id="a9643-105">訊息的 *lParam* 參數是 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構的位址，其中包含 [屬性工作表] 對話方塊的控制碼、頁面對話方塊的控制碼，以及通知碼。</span><span class="sxs-lookup"><span data-stu-id="a9643-105">The *lParam* parameter of the message is the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, which contains the handle to the property sheet dialog box, the handle to the page dialog box, and a notification code.</span></span> <span data-ttu-id="a9643-106">頁面必須藉由將頁面的 DWL \_ MSGRESULT 值設定為 **TRUE** 或 **FALSE**，來回應某些通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a9643-106">The page must respond to some notification messages by setting the DWL\_MSGRESULT value of the page to either **TRUE** or **FALSE**.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a9643-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="a9643-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a9643-108">技術</span><span class="sxs-lookup"><span data-stu-id="a9643-108">Technologies</span></span>

-   [<span data-ttu-id="a9643-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="a9643-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a9643-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="a9643-110">Prerequisites</span></span>

-   <span data-ttu-id="a9643-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a9643-111">C/C++</span></span>
-   <span data-ttu-id="a9643-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="a9643-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a9643-113">指示</span><span class="sxs-lookup"><span data-stu-id="a9643-113">Instructions</span></span>

### <a name="process-notification-messages"></a><span data-ttu-id="a9643-114">處理通知訊息</span><span class="sxs-lookup"><span data-stu-id="a9643-114">Process Notification Messages</span></span>

<span data-ttu-id="a9643-115">下列範例是來自頁面之對話方塊程式的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="a9643-115">The following example is a code fragment from the dialog box procedure for a page.</span></span> <span data-ttu-id="a9643-116">它會示範如何處理 [PSN 說明 \_ ](psn-help.md) 通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="a9643-116">It shows how to process the [PSN\_HELP](psn-help.md) notification code.</span></span>


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a><span data-ttu-id="a9643-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9643-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9643-118">使用屬性工作表</span><span class="sxs-lookup"><span data-stu-id="a9643-118">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="a9643-119">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a9643-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




