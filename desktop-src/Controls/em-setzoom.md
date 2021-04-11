---
title: 'EM_SETZOOM 訊息 (Richedit .h) '
description: 設定縮放比例。 比率必須是介於1/64 到64之間的值。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843803"
---
# <a name="em_setzoom-message"></a><span data-ttu-id="c51dd-106">EM \_ SETZOOM 訊息</span><span class="sxs-lookup"><span data-stu-id="c51dd-106">EM\_SETZOOM message</span></span>

<span data-ttu-id="c51dd-107">設定多行編輯控制項或 rich edit 控制項的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="c51dd-107">Sets the zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="c51dd-108">比率必須是介於1/64 到64之間的值。</span><span class="sxs-lookup"><span data-stu-id="c51dd-108">The ratio must be a value between 1/64 and 64.</span></span> <span data-ttu-id="c51dd-109">編輯控制項必須設定 **ES \_ EX \_ 可** 擴充樣式，此訊息才能有效果，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="c51dd-109">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="c51dd-110">參數</span><span class="sxs-lookup"><span data-stu-id="c51dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c51dd-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c51dd-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c51dd-112">縮放比例的分子。</span><span class="sxs-lookup"><span data-stu-id="c51dd-112">Numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="c51dd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c51dd-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c51dd-114">縮放比例的分母。</span><span class="sxs-lookup"><span data-stu-id="c51dd-114">Denominator of the zoom ratio.</span></span> <span data-ttu-id="c51dd-115">這些參數可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="c51dd-115">These parameters can have the following values.</span></span>



| <span data-ttu-id="c51dd-116">值</span><span class="sxs-lookup"><span data-stu-id="c51dd-116">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="c51dd-117">意義</span><span class="sxs-lookup"><span data-stu-id="c51dd-117">Meaning</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <span data-ttu-id="c51dd-118"><dt>**兩者都是0**</dt></span><span class="sxs-lookup"><span data-stu-id="c51dd-118"><dt>**Both 0**</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="c51dd-119">使用 **EM \_ SETZOOM** 訊息關閉縮放， (縮放可能仍會使用 [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)) 進行。</span><span class="sxs-lookup"><span data-stu-id="c51dd-119">Turns off zooming by using the **EM\_SETZOOM** message (zooming may still occur using [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span></span><br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <span data-ttu-id="c51dd-120"><dt>**1/64 < (wParam/lParam) < 64**</dt></span><span class="sxs-lookup"><span data-stu-id="c51dd-120"><dt>**1/64 < (wParam / lParam) < 64**</dt></span></span> </dl> | <span data-ttu-id="c51dd-121">依縮放比例分子/分母縮放顯示比例</span><span class="sxs-lookup"><span data-stu-id="c51dd-121">Zooms display by the zoom ratio numerator/denominator</span></span><br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c51dd-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c51dd-122">Return value</span></span>

<span data-ttu-id="c51dd-123">如果接受新的縮放設定，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c51dd-123">If the new zoom setting is accepted, the return value is **TRUE**.</span></span>

<span data-ttu-id="c51dd-124">如果未接受新的縮放設定，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c51dd-124">If the new zoom setting is not accepted, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c51dd-125">備註</span><span class="sxs-lookup"><span data-stu-id="c51dd-125">Remarks</span></span>

<span data-ttu-id="c51dd-126">**編輯：** 在 Windows 10 1809 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="c51dd-126">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="c51dd-127">編輯控制項必須設定 **ES \_ EX \_ 可** 擴充樣式，此訊息才能有效果，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="c51dd-127">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="c51dd-128">如需編輯控制項的詳細資訊，請參閱 [編輯控制項](about-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="c51dd-128">For information about the edit control, see [Edit Controls](about-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c51dd-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c51dd-129">Requirements</span></span>



| <span data-ttu-id="c51dd-130">需求</span><span class="sxs-lookup"><span data-stu-id="c51dd-130">Requirement</span></span> | <span data-ttu-id="c51dd-131">值</span><span class="sxs-lookup"><span data-stu-id="c51dd-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c51dd-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c51dd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c51dd-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c51dd-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c51dd-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c51dd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c51dd-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c51dd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c51dd-136">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c51dd-136">Redistributable</span></span><br/>          | <span data-ttu-id="c51dd-137">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="c51dd-137">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="c51dd-138">標頭</span><span class="sxs-lookup"><span data-stu-id="c51dd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c51dd-139"><dt>Richedit .h/Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c51dd-139"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c51dd-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c51dd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51dd-141">**EM \_ GETZOOM**</span><span class="sxs-lookup"><span data-stu-id="c51dd-141">**EM\_GETZOOM**</span></span>](em-getzoom.md)
</dt> </dl>

 

 





