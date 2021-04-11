---
description: 以下是筆觸常數。
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: '筆觸常數 (Tabflicks .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113420"
---
# <a name="flicks-constants"></a><span data-ttu-id="64d58-103">筆觸常數</span><span class="sxs-lookup"><span data-stu-id="64d58-103">Flicks Constants</span></span>

<span data-ttu-id="64d58-104">以下是筆觸常數。</span><span class="sxs-lookup"><span data-stu-id="64d58-104">The following are the Flicks constants.</span></span>



| <span data-ttu-id="64d58-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="64d58-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="64d58-106">Description</span><span class="sxs-lookup"><span data-stu-id="64d58-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <span data-ttu-id="64d58-107"><dt>**筆鋒 \_WM \_ 處理的 \_ 遮罩**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="64d58-107"><dt>**FLICK\_WM\_HANDLED\_MASK**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="64d58-108">處理 [**WM \_ TABLET \_ 筆鋒訊息**](wm-tablet-flick-message.md) 訊息之後要傳回的值。</span><span class="sxs-lookup"><span data-stu-id="64d58-108">The value to return after handling the [**WM\_TABLET\_FLICK Message**](wm-tablet-flick-message.md) message.</span></span> <span data-ttu-id="64d58-109">如果傳回了 [筆觸 **\_ WM \_ 處理的 \_ 遮罩** ]，就不會進行任何進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="64d58-109">If **FLICK\_WM\_HANDLED\_MASK** is returned, no further action occurs.</span></span> <span data-ttu-id="64d58-110">否則，Windows 會傳送後續通知（例如， [**wm \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand)、 [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)或 [**wm \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)），這取決於與筆觸相關聯的動作。</span><span class="sxs-lookup"><span data-stu-id="64d58-110">Otherwise, Windows sends follow-up notifications, such as [**WM\_APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll), or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown), depending on which action is associated with the pen flick.</span></span> <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <span data-ttu-id="64d58-111"><dt>**NUM \_筆鋒 \_ 方向**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="64d58-111"><dt>**NUM\_FLICK\_DIRECTIONS**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="64d58-112">在 [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) 列舉中定義的方向數目。</span><span class="sxs-lookup"><span data-stu-id="64d58-112">The number of directions defined in the [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) enumeration.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="64d58-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="64d58-113">Requirements</span></span>



| <span data-ttu-id="64d58-114">需求</span><span class="sxs-lookup"><span data-stu-id="64d58-114">Requirement</span></span> | <span data-ttu-id="64d58-115">值</span><span class="sxs-lookup"><span data-stu-id="64d58-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64d58-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64d58-116">Minimum supported client</span></span><br/> | <span data-ttu-id="64d58-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64d58-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64d58-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64d58-118">Minimum supported server</span></span><br/> | <span data-ttu-id="64d58-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64d58-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="64d58-120">標頭</span><span class="sxs-lookup"><span data-stu-id="64d58-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d58-121"><dt>Tabflicks。h</dt></span><span class="sxs-lookup"><span data-stu-id="64d58-121"><dt>Tabflicks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d58-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64d58-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d58-123">**FLICKDIRECTION 列舉**</span><span class="sxs-lookup"><span data-stu-id="64d58-123">**FLICKDIRECTION Enumeration**</span></span>](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[<span data-ttu-id="64d58-124">**WM \_ TABLET \_ 筆鋒訊息**</span><span class="sxs-lookup"><span data-stu-id="64d58-124">**WM\_TABLET\_FLICK Message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="64d58-125">筆觸手勢</span><span class="sxs-lookup"><span data-stu-id="64d58-125">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="64d58-126">[回應觸控筆觸](/previous-versions//dd356077(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64d58-126">[Responding to Pen Flicks](/previous-versions//dd356077(v=vs.85))</span></span>
</dt> </dl>

 

