---
title: 如何限制滑杆移動
description: 如關於敘述區控制項中所述，您可以將部分的部分部分的資料格範圍設定為選取範圍。 選取範圍的其中一個用途，就是限制滑杆的移動，讓部分的完整範圍超出限制。
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839591"
---
# <a name="how-to-limit-slider-movement"></a><span data-ttu-id="80751-104">如何限制滑杆移動</span><span class="sxs-lookup"><span data-stu-id="80751-104">How to Limit Slider Movement</span></span>

<span data-ttu-id="80751-105">如關於敘述區 [控制項](trackbar-controls.md)中所述，您可以將部分的部分部分的資料格範圍設定為選取範圍。</span><span class="sxs-lookup"><span data-stu-id="80751-105">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="80751-106">選取範圍的其中一個用途，就是限制滑杆的移動，讓部分的完整範圍超出限制。</span><span class="sxs-lookup"><span data-stu-id="80751-106">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="80751-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="80751-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="80751-108">技術</span><span class="sxs-lookup"><span data-stu-id="80751-108">Technologies</span></span>

-   [<span data-ttu-id="80751-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="80751-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="80751-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="80751-110">Prerequisites</span></span>

-   <span data-ttu-id="80751-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="80751-111">C/C++</span></span>
-   <span data-ttu-id="80751-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="80751-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="80751-113">指示</span><span class="sxs-lookup"><span data-stu-id="80751-113">Instructions</span></span>

### <a name="limit-slider-movement"></a><span data-ttu-id="80751-114">限制滑杆移動</span><span class="sxs-lookup"><span data-stu-id="80751-114">Limit Slider Movement</span></span>

<span data-ttu-id="80751-115">下列範例程式碼會在移動滑杆的位置超出選取範圍時，重設滑杆的位置，藉此限制滑杆的移動。</span><span class="sxs-lookup"><span data-stu-id="80751-115">The following example code limits movement of the slider by resetting the slider's position whenever it is moved outside the selection range.</span></span>


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a><span data-ttu-id="80751-116">備註</span><span class="sxs-lookup"><span data-stu-id="80751-116">Remarks</span></span>

<span data-ttu-id="80751-117">此程式碼片段會是對話方塊視窗程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="80751-117">This code snippet would be part of a dialog box's Window Procedure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80751-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="80751-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="80751-119">[使用 [使用] 控制項](using-trackbar-controls.md)</span><span class="sxs-lookup"><span data-stu-id="80751-119">[Using Trackbar Controls](using-trackbar-controls.md)</span></span>
</dt> </dl>

 

 




