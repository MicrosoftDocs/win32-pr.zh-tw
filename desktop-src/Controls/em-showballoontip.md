---
title: 'EM_SHOWBALLOONTIP 訊息 (Commctrl .h) '
description: EM \_ SHOWBALLOONTIP 訊息會顯示與編輯控制項相關聯的氣球提示。
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- EM_SHOWBALLOONTIP message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104207"
---
# <a name="em_showballoontip-message"></a><span data-ttu-id="579d1-104">EM \_ SHOWBALLOONTIP 訊息</span><span class="sxs-lookup"><span data-stu-id="579d1-104">EM\_SHOWBALLOONTIP message</span></span>

<span data-ttu-id="579d1-105">**EM \_ SHOWBALLOONTIP** 訊息會顯示與編輯控制項相關聯的氣球提示。</span><span class="sxs-lookup"><span data-stu-id="579d1-105">The **EM\_SHOWBALLOONTIP** message displays a balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="579d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="579d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="579d1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="579d1-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="579d1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="579d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="579d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="579d1-110">[**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)結構的指標，其中包含要顯示之氣球提示的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="579d1-110">A pointer to an [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) structure that contains information about the balloon tip to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579d1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="579d1-111">Return value</span></span>

<span data-ttu-id="579d1-112">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="579d1-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="579d1-113">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="579d1-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="579d1-114">備註</span><span class="sxs-lookup"><span data-stu-id="579d1-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="579d1-115">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="579d1-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="579d1-116">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="579d1-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="579d1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="579d1-117">Requirements</span></span>



| <span data-ttu-id="579d1-118">需求</span><span class="sxs-lookup"><span data-stu-id="579d1-118">Requirement</span></span> | <span data-ttu-id="579d1-119">值</span><span class="sxs-lookup"><span data-stu-id="579d1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="579d1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="579d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="579d1-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="579d1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="579d1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="579d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="579d1-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="579d1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="579d1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="579d1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="579d1-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="579d1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="579d1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="579d1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="579d1-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="579d1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="579d1-128">**EDITBALLOONTIP**</span><span class="sxs-lookup"><span data-stu-id="579d1-128">**EDITBALLOONTIP**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[<span data-ttu-id="579d1-129">**編輯 \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="579d1-129">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





