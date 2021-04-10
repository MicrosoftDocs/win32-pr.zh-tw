---
title: 'EM_GETZOOM 訊息 (Richedit .h) '
description: 取得目前的縮放比例。 Zoom 比例一律介於1/64 到64之間。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- EM_GETZOOM message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685606"
---
# <a name="em_getzoom-message"></a><span data-ttu-id="b0353-106">EM \_ GETZOOM 訊息</span><span class="sxs-lookup"><span data-stu-id="b0353-106">EM\_GETZOOM message</span></span>

<span data-ttu-id="b0353-107">取得多行編輯控制項或 rich edit 控制項的目前縮放比例。</span><span class="sxs-lookup"><span data-stu-id="b0353-107">Gets the current zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="b0353-108">Zoom 比例一律介於1/64 到64之間。</span><span class="sxs-lookup"><span data-stu-id="b0353-108">The zoom ration is always between 1/64 and 64.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0353-109">參數</span><span class="sxs-lookup"><span data-stu-id="b0353-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0353-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0353-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0353-111">接收縮放比例的分子。</span><span class="sxs-lookup"><span data-stu-id="b0353-111">Receives the numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="b0353-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0353-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0353-113">接收縮放比例的分母。</span><span class="sxs-lookup"><span data-stu-id="b0353-113">Receives the denominator of the zoom ratio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0353-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0353-114">Return value</span></span>

<span data-ttu-id="b0353-115">如果處理訊息，訊息會傳回 TRUE，如果 *wParam* 和 *lParam* 都不是 **Null**，就會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b0353-115">The message returns **TRUE** if message is processed, which it will be if both *wParam* and *lParam* are not **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0353-116">備註</span><span class="sxs-lookup"><span data-stu-id="b0353-116">Remarks</span></span>

<span data-ttu-id="b0353-117">**編輯：** 在 Windows 10 1809 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="b0353-117">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="b0353-118">編輯控制項必須設定 **ES \_ EX \_ 可** 擴充樣式，此訊息才能有效果，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="b0353-118">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="b0353-119">如需編輯控制項的詳細資訊，請參閱 [編輯控制項](edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="b0353-119">For information about the edit control, see [Edit Controls](edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0353-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0353-120">Requirements</span></span>



| <span data-ttu-id="b0353-121">需求</span><span class="sxs-lookup"><span data-stu-id="b0353-121">Requirement</span></span> | <span data-ttu-id="b0353-122">值</span><span class="sxs-lookup"><span data-stu-id="b0353-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0353-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0353-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b0353-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0353-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0353-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0353-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b0353-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0353-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0353-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b0353-127">Redistributable</span></span><br/>          | <span data-ttu-id="b0353-128">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="b0353-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="b0353-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b0353-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0353-130"><dt>Richedit .h/Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0353-130"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0353-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0353-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0353-132">**EM \_ SETZOOM**</span><span class="sxs-lookup"><span data-stu-id="b0353-132">**EM\_SETZOOM**</span></span>](em-setzoom.md)
</dt> </dl>

 

 





