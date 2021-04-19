---
title: 如何使用 SysLink 通知
description: 有兩個通知訊息與 SysLink control \ 郵件相關聯，一個用於滑鼠 (NM \_ 按一下 (SysLink) ) ，另一個則是鍵盤 (NM 傳回 \_) 。
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "106967882"
---
# <a name="how-to-use-syslink-notifications"></a><span data-ttu-id="bfadc-103">如何使用 SysLink 通知</span><span class="sxs-lookup"><span data-stu-id="bfadc-103">How to Use SysLink Notifications</span></span>

<span data-ttu-id="bfadc-104">有兩個通知訊息與 SysLink 控制項相關聯—一個用於滑鼠 ([nm \_ 按一下 (SysLink) ](nm-click-syslink.md)) ，另一個則是鍵盤 ([NM \_ 傳回](nm-return.md)) 。</span><span class="sxs-lookup"><span data-stu-id="bfadc-104">There are two notification messages associated with the SysLink control—one for the mouse ([NM\_CLICK (syslink)](nm-click-syslink.md)), and one for the keyboard ([NM\_RETURN](nm-return.md)).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bfadc-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="bfadc-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bfadc-106">技術</span><span class="sxs-lookup"><span data-stu-id="bfadc-106">Technologies</span></span>

-   [<span data-ttu-id="bfadc-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="bfadc-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bfadc-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="bfadc-108">Prerequisites</span></span>

-   <span data-ttu-id="bfadc-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="bfadc-109">C/C++</span></span>
-   <span data-ttu-id="bfadc-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="bfadc-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bfadc-111">指示</span><span class="sxs-lookup"><span data-stu-id="bfadc-111">Instructions</span></span>

### <a name="use-syslink-notifications"></a><span data-ttu-id="bfadc-112">使用 SysLink 通知</span><span class="sxs-lookup"><span data-stu-id="bfadc-112">Use SysLink Notifications</span></span>

<span data-ttu-id="bfadc-113">下列範例程式碼示範如何處理當使用者按下 [一個範例](create-syslink-controls.md)中的兩個連結之一時，所產生的 SysLink 通知。</span><span class="sxs-lookup"><span data-stu-id="bfadc-113">The following example code shows how to process the SysLink notifications that are generated when the user clicks either of the two links in the [previous example](create-syslink-controls.md).</span></span> <span data-ttu-id="bfadc-114">當使用者按一下網際網路 URL 時，會在預設瀏覽器中開啟相關聯的網頁。</span><span class="sxs-lookup"><span data-stu-id="bfadc-114">When the user clicks the Internet URL, the associated webpage opens in the default browser.</span></span> <span data-ttu-id="bfadc-115">當使用者按一下應用程式定義的超連結時，會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="bfadc-115">When the user clicks the application-defined hyperlink, a message box is displayed.</span></span>


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a><span data-ttu-id="bfadc-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfadc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfadc-117">使用 SysLink 控制項</span><span class="sxs-lookup"><span data-stu-id="bfadc-117">Using SysLink Controls</span></span>](using-syslink-controls.md)
</dt> <dt>

<span data-ttu-id="bfadc-118">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bfadc-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




