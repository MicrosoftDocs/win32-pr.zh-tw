---
title: 'EM_GETSTORYTYPE 訊息 (Richedit .h) '
description: 取得案例類型。
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- EM_GETSTORYTYPE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843484"
---
# <a name="em_getstorytype-message"></a><span data-ttu-id="195b0-104">EM \_ GETSTORYTYPE 訊息</span><span class="sxs-lookup"><span data-stu-id="195b0-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="195b0-105">取得案例類型。</span><span class="sxs-lookup"><span data-stu-id="195b0-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="195b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="195b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="195b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="195b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="195b0-108">故事索引。</span><span class="sxs-lookup"><span data-stu-id="195b0-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="195b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="195b0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="195b0-110">保護必須是0。</span><span class="sxs-lookup"><span data-stu-id="195b0-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="195b0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="195b0-111">Return value</span></span>

<span data-ttu-id="195b0-112">傳回案例類型（可以是用戶端定義的自訂值），或下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="195b0-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="195b0-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="195b0-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="195b0-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="195b0-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="195b0-128">Requirements</span></span>



| <span data-ttu-id="195b0-129">需求</span><span class="sxs-lookup"><span data-stu-id="195b0-129">Requirement</span></span> | <span data-ttu-id="195b0-130">值</span><span class="sxs-lookup"><span data-stu-id="195b0-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="195b0-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="195b0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="195b0-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="195b0-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="195b0-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="195b0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="195b0-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="195b0-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="195b0-135">標頭</span><span class="sxs-lookup"><span data-stu-id="195b0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="195b0-136"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="195b0-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="195b0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="195b0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="195b0-138">**EM \_ SETSTORYTYPE**</span><span class="sxs-lookup"><span data-stu-id="195b0-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="195b0-139">**ITextStoryRanges：： Item**</span><span class="sxs-lookup"><span data-stu-id="195b0-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





