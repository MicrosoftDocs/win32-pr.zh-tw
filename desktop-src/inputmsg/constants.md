---
title: 指標輸入訊息和通知常數
description: 本節中的主題提供指標輸入訊息和通知常數的參考規格。
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db54614e10c02cea5dfd4df9b7cf637abb3977c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106995131"
---
# <a name="pointer-input-messages-and-notifications-constants"></a><span data-ttu-id="1f924-103">指標輸入訊息和通知常數</span><span class="sxs-lookup"><span data-stu-id="1f924-103">Pointer Input Messages and Notifications constants</span></span>

<span data-ttu-id="1f924-104">本節中的主題提供 [指標輸入訊息和通知](messages-and-notifications-portal.md) 常數的參考規格。</span><span class="sxs-lookup"><span data-stu-id="1f924-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1f924-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="1f924-105">In this section</span></span>



| <span data-ttu-id="1f924-106">主題</span><span class="sxs-lookup"><span data-stu-id="1f924-106">Topic</span></span>                                                                             | <span data-ttu-id="1f924-107">描述</span><span class="sxs-lookup"><span data-stu-id="1f924-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f924-108">**輔助按鍵狀態**</span><span class="sxs-lookup"><span data-stu-id="1f924-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="1f924-109">指出產生輸入時按下的鍵盤輔助按鍵。</span><span class="sxs-lookup"><span data-stu-id="1f924-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="1f924-110">**畫筆旗標**</span><span class="sxs-lookup"><span data-stu-id="1f924-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="1f924-111">可以出現在 [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **penFlags** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="1f924-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="1f924-112">**畫筆遮罩**</span><span class="sxs-lookup"><span data-stu-id="1f924-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="1f924-113">可以出現在 [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **penMask** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="1f924-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="1f924-114">**指標裝置變更**</span><span class="sxs-lookup"><span data-stu-id="1f924-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="1f924-115">可以在 [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md)訊息的 *wParam* 參數中傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="1f924-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="1f924-116">**指標旗標**</span><span class="sxs-lookup"><span data-stu-id="1f924-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="1f924-117">可以出現在 [**POINTER_INFO**](/previous-versions/windows/desktop/api)結構的 **pointerFlags** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="1f924-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="1f924-118">**指標訊息旗標**</span><span class="sxs-lookup"><span data-stu-id="1f924-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="1f924-119">各種指標宏所使用的值 (查看 [宏](macros.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1f924-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="1f924-120">**觸控旗標**</span><span class="sxs-lookup"><span data-stu-id="1f924-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="1f924-121">可以出現在 [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)結構的 **touchFlags** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="1f924-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="1f924-122">**觸控點擊測試視窗**</span><span class="sxs-lookup"><span data-stu-id="1f924-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="1f924-123">指出透過 [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) 函式註冊的 windows 會如何處理觸控點擊測試的訊息。</span><span class="sxs-lookup"><span data-stu-id="1f924-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="1f924-124">**觸控遮罩**</span><span class="sxs-lookup"><span data-stu-id="1f924-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="1f924-125">可以出現在 [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)結構的 **touchMask** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="1f924-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="1f924-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f924-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f924-127">指標輸入訊息參考</span><span class="sxs-lookup"><span data-stu-id="1f924-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

