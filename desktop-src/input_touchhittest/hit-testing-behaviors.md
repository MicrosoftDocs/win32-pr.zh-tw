---
title: 觸控點擊測試行為
description: 應用程式或 UI 架構會使用下列常數，來識別透過 RegisterTouchHitTestingWindow 函式註冊的 windows 如何處理觸控點擊測試的訊息。
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965928"
---
# <a name="touch-hit-testing-behaviors"></a><span data-ttu-id="1c2c0-103">觸控點擊測試行為</span><span class="sxs-lookup"><span data-stu-id="1c2c0-103">Touch Hit Testing Behaviors</span></span>

<span data-ttu-id="1c2c0-104">應用程式或 UI 架構會使用下列常數，來識別透過 [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) 函式註冊的 windows 如何處理觸控點擊測試的訊息。</span><span class="sxs-lookup"><span data-stu-id="1c2c0-104">The following constants are used by applications or UI frameworks to identify how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

| <span data-ttu-id="1c2c0-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="1c2c0-105">Constant/value</span></span> | <span data-ttu-id="1c2c0-106">Description</span><span class="sxs-lookup"><span data-stu-id="1c2c0-106">Description</span></span> |
|---|---|
| <span data-ttu-id="1c2c0-107">**TOUCH_HIT_TESTING_DEFAULT** </dt><dt>0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="1c2c0-107">**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</span></span> | <span data-ttu-id="1c2c0-108">指出 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 的訊息不會傳送至目標視窗，而是傳送至子視窗。</span><span class="sxs-lookup"><span data-stu-id="1c2c0-108">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span data-ttu-id="1c2c0-109">**TOUCH_HIT_TESTING_CLIENT** </dt><dt>1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="1c2c0-109">**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</span></span>    | <span data-ttu-id="1c2c0-110">指出 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 的訊息會傳送至目標視窗。</span><span class="sxs-lookup"><span data-stu-id="1c2c0-110">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span data-ttu-id="1c2c0-111">**TOUCH_HIT_TESTING_NONE** </dt><dt>2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="1c2c0-111">**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</span></span>          | <span data-ttu-id="1c2c0-112">指出 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 的訊息不會傳送至目標視窗或子視窗。</span><span class="sxs-lookup"><span data-stu-id="1c2c0-112">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |

## <a name="requirements"></a><span data-ttu-id="1c2c0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c2c0-113">Requirements</span></span>

| <span data-ttu-id="1c2c0-114">需求</span><span class="sxs-lookup"><span data-stu-id="1c2c0-114">Requirement</span></span> | <span data-ttu-id="1c2c0-115">值</span><span class="sxs-lookup"><span data-stu-id="1c2c0-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2c0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c2c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c2c0-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c2c0-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1c2c0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c2c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c2c0-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="1c2c0-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="1c2c0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1c2c0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c2c0-121"><dt>Winuser。h</span><span class="sxs-lookup"><span data-stu-id="1c2c0-121"><dt>Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="1c2c0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c2c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2c0-123">常數</span><span class="sxs-lookup"><span data-stu-id="1c2c0-123">Constants</span></span>](constants.md)
