---
title: 如何建立跟蹤條
description: 建立程式時，會初始化其範圍及其選取範圍。 此時也會設定頁面大小。
ms.assetid: FA110B4A-D3D7-49D8-A3DC-368099F6DA1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9468ff044b94837f54d04cda4a9105f15410692
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021024"
---
# <a name="how-to-create-a-trackbar"></a><span data-ttu-id="61084-104">如何建立跟蹤條</span><span class="sxs-lookup"><span data-stu-id="61084-104">How to Create a Trackbar</span></span>

<span data-ttu-id="61084-105">建立程式時，會初始化其範圍及其選取範圍。</span><span class="sxs-lookup"><span data-stu-id="61084-105">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="61084-106">此時也會設定頁面大小。</span><span class="sxs-lookup"><span data-stu-id="61084-106">The page size is also set at this time.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="61084-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="61084-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="61084-108">技術</span><span class="sxs-lookup"><span data-stu-id="61084-108">Technologies</span></span>

-   [<span data-ttu-id="61084-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="61084-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="61084-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="61084-110">Prerequisites</span></span>

-   <span data-ttu-id="61084-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="61084-111">C/C++</span></span>
-   <span data-ttu-id="61084-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="61084-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="61084-113">指示</span><span class="sxs-lookup"><span data-stu-id="61084-113">Instructions</span></span>

### <a name="create-a-trackbar"></a><span data-ttu-id="61084-114">建立跟蹤條</span><span class="sxs-lookup"><span data-stu-id="61084-114">Create a Trackbar</span></span>

<span data-ttu-id="61084-115">下列範例示範如何建立具有 [**tb \_ AUTOTICKS**](trackbar-control-styles.md) 和 [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) 樣式的顯示。</span><span class="sxs-lookup"><span data-stu-id="61084-115">The following example shows how to create a trackbar with the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) and [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) styles.</span></span>


```
// CreateTrackbar - creates and initializes a trackbar. 
// 
// Global variable
//     g_hinst - instance handle
//
HWND WINAPI CreateTrackbar( 
    HWND hwndDlg,  // handle of dialog box (parent window) 
    UINT iMin,     // minimum value in trackbar range 
    UINT iMax,     // maximum value in trackbar range 
    UINT iSelMin,  // minimum value in trackbar selection 
    UINT iSelMax)  // maximum value in trackbar selection 
{ 

    InitCommonControls(); // loads common control's DLL 

    hwndTrack = CreateWindowEx( 
        0,                               // no extended styles 
        TRACKBAR_CLASS,                  // class name 
        "Trackbar Control",              // title (caption) 
        WS_CHILD | 
        WS_VISIBLE | 
        TBS_AUTOTICKS | 
        TBS_ENABLESELRANGE,              // style 
        10, 10,                          // position 
        200, 30,                         // size 
        hwndDlg,                         // parent window 
        ID_TRACKBAR,                     // control identifier 
        g_hinst,                         // instance 
        NULL                             // no WM_CREATE parameter 
        ); 

    SendMessage(hwndTrack, TBM_SETRANGE, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) MAKELONG(iMin, iMax));  // min. & max. positions
        
    SendMessage(hwndTrack, TBM_SETPAGESIZE, 
        0, (LPARAM) 4);                  // new page size 

    SendMessage(hwndTrack, TBM_SETSEL, 
        (WPARAM) FALSE,                  // redraw flag 
        (LPARAM) MAKELONG(iSelMin, iSelMax)); 
        
    SendMessage(hwndTrack, TBM_SETPOS, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) iSelMin); 

    SetFocus(hwndTrack); 

    return hwndTrack; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="61084-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="61084-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="61084-117">[使用 [使用] 控制項](using-trackbar-controls.md)</span><span class="sxs-lookup"><span data-stu-id="61084-117">[Using Trackbar Controls](using-trackbar-controls.md)</span></span>
</dt> </dl>

 

 




