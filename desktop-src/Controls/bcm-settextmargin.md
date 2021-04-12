---
title: 'BCM_SETTEXTMARGIN 訊息 (Commctrl .h) '
description: BCM \_ SETTEXTMARGIN 訊息會設定在按鈕控制項中繪製文字的邊界。
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- BCM_SETTEXTMARGIN message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465269"
---
# <a name="bcm_settextmargin-message"></a><span data-ttu-id="ccca4-104">BCM \_ SETTEXTMARGIN 訊息</span><span class="sxs-lookup"><span data-stu-id="ccca4-104">BCM\_SETTEXTMARGIN message</span></span>

<span data-ttu-id="ccca4-105">**BCM \_ SETTEXTMARGIN** 訊息會設定在按鈕控制項中繪製文字的邊界。</span><span class="sxs-lookup"><span data-stu-id="ccca4-105">The **BCM\_SETTEXTMARGIN** message sets the margins for drawing text in a button control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccca4-106">參數</span><span class="sxs-lookup"><span data-stu-id="ccca4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccca4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccca4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccca4-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="ccca4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ccca4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccca4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccca4-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，指定用來繪製文字的邊界。</span><span class="sxs-lookup"><span data-stu-id="ccca4-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccca4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccca4-111">Return value</span></span>

<span data-ttu-id="ccca4-112">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ccca4-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="ccca4-113">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ccca4-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccca4-114">備註</span><span class="sxs-lookup"><span data-stu-id="ccca4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ccca4-115">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="ccca4-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ccca4-116">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ccca4-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccca4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccca4-117">Requirements</span></span>



| <span data-ttu-id="ccca4-118">需求</span><span class="sxs-lookup"><span data-stu-id="ccca4-118">Requirement</span></span> | <span data-ttu-id="ccca4-119">值</span><span class="sxs-lookup"><span data-stu-id="ccca4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccca4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccca4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ccca4-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccca4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ccca4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccca4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ccca4-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccca4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccca4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ccca4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccca4-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccca4-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccca4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccca4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccca4-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="ccca4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ccca4-128">**按鈕 \_ SetTextMargin**</span><span class="sxs-lookup"><span data-stu-id="ccca4-128">**Button\_SetTextMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

<span data-ttu-id="ccca4-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="ccca4-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ccca4-130">按鈕</span><span class="sxs-lookup"><span data-stu-id="ccca4-130">Buttons</span></span>](buttons.md)
</dt> </dl>

 

