---
title: 'CB_GETHORIZONTALEXTENT 訊息 (Winuser .h) '
description: 取得清單方塊可水準滾動 (可滾動寬度) 的寬度（以圖元為單位）。 只有在清單方塊具有水準捲軸時，才適用這種情況。
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- CB_GETHORIZONTALEXTENT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a2b1fb7c8fe7549360801516364528c9a2ef1f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025091"
---
# <a name="cb_gethorizontalextent-message"></a><span data-ttu-id="b5e1d-105">CB \_ GETHORIZONTALEXTENT 訊息</span><span class="sxs-lookup"><span data-stu-id="b5e1d-105">CB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="b5e1d-106">取得清單方塊可水準滾動 (可滾動寬度) 的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5e1d-106">Gets the width, in pixels, that the list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="b5e1d-107">只有在清單方塊具有水準捲軸時，才適用這種情況。</span><span class="sxs-lookup"><span data-stu-id="b5e1d-107">This is applicable only if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5e1d-108">參數</span><span class="sxs-lookup"><span data-stu-id="b5e1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5e1d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5e1d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5e1d-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b5e1d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5e1d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5e1d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5e1d-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b5e1d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5e1d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5e1d-113">Return value</span></span>

<span data-ttu-id="b5e1d-114">傳回值是可滾動的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5e1d-114">The return value is the scrollable width, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5e1d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5e1d-115">Requirements</span></span>



| <span data-ttu-id="b5e1d-116">需求</span><span class="sxs-lookup"><span data-stu-id="b5e1d-116">Requirement</span></span> | <span data-ttu-id="b5e1d-117">值</span><span class="sxs-lookup"><span data-stu-id="b5e1d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e1d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5e1d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5e1d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5e1d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5e1d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5e1d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5e1d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5e1d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5e1d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b5e1d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5e1d-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b5e1d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5e1d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5e1d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e1d-125">**CB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="b5e1d-125">**CB\_SETHORIZONTALEXTENT**</span></span>](cb-sethorizontalextent.md)
</dt> </dl>

 

 





