---
title: 'EM_HIDEBALLOONTIP 訊息 (Commctrl .h) '
description: 隱藏任何與編輯控制項相關聯的氣球提示。
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- EM_HIDEBALLOONTIP message Windows 控制項
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933989"
---
# <a name="em_hideballoontip-message"></a><span data-ttu-id="46a75-104">EM \_ HIDEBALLOONTIP 訊息</span><span class="sxs-lookup"><span data-stu-id="46a75-104">EM\_HIDEBALLOONTIP message</span></span>

<span data-ttu-id="46a75-105">隱藏任何與編輯控制項相關聯的氣球提示。</span><span class="sxs-lookup"><span data-stu-id="46a75-105">Hides any balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="46a75-106">參數</span><span class="sxs-lookup"><span data-stu-id="46a75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46a75-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46a75-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46a75-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="46a75-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="46a75-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46a75-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46a75-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="46a75-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46a75-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="46a75-111">Return value</span></span>

<span data-ttu-id="46a75-112">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="46a75-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="46a75-113">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="46a75-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="46a75-114">備註</span><span class="sxs-lookup"><span data-stu-id="46a75-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46a75-115">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="46a75-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="46a75-116">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="46a75-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46a75-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="46a75-117">Requirements</span></span>



| <span data-ttu-id="46a75-118">需求</span><span class="sxs-lookup"><span data-stu-id="46a75-118">Requirement</span></span> | <span data-ttu-id="46a75-119">值</span><span class="sxs-lookup"><span data-stu-id="46a75-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46a75-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46a75-120">Minimum supported client</span></span><br/> | <span data-ttu-id="46a75-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46a75-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46a75-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46a75-122">Minimum supported server</span></span><br/> | <span data-ttu-id="46a75-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46a75-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46a75-124">標頭</span><span class="sxs-lookup"><span data-stu-id="46a75-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="46a75-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="46a75-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46a75-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46a75-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a75-127">**編輯 \_ HideBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="46a75-127">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





