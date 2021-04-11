---
title: 'BM_GETIMAGE 訊息 (Winuser .h) '
description: 抓取影像的控制碼 (圖示或點陣圖) 與按鈕相關聯。
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317364"
---
# <a name="bm_getimage-message"></a><span data-ttu-id="e0f97-104">BM \_ GETIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="e0f97-104">BM\_GETIMAGE message</span></span>

<span data-ttu-id="e0f97-105">抓取影像的控制碼 (圖示或點陣圖) 與按鈕相關聯。</span><span class="sxs-lookup"><span data-stu-id="e0f97-105">Retrieves a handle to the image (icon or bitmap) associated with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0f97-106">參數</span><span class="sxs-lookup"><span data-stu-id="e0f97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f97-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0f97-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0f97-108">要與按鈕相關聯的影像類型。</span><span class="sxs-lookup"><span data-stu-id="e0f97-108">The type of image to associate with the button.</span></span> <span data-ttu-id="e0f97-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e0f97-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e0f97-110">值</span><span class="sxs-lookup"><span data-stu-id="e0f97-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="e0f97-111">意義</span><span class="sxs-lookup"><span data-stu-id="e0f97-111">Meaning</span></span>              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="e0f97-112"><dt>**影像 \_ 點陣圖**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f97-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl> | <span data-ttu-id="e0f97-113">點陣圖。</span><span class="sxs-lookup"><span data-stu-id="e0f97-113">A bitmap.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="e0f97-114"><dt>**影像 \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f97-114"><dt>**IMAGE\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="e0f97-115">圖示。</span><span class="sxs-lookup"><span data-stu-id="e0f97-115">An icon.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="e0f97-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0f97-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0f97-117">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e0f97-117">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f97-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0f97-118">Return value</span></span>

<span data-ttu-id="e0f97-119">傳回值是影像的控制碼（如果有的話）。否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e0f97-119">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f97-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0f97-120">Requirements</span></span>



| <span data-ttu-id="e0f97-121">需求</span><span class="sxs-lookup"><span data-stu-id="e0f97-121">Requirement</span></span> | <span data-ttu-id="e0f97-122">值</span><span class="sxs-lookup"><span data-stu-id="e0f97-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f97-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0f97-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f97-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0f97-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0f97-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0f97-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f97-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0f97-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e0f97-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e0f97-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0f97-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e0f97-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f97-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0f97-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0f97-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="e0f97-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0f97-131">**BM \_ SETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="e0f97-131">**BM\_SETIMAGE**</span></span>](bm-setimage.md)
</dt> <dt>

<span data-ttu-id="e0f97-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="e0f97-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0f97-133">按鈕</span><span class="sxs-lookup"><span data-stu-id="e0f97-133">Buttons</span></span>](buttons.md)
</dt> </dl>

 

 





