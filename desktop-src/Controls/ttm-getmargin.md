---
title: 'TTM_GETMARGIN 訊息 (Commctrl .h) '
description: 抓取工具提示視窗的頂端、左方、底端和右邊界設定。 邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- TTM_GETMARGIN message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934397"
---
# <a name="ttm_getmargin-message"></a><span data-ttu-id="71142-105">TTM \_ GETMARGIN 訊息</span><span class="sxs-lookup"><span data-stu-id="71142-105">TTM\_GETMARGIN message</span></span>

<span data-ttu-id="71142-106">抓取工具提示視窗的頂端、左方、底端和右邊界設定。</span><span class="sxs-lookup"><span data-stu-id="71142-106">Retrieves the top, left, bottom, and right margins set for a tooltip window.</span></span> <span data-ttu-id="71142-107">邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="71142-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="71142-108">參數</span><span class="sxs-lookup"><span data-stu-id="71142-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71142-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71142-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="71142-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="71142-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="71142-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71142-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71142-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收邊界資訊。</span><span class="sxs-lookup"><span data-stu-id="71142-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the margin information.</span></span> <span data-ttu-id="71142-113">**矩形** 結構的成員不會定義周框。</span><span class="sxs-lookup"><span data-stu-id="71142-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="71142-114">針對此訊息的目的，結構成員會以下面方式解讀：</span><span class="sxs-lookup"><span data-stu-id="71142-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="71142-115">值</span><span class="sxs-lookup"><span data-stu-id="71142-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="71142-116">意義</span><span class="sxs-lookup"><span data-stu-id="71142-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="71142-117"><dt>**top**</dt></span><span class="sxs-lookup"><span data-stu-id="71142-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="71142-118">上方框線和工具提示文字頂端之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="71142-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="71142-119"><dt>**離開**</dt></span><span class="sxs-lookup"><span data-stu-id="71142-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="71142-120">工具提示文字的左邊框線和左邊緣之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="71142-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="71142-121"><dt>**底部**</dt></span><span class="sxs-lookup"><span data-stu-id="71142-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="71142-122">下方框線和工具提示文字底端之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="71142-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="71142-123"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="71142-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="71142-124">工具提示文字右框線和右端之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="71142-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71142-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="71142-125">Return value</span></span>

<span data-ttu-id="71142-126">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="71142-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="71142-127">備註</span><span class="sxs-lookup"><span data-stu-id="71142-127">Remarks</span></span>

<span data-ttu-id="71142-128">當您建立工具提示控制項時，四個邊界都會預設為零。</span><span class="sxs-lookup"><span data-stu-id="71142-128">All four margins default to zero when you create the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="71142-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="71142-129">Requirements</span></span>



| <span data-ttu-id="71142-130">需求</span><span class="sxs-lookup"><span data-stu-id="71142-130">Requirement</span></span> | <span data-ttu-id="71142-131">值</span><span class="sxs-lookup"><span data-stu-id="71142-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71142-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71142-132">Minimum supported client</span></span><br/> | <span data-ttu-id="71142-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71142-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71142-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71142-134">Minimum supported server</span></span><br/> | <span data-ttu-id="71142-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71142-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71142-136">標頭</span><span class="sxs-lookup"><span data-stu-id="71142-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="71142-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="71142-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71142-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71142-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71142-139">**TTM \_ SETMARGIN**</span><span class="sxs-lookup"><span data-stu-id="71142-139">**TTM\_SETMARGIN**</span></span>](ttm-setmargin.md)
</dt> </dl>

 

