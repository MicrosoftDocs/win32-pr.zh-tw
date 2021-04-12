---
title: 如何控制 AVI 剪輯
description: 本主題將示範如何使用動畫控制項宏來播放、停止及關閉相關聯的 Audio-Video 交錯 (AVI) 剪輯。
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463965"
---
# <a name="how-to-control-the-avi-clip"></a><span data-ttu-id="396a1-103">如何控制 AVI 剪輯</span><span class="sxs-lookup"><span data-stu-id="396a1-103">How to Control the AVI Clip</span></span>

<span data-ttu-id="396a1-104">本主題將示範如何使用動畫控制項宏來播放、停止及關閉相關聯的 Audio-Video 交錯 (AVI) 剪輯。</span><span class="sxs-lookup"><span data-stu-id="396a1-104">This topic demonstrates how to use the animation control macros to play, stop, and close an associated Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="396a1-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="396a1-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="396a1-106">技術</span><span class="sxs-lookup"><span data-stu-id="396a1-106">Technologies</span></span>

-   [<span data-ttu-id="396a1-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="396a1-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="396a1-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="396a1-108">Prerequisites</span></span>

-   <span data-ttu-id="396a1-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="396a1-109">C/C++</span></span>
-   <span data-ttu-id="396a1-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="396a1-110">Windows User Interface Programming</span></span>
-   <span data-ttu-id="396a1-111">AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="396a1-111">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="396a1-112">指示</span><span class="sxs-lookup"><span data-stu-id="396a1-112">Instructions</span></span>


<span data-ttu-id="396a1-113">建立函式，此函式會將動畫控制項的控制碼作為參數，並使用旗標來指出要在相關聯的 AVI 剪輯上執行的動作。</span><span class="sxs-lookup"><span data-stu-id="396a1-113">Create a function that takes as parameters a handle to the animation control and a flag that indicates the action to be performed on the associated AVI clip.</span></span>

<span data-ttu-id="396a1-114">下列 c + + 範例中的函式會呼叫三個動畫控制項宏的其中一個 ([**動畫 \_ 播放**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)、[**動畫 \_ 停止**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)、根據 *nAction* 參數的值來建立 [**\_ 關閉**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) 的動畫。</span><span class="sxs-lookup"><span data-stu-id="396a1-114">The function in the following C++ example calls one of three animation control macros ([**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) based on the value of the *nAction* parameter.</span></span> <span data-ttu-id="396a1-115">與 AVI 剪輯相關聯之動畫控制項的控制碼，會透過 *hwndAnim* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="396a1-115">The handle to the animation control that is associated with the AVI clip is passed via the *hwndAnim* parameter.</span></span>


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a><span data-ttu-id="396a1-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="396a1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="396a1-117">關於動畫控制項</span><span class="sxs-lookup"><span data-stu-id="396a1-117">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="396a1-118">動畫控制項參考</span><span class="sxs-lookup"><span data-stu-id="396a1-118">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="396a1-119">使用動畫控制項</span><span class="sxs-lookup"><span data-stu-id="396a1-119">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="396a1-120">動畫控制項</span><span class="sxs-lookup"><span data-stu-id="396a1-120">Animation Control</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




