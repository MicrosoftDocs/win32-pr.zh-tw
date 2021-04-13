---
title: 'LVM_SCROLL 訊息 (Commctrl .h) '
description: 滾動清單視圖控制項的內容。 您可以明確地傳送此訊息，或使用 ListView \_ 滾動宏來傳送。
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465869"
---
# <a name="lvm_scroll-message"></a><span data-ttu-id="173e3-105">LVM \_ 捲軸訊息</span><span class="sxs-lookup"><span data-stu-id="173e3-105">LVM\_SCROLL message</span></span>

<span data-ttu-id="173e3-106">滾動清單視圖控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="173e3-106">Scrolls the content of a list-view control.</span></span> <span data-ttu-id="173e3-107">您可以明確地傳送此訊息，或使用 [**ListView \_ 滾動**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="173e3-107">You can send this message explicitly or by using the [**ListView\_Scroll**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="173e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="173e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="173e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="173e3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="173e3-110">**Int** 類型的值，指定相對於清單視圖內容目前位置的水準滾動量（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="173e3-110">Value of type **int** that specifies the amount of horizontal scrolling, in pixels, relative to the current position of the list view content.</span></span> <span data-ttu-id="173e3-111">如果清單視圖控制項在清單視圖中，此值會無條件進位到構成整個資料行之最接近的圖元數目。</span><span class="sxs-lookup"><span data-stu-id="173e3-111">If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column.</span></span>

</dd> <dt>

<span data-ttu-id="173e3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="173e3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="173e3-113">**Int** 類型的值，指定垂直捲動的數量（以圖元為單位），相對於清單視圖內容的目前位置。</span><span class="sxs-lookup"><span data-stu-id="173e3-113">Value of type **int** that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="173e3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="173e3-114">Return value</span></span>

<span data-ttu-id="173e3-115">如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="173e3-115">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="173e3-116">備註</span><span class="sxs-lookup"><span data-stu-id="173e3-116">Remarks</span></span>

<span data-ttu-id="173e3-117">當清單視圖控制項位於報表檢視時，控制項只能以整行遞增的方式垂直捲動。</span><span class="sxs-lookup"><span data-stu-id="173e3-117">When the list-view control is in report view, the control can only be scrolled vertically in whole line increments.</span></span> <span data-ttu-id="173e3-118">因此， *lParam* 參數將會舍入形成整行增量的最接近圖元數目。</span><span class="sxs-lookup"><span data-stu-id="173e3-118">Therefore, the *lParam* parameter will be rounded to the nearest number of pixels that form a whole line increment.</span></span> <span data-ttu-id="173e3-119">例如，如果線條的高度為16圖元，而針對 *lParam* 傳遞的是8，則清單會以16圖元滾動 (1 行) 。</span><span class="sxs-lookup"><span data-stu-id="173e3-119">For example, if the height of a line is 16 pixels and 8 is passed for *lParam*, the list will be scrolled by 16 pixels (1 line).</span></span> <span data-ttu-id="173e3-120">如果針對 *lParam* 傳遞7，此清單將會滾動 (0 行) 的0圖元。</span><span class="sxs-lookup"><span data-stu-id="173e3-120">If 7 is passed for *lParam*, the list will be scrolled 0 pixels (0 lines).</span></span>

## <a name="requirements"></a><span data-ttu-id="173e3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="173e3-121">Requirements</span></span>



| <span data-ttu-id="173e3-122">需求</span><span class="sxs-lookup"><span data-stu-id="173e3-122">Requirement</span></span> | <span data-ttu-id="173e3-123">值</span><span class="sxs-lookup"><span data-stu-id="173e3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="173e3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="173e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="173e3-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="173e3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="173e3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="173e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="173e3-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="173e3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="173e3-128">標頭</span><span class="sxs-lookup"><span data-stu-id="173e3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="173e3-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="173e3-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





