---
title: 'MCIWNDM_CHANGESTYLES 訊息 (Vfw .h) '
description: MCIWNDM \_ CHANGESTYLES 訊息會變更 MCIWnd 視窗所使用的樣式。 您可以使用 MCIWndChangeStyles 宏明確地傳送此訊息。
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996573"
---
# <a name="mciwndm_changestyles-message"></a><span data-ttu-id="c59b9-105">MCIWNDM \_ CHANGESTYLES 訊息</span><span class="sxs-lookup"><span data-stu-id="c59b9-105">MCIWNDM\_CHANGESTYLES message</span></span>

<span data-ttu-id="c59b9-106">**MCIWNDM \_ CHANGESTYLES** 訊息會變更 MCIWnd 視窗所使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="c59b9-106">The **MCIWNDM\_CHANGESTYLES** message changes the styles used by the MCIWnd window.</span></span> <span data-ttu-id="c59b9-107">您可以使用 [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c59b9-107">You can send this message explicitly or by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro.</span></span>


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a><span data-ttu-id="c59b9-108">參數</span><span class="sxs-lookup"><span data-stu-id="c59b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c59b9-109"><span id="mask"></span><span id="MASK"></span>*面具*</span><span class="sxs-lookup"><span data-stu-id="c59b9-109"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="c59b9-110">識別可變更之樣式的遮罩。</span><span class="sxs-lookup"><span data-stu-id="c59b9-110">Mask that identifies the styles that can change.</span></span> <span data-ttu-id="c59b9-111">這個遮罩是將允許變更之所有樣式的位 OR 運算子。</span><span class="sxs-lookup"><span data-stu-id="c59b9-111">This mask is the bitwise OR operator of all styles that will be permitted to change.</span></span>

</dd> <dt>

<span data-ttu-id="c59b9-112"><span id="value"></span><span id="VALUE"></span>*價值*</span><span class="sxs-lookup"><span data-stu-id="c59b9-112"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="c59b9-113">視窗的新樣式設定。</span><span class="sxs-lookup"><span data-stu-id="c59b9-113">New style settings for the window.</span></span> <span data-ttu-id="c59b9-114">針對此參數指定零，以關閉遮罩中識別的所有樣式。</span><span class="sxs-lookup"><span data-stu-id="c59b9-114">Specify zero for this parameter to turn off all styles identified in the mask.</span></span> <span data-ttu-id="c59b9-115">如需可用樣式的清單，請參閱 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函數。</span><span class="sxs-lookup"><span data-stu-id="c59b9-115">For a list of the available styles, see the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c59b9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c59b9-116">Return Value</span></span>

<span data-ttu-id="c59b9-117">傳回零。</span><span class="sxs-lookup"><span data-stu-id="c59b9-117">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c59b9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c59b9-118">Requirements</span></span>



| <span data-ttu-id="c59b9-119">需求</span><span class="sxs-lookup"><span data-stu-id="c59b9-119">Requirement</span></span> | <span data-ttu-id="c59b9-120">值</span><span class="sxs-lookup"><span data-stu-id="c59b9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c59b9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c59b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c59b9-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c59b9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c59b9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c59b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c59b9-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c59b9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c59b9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c59b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c59b9-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="c59b9-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59b9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c59b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59b9-128">**MCIWndCreate**</span><span class="sxs-lookup"><span data-stu-id="c59b9-128">**MCIWndCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[<span data-ttu-id="c59b9-129">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="c59b9-129">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





