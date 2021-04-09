---
title: 如何使用好友視窗
description: 藉由將其他控制項設定為標題的合作者視窗，您就可以將這些控制項以標籤的形式自動放置在這些標題的結尾。
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eca9a4e3b3049f8d4cf7515879d91a096f5a9e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021282"
---
# <a name="how-to-use-buddy-windows"></a><span data-ttu-id="5cbb8-103">如何使用好友視窗</span><span class="sxs-lookup"><span data-stu-id="5cbb8-103">How to Use Buddy Windows</span></span>

<span data-ttu-id="5cbb8-104">藉由將其他控制項設定為標題的合作者視窗，您就可以將這些控制項以標籤的形式自動放置在這些標題的結尾。</span><span class="sxs-lookup"><span data-stu-id="5cbb8-104">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span>

<span data-ttu-id="5cbb8-105">下圖顯示水準和垂直的橫條，兩者都有靜態控制項做為合作者視窗。</span><span class="sxs-lookup"><span data-stu-id="5cbb8-105">The following illustration shows a horizontal and a vertical trackbar, both with static controls as buddy windows.</span></span>

![顯示具有水準橫條和垂直橫條之對話方塊的螢幕擷取畫面](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="5cbb8-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="5cbb8-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5cbb8-108">技術</span><span class="sxs-lookup"><span data-stu-id="5cbb8-108">Technologies</span></span>

-   [<span data-ttu-id="5cbb8-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="5cbb8-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5cbb8-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="5cbb8-110">Prerequisites</span></span>

-   <span data-ttu-id="5cbb8-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="5cbb8-111">C/C++</span></span>
-   <span data-ttu-id="5cbb8-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="5cbb8-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5cbb8-113">指示</span><span class="sxs-lookup"><span data-stu-id="5cbb8-113">Instructions</span></span>

### <a name="use-buddy-windows"></a><span data-ttu-id="5cbb8-114">使用好友視窗</span><span class="sxs-lookup"><span data-stu-id="5cbb8-114">Use Buddy Windows</span></span>

<span data-ttu-id="5cbb8-115">下列程式碼範例會建立如圖所示的好友視窗。</span><span class="sxs-lookup"><span data-stu-id="5cbb8-115">The following code example creates the buddy windows shown in the illustration.</span></span>


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a><span data-ttu-id="5cbb8-116">備註</span><span class="sxs-lookup"><span data-stu-id="5cbb8-116">Remarks</span></span>

<span data-ttu-id="5cbb8-117">**IDC \_>SLIDER1** 和 **IDC \_ slider2.value** 是 trackbars 在資源編輯器中建立的。</span><span class="sxs-lookup"><span data-stu-id="5cbb8-117">**IDC\_SLIDER1** and **IDC\_SLIDER2** are trackbars created in the resource editor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cbb8-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="5cbb8-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5cbb8-119">[使用 [使用] 控制項](using-trackbar-controls.md)</span><span class="sxs-lookup"><span data-stu-id="5cbb8-119">[Using Trackbar Controls](using-trackbar-controls.md)</span></span>
</dt> </dl>

 

 




