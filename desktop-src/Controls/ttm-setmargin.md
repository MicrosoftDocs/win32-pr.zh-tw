---
title: 'TTM_SETMARGIN 訊息 (Commctrl .h) '
description: 設定工具提示視窗的頂端、左方、下邊界和右邊界。 邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968165"
---
# <a name="ttm_setmargin-message"></a><span data-ttu-id="4b66b-105">TTM \_ SETMARGIN 訊息</span><span class="sxs-lookup"><span data-stu-id="4b66b-105">TTM\_SETMARGIN message</span></span>

<span data-ttu-id="4b66b-106">設定工具提示視窗的頂端、左方、下邊界和右邊界。</span><span class="sxs-lookup"><span data-stu-id="4b66b-106">Sets the top, left, bottom, and right margins for a tooltip window.</span></span> <span data-ttu-id="4b66b-107">邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b66b-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b66b-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b66b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b66b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b66b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4b66b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4b66b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4b66b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b66b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b66b-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含要設定的邊界資訊。</span><span class="sxs-lookup"><span data-stu-id="4b66b-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margin information to be set.</span></span> <span data-ttu-id="4b66b-113">**矩形** 結構的成員不會定義周框。</span><span class="sxs-lookup"><span data-stu-id="4b66b-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="4b66b-114">針對此訊息的目的，結構成員會以下面方式解讀：</span><span class="sxs-lookup"><span data-stu-id="4b66b-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="4b66b-115">值</span><span class="sxs-lookup"><span data-stu-id="4b66b-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="4b66b-116">意義</span><span class="sxs-lookup"><span data-stu-id="4b66b-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="4b66b-117"><dt>**top**</dt></span><span class="sxs-lookup"><span data-stu-id="4b66b-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="4b66b-118">上方框線和工具提示文字頂端之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b66b-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="4b66b-119"><dt>**離開**</dt></span><span class="sxs-lookup"><span data-stu-id="4b66b-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="4b66b-120">工具提示文字的左邊框線和左邊緣之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b66b-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="4b66b-121"><dt>**底部**</dt></span><span class="sxs-lookup"><span data-stu-id="4b66b-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="4b66b-122">下方框線和工具提示文字底端之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b66b-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="4b66b-123"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="4b66b-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="4b66b-124">工具提示文字右框線和右端之間的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b66b-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b66b-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b66b-125">Return value</span></span>

<span data-ttu-id="4b66b-126">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="4b66b-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b66b-127">備註</span><span class="sxs-lookup"><span data-stu-id="4b66b-127">Remarks</span></span>

<span data-ttu-id="4b66b-128">當應用程式在 Windows Vista 上執行，而且已啟用工具提示的視覺化樣式時，此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="4b66b-128">This message has no effect when the application runs on Windows Vista and visual styles are enabled for the tooltip.</span></span> <span data-ttu-id="4b66b-129">您可以使用 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)來停用工具提示的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="4b66b-129">You can disable visual styles for the tooltip by using [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b66b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b66b-130">Requirements</span></span>



| <span data-ttu-id="4b66b-131">需求</span><span class="sxs-lookup"><span data-stu-id="4b66b-131">Requirement</span></span> | <span data-ttu-id="4b66b-132">值</span><span class="sxs-lookup"><span data-stu-id="4b66b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b66b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b66b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4b66b-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b66b-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b66b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b66b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4b66b-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b66b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b66b-137">標頭</span><span class="sxs-lookup"><span data-stu-id="4b66b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b66b-138"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4b66b-138"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b66b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b66b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b66b-140">**TTM \_ GETMARGIN**</span><span class="sxs-lookup"><span data-stu-id="4b66b-140">**TTM\_GETMARGIN**</span></span>](ttm-getmargin.md)
</dt> </dl>

 

