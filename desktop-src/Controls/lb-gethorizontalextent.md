---
title: 'LB_GETHORIZONTALEXTENT 訊息 (Winuser .h) '
description: 取得清單方塊可水準滾動 (可滾動寬度的寬度（以圖元為單位）) 如果清單方塊具有水準捲軸。
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935014"
---
# <a name="lb_gethorizontalextent-message"></a><span data-ttu-id="b5bf2-104">LB \_ GETHORIZONTALEXTENT 訊息</span><span class="sxs-lookup"><span data-stu-id="b5bf2-104">LB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="b5bf2-105">取得清單方塊可水準滾動 (可滾動寬度的寬度（以圖元為單位）) 如果清單方塊具有水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="b5bf2-105">Gets the width, in pixels, that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5bf2-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5bf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5bf2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5bf2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5bf2-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b5bf2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5bf2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5bf2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5bf2-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b5bf2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5bf2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5bf2-111">Return value</span></span>

<span data-ttu-id="b5bf2-112">傳回值是清單方塊的可滾動寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5bf2-112">The return value is the scrollable width, in pixels, of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5bf2-113">備註</span><span class="sxs-lookup"><span data-stu-id="b5bf2-113">Remarks</span></span>

<span data-ttu-id="b5bf2-114">若要回應 **LB \_ GETHORIZONTALEXTENT** 訊息，必須使用 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式來定義清單方塊。</span><span class="sxs-lookup"><span data-stu-id="b5bf2-114">To respond to the **LB\_GETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="b5bf2-115">如果應用程式未設定清單方塊的水準範圍 (使用 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)) ，則預設的水準範圍為零。</span><span class="sxs-lookup"><span data-stu-id="b5bf2-115">If the application does not set the horizontal extent of the list box (using [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), the default horizontal extent is zero.</span></span> <span data-ttu-id="b5bf2-116">請注意，清單方塊不會動態更新其水準範圍。</span><span class="sxs-lookup"><span data-stu-id="b5bf2-116">Note that the list box does not update its horizontal extent dynamically.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5bf2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5bf2-117">Requirements</span></span>



| <span data-ttu-id="b5bf2-118">需求</span><span class="sxs-lookup"><span data-stu-id="b5bf2-118">Requirement</span></span> | <span data-ttu-id="b5bf2-119">值</span><span class="sxs-lookup"><span data-stu-id="b5bf2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5bf2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5bf2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5bf2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5bf2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5bf2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5bf2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5bf2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5bf2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5bf2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b5bf2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5bf2-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b5bf2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5bf2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5bf2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5bf2-127">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="b5bf2-127">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

