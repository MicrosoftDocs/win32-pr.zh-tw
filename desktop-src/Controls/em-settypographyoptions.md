---
title: 'EM_SETTYPOGRAPHYOPTIONS 訊息 (Richedit .h) '
description: 設定 rich edit 控制項之印刷樣式選項的目前狀態。
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934541"
---
# <a name="em_settypographyoptions-message"></a><span data-ttu-id="f776e-104">EM \_ SETTYPOGRAPHYOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="f776e-104">EM\_SETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="f776e-105">設定 rich edit 控制項之印刷樣式選項的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f776e-105">Sets the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f776e-106">參數</span><span class="sxs-lookup"><span data-stu-id="f776e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f776e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f776e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f776e-108">指定下列其中一個或兩個值。</span><span class="sxs-lookup"><span data-stu-id="f776e-108">Specifies one or both of the following values.</span></span>



| <span data-ttu-id="f776e-109">值</span><span class="sxs-lookup"><span data-stu-id="f776e-109">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="f776e-110">意義</span><span class="sxs-lookup"><span data-stu-id="f776e-110">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <span data-ttu-id="f776e-111"><dt>**至 \_ADVANCEDTYPOGRAPHY**</dt></span><span class="sxs-lookup"><span data-stu-id="f776e-111"><dt>**TO\_ADVANCEDTYPOGRAPHY** </dt></span></span> </dl> | <span data-ttu-id="f776e-112">已開啟先進的換行和行格式。</span><span class="sxs-lookup"><span data-stu-id="f776e-112">Advanced line breaking and line formatting is turned on.</span></span> <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <span data-ttu-id="f776e-113"><dt>**\_SIMPLELINEBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="f776e-113"><dt>**TO\_SIMPLELINEBREAK**</dt></span></span> </dl>             | <span data-ttu-id="f776e-114">更快速地細分簡單文字 (需要 **\_ ADVANCEDTYPOGRAPHY**) 。</span><span class="sxs-lookup"><span data-stu-id="f776e-114">Faster line breaking for simple text (requires **TO\_ADVANCEDTYPOGRAPHY**).</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="f776e-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f776e-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f776e-116">由 *wParam* 中的一或多個旗標所組成的遮罩。</span><span class="sxs-lookup"><span data-stu-id="f776e-116">A mask consisting of one or more of the flags in *wParam*.</span></span> <span data-ttu-id="f776e-117">只會設定或清除此遮罩中設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="f776e-117">Only the flags that are set in this mask will be set or cleared.</span></span> <span data-ttu-id="f776e-118">這可讓您設定或清除單一旗標，而不需要讀取目前的旗標狀態。</span><span class="sxs-lookup"><span data-stu-id="f776e-118">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f776e-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f776e-119">Return value</span></span>

<span data-ttu-id="f776e-120">如果 *wParam* 有效，**則傳回 TRUE** ，否則傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f776e-120">Returns **TRUE** if *wParam* is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f776e-121">備註</span><span class="sxs-lookup"><span data-stu-id="f776e-121">Remarks</span></span>

<span data-ttu-id="f776e-122">Rich edit 控制項會在需要時自動開啟 Advanced line 斷線，例如處理阿拉伯文和希伯來文等複雜字集，以及數學。</span><span class="sxs-lookup"><span data-stu-id="f776e-122">Advanced line breaking is turned on automatically by the rich edit control when needed, such as for handling complex scripts like Arabic and Hebrew, and for mathematics.</span></span> <span data-ttu-id="f776e-123">它也需要對齊段落、斷字和其他印刷樣式功能。</span><span class="sxs-lookup"><span data-stu-id="f776e-123">It s also needed for justified paragraphs, hyphenation, and other typographic features.</span></span>

## <a name="requirements"></a><span data-ttu-id="f776e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f776e-124">Requirements</span></span>



| <span data-ttu-id="f776e-125">需求</span><span class="sxs-lookup"><span data-stu-id="f776e-125">Requirement</span></span> | <span data-ttu-id="f776e-126">值</span><span class="sxs-lookup"><span data-stu-id="f776e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f776e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f776e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f776e-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f776e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f776e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f776e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f776e-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f776e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f776e-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f776e-131">Redistributable</span></span><br/>          | <span data-ttu-id="f776e-132">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="f776e-132">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="f776e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f776e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f776e-134"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f776e-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f776e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f776e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f776e-136">**EM \_ GETTYPOGRAPHYOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="f776e-136">**EM\_GETTYPOGRAPHYOPTIONS**</span></span>](em-gettypographyoptions.md)
</dt> </dl>

 

 





