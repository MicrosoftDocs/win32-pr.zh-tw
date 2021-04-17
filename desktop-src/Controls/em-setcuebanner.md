---
title: 'EM_SETCUEBANNER 訊息 (Commctrl .h) '
description: 設定 [編輯] 控制項所顯示的文字提示或提示，以提示使用者輸入資訊。
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466548"
---
# <a name="em_setcuebanner-message"></a><span data-ttu-id="cdda2-104">EM \_ SETCUEBANNER 訊息</span><span class="sxs-lookup"><span data-stu-id="cdda2-104">EM\_SETCUEBANNER message</span></span>

<span data-ttu-id="cdda2-105">設定 [編輯] 控制項所顯示的文字提示或提示，以提示使用者輸入資訊。</span><span class="sxs-lookup"><span data-stu-id="cdda2-105">Sets the textual cue, or tip, that is displayed by the edit control to prompt the user for information.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdda2-106">參數</span><span class="sxs-lookup"><span data-stu-id="cdda2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdda2-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdda2-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdda2-108">如果在編輯控制項有焦點時，提示橫幅應該會顯示，則 **為 TRUE** 。否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cdda2-108">**TRUE** if the cue banner should show even when the edit control has focus; otherwise, **FALSE**.</span></span> <span data-ttu-id="cdda2-109">**FALSE** 是當使用者按一下控制項時，提示橫幅消失的預設行為。</span><span class="sxs-lookup"><span data-stu-id="cdda2-109">**FALSE** is the default behavior the cue banner disappears when the user clicks in the control.</span></span>

</dd> <dt>

<span data-ttu-id="cdda2-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdda2-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdda2-111">Unicode 字串的指標，其中包含要顯示為文字提示的文字。</span><span class="sxs-lookup"><span data-stu-id="cdda2-111">A pointer to a Unicode string that contains the text to display as the textual cue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdda2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdda2-112">Return value</span></span>

<span data-ttu-id="cdda2-113">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="cdda2-113">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="cdda2-114">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cdda2-114">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdda2-115">備註</span><span class="sxs-lookup"><span data-stu-id="cdda2-115">Remarks</span></span>

<span data-ttu-id="cdda2-116">用來開始搜尋的編輯控制項可能會以灰色文字顯示為文字提示的「輸入搜尋」。</span><span class="sxs-lookup"><span data-stu-id="cdda2-116">An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue.</span></span> <span data-ttu-id="cdda2-117">當使用者按一下文字時，文字會消失，使用者可以輸入。</span><span class="sxs-lookup"><span data-stu-id="cdda2-117">When the user clicks the text, the text goes away and the user can type.</span></span>

<span data-ttu-id="cdda2-118">您無法在多行編輯控制項或 rich edit 控制項上設定提示橫幅。</span><span class="sxs-lookup"><span data-stu-id="cdda2-118">You cannot set a cue banner on a multiline edit control or on a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="cdda2-119">若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="cdda2-119">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cdda2-120">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="cdda2-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cdda2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdda2-121">Requirements</span></span>



| <span data-ttu-id="cdda2-122">需求</span><span class="sxs-lookup"><span data-stu-id="cdda2-122">Requirement</span></span> | <span data-ttu-id="cdda2-123">值</span><span class="sxs-lookup"><span data-stu-id="cdda2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdda2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdda2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cdda2-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdda2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cdda2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdda2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cdda2-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdda2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cdda2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="cdda2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdda2-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cdda2-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdda2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdda2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdda2-131">**編輯 \_ SetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="cdda2-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





