---
title: 'EM_SETPAGEROTATE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的文字版面配置。
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- EM_SETPAGEROTATE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934275"
---
# <a name="em_setpagerotate-message"></a><span data-ttu-id="5ff2b-104">EM \_ SETPAGEROTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="5ff2b-104">EM\_SETPAGEROTATE message</span></span>

<span data-ttu-id="5ff2b-105">\[**EM \_SETPAGEROTATE** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-105">\[**EM\_SETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5ff2b-106">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5ff2b-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="5ff2b-107">設定 rich edit 控制項的文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-107">Sets the text layout for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ff2b-108">參數</span><span class="sxs-lookup"><span data-stu-id="5ff2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff2b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ff2b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ff2b-110">文字版面配置值。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-110">Text layout value.</span></span> <span data-ttu-id="5ff2b-111">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-111">This can be one of the following values.</span></span>



| <span data-ttu-id="5ff2b-112">值</span><span class="sxs-lookup"><span data-stu-id="5ff2b-112">Value</span></span>                                                                                                                                       | <span data-ttu-id="5ff2b-113">意義</span><span class="sxs-lookup"><span data-stu-id="5ff2b-113">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <span data-ttu-id="5ff2b-114"><dt>**EPR \_ 0**</dt></span><span class="sxs-lookup"><span data-stu-id="5ff2b-114"><dt>**EPR\_0**</dt></span></span> </dl>       | <span data-ttu-id="5ff2b-115">文字會從左至右，以及從上到下。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-115">Text flows from left to right and from top to bottom.</span></span><br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <span data-ttu-id="5ff2b-116"><dt>**EPR \_ 90**</dt></span><span class="sxs-lookup"><span data-stu-id="5ff2b-116"><dt>**EPR\_90**</dt></span></span> </dl>    | <span data-ttu-id="5ff2b-117">文字會從下到上，從左至右流動。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-117">Text flows from bottom to top and from left to right.</span></span><br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <span data-ttu-id="5ff2b-118"><dt>**EPR \_ 180**</dt></span><span class="sxs-lookup"><span data-stu-id="5ff2b-118"><dt>**EPR\_180**</dt></span></span> </dl> | <span data-ttu-id="5ff2b-119">文字會從右至左，從下到上流動。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-119">Text flows from right to left and from bottom to top.</span></span><br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <span data-ttu-id="5ff2b-120"><dt>**EPR \_ 270**</dt></span><span class="sxs-lookup"><span data-stu-id="5ff2b-120"><dt>**EPR\_270**</dt></span></span> </dl> | <span data-ttu-id="5ff2b-121">文字會從上到下，從右至左流動。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-121">Text flows from top to bottom and from right to left.</span></span><br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <span data-ttu-id="5ff2b-122"><dt>**EPR \_ SE**</dt></span><span class="sxs-lookup"><span data-stu-id="5ff2b-122"><dt>**EPR\_SE**</dt></span></span> </dl>    | <span data-ttu-id="5ff2b-123">**Windows 8：** 文字流程由上到下，由左至右 (蒙古文字配置) 。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-123">**Windows 8:** Text flows top to bottom and left to right (Mongolian text layout).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5ff2b-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ff2b-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ff2b-125">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-125">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff2b-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ff2b-126">Return value</span></span>

<span data-ttu-id="5ff2b-127">傳回值是新的文字版面配置值。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-127">Return value is the new text layout value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff2b-128">備註</span><span class="sxs-lookup"><span data-stu-id="5ff2b-128">Remarks</span></span>

<span data-ttu-id="5ff2b-129">這則訊息會設定整份檔的文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-129">This message sets the text layout for the entire document.</span></span> <span data-ttu-id="5ff2b-130">不過，內嵌的內容不會旋轉，且必須由應用程式分開旋轉。</span><span class="sxs-lookup"><span data-stu-id="5ff2b-130">However, embedded contents are not rotated and must be rotated separately by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff2b-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ff2b-131">Requirements</span></span>



| <span data-ttu-id="5ff2b-132">需求</span><span class="sxs-lookup"><span data-stu-id="5ff2b-132">Requirement</span></span> | <span data-ttu-id="5ff2b-133">值</span><span class="sxs-lookup"><span data-stu-id="5ff2b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff2b-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ff2b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff2b-135">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ff2b-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ff2b-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ff2b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff2b-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ff2b-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ff2b-138">標頭</span><span class="sxs-lookup"><span data-stu-id="5ff2b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ff2b-139"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff2b-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff2b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ff2b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff2b-141">**EM \_ GETPAGEROTATE**</span><span class="sxs-lookup"><span data-stu-id="5ff2b-141">**EM\_GETPAGEROTATE**</span></span>](em-getpagerotate.md)
</dt> </dl>

 

 





