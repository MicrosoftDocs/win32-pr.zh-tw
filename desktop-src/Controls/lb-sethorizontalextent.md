---
title: 'LB_SETHORIZONTALEXTENT 訊息 (Winuser .h) '
description: 設定以圖元為單位的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844111"
---
# <a name="lb_sethorizontalextent-message"></a><span data-ttu-id="2e590-104">LB \_ SETHORIZONTALEXTENT 訊息</span><span class="sxs-lookup"><span data-stu-id="2e590-104">LB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="2e590-105">設定以圖元為單位的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。</span><span class="sxs-lookup"><span data-stu-id="2e590-105">Sets the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="2e590-106">如果清單方塊的寬度小於此值，水準捲軸會水準滾動清單方塊中的專案。</span><span class="sxs-lookup"><span data-stu-id="2e590-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="2e590-107">如果清單方塊的寬度等於或大於此值，則會隱藏水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="2e590-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e590-108">參數</span><span class="sxs-lookup"><span data-stu-id="2e590-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e590-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e590-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e590-110">指定清單方塊可滾動的圖元數。</span><span class="sxs-lookup"><span data-stu-id="2e590-110">Specifies the number of pixels by which the list box can be scrolled.</span></span>

<span data-ttu-id="2e590-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="2e590-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span>

</dd> <dt>

<span data-ttu-id="2e590-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e590-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e590-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2e590-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e590-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e590-114">Return value</span></span>

<span data-ttu-id="2e590-115">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2e590-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e590-116">備註</span><span class="sxs-lookup"><span data-stu-id="2e590-116">Remarks</span></span>

<span data-ttu-id="2e590-117">若要回應 **LB \_ SETHORIZONTALEXTENT** 訊息，必須使用 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式來定義清單方塊。</span><span class="sxs-lookup"><span data-stu-id="2e590-117">To respond to the **LB\_SETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="2e590-118">請注意，清單方塊不會動態更新其水準範圍。</span><span class="sxs-lookup"><span data-stu-id="2e590-118">Note that a list box does not update its horizontal extent dynamically.</span></span>

<span data-ttu-id="2e590-119">此訊息對多欄清單方塊沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="2e590-119">This message has no effect on a multiple-column list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e590-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e590-120">Requirements</span></span>



| <span data-ttu-id="2e590-121">需求</span><span class="sxs-lookup"><span data-stu-id="2e590-121">Requirement</span></span> | <span data-ttu-id="2e590-122">值</span><span class="sxs-lookup"><span data-stu-id="2e590-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e590-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e590-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2e590-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e590-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e590-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e590-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2e590-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e590-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e590-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2e590-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e590-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2e590-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e590-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e590-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e590-130">**LB \_ GETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="2e590-130">**LB\_GETHORIZONTALEXTENT**</span></span>](lb-gethorizontalextent.md)
</dt> </dl>

 

