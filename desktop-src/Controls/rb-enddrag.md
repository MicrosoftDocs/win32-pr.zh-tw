---
title: 'RB_ENDDRAG 訊息 (Commctrl .h) '
description: 終止 Rebar 控制項的拖放作業。 此訊息不會造成 RBN \_ ENDDRAG 通知傳送。
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- RB_ENDDRAG message Windows 控制項
topic_type:
- apiref
api_name:
- RB_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6f201471b6f260555aacb9d89c1363492ed6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934709"
---
# <a name="rb_enddrag-message"></a><span data-ttu-id="3a0ef-105">RB \_ ENDDRAG 訊息</span><span class="sxs-lookup"><span data-stu-id="3a0ef-105">RB\_ENDDRAG message</span></span>

<span data-ttu-id="3a0ef-106">終止 Rebar 控制項的拖放作業。</span><span class="sxs-lookup"><span data-stu-id="3a0ef-106">Terminates the rebar control's drag-and-drop operation.</span></span> <span data-ttu-id="3a0ef-107">此訊息不會造成 [RBN \_ ENDDRAG](rbn-enddrag.md) 通知傳送。</span><span class="sxs-lookup"><span data-stu-id="3a0ef-107">This message does not cause an [RBN\_ENDDRAG](rbn-enddrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a0ef-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a0ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a0ef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a0ef-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3a0ef-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3a0ef-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3a0ef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a0ef-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3a0ef-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3a0ef-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a0ef-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a0ef-113">Return value</span></span>

<span data-ttu-id="3a0ef-114">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="3a0ef-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a0ef-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a0ef-115">Requirements</span></span>



| <span data-ttu-id="3a0ef-116">需求</span><span class="sxs-lookup"><span data-stu-id="3a0ef-116">Requirement</span></span> | <span data-ttu-id="3a0ef-117">值</span><span class="sxs-lookup"><span data-stu-id="3a0ef-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0ef-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a0ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a0ef-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a0ef-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a0ef-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a0ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a0ef-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a0ef-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a0ef-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3a0ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a0ef-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a0ef-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0ef-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a0ef-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a0ef-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="3a0ef-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a0ef-126">**RB \_ BEGINDRAG**</span><span class="sxs-lookup"><span data-stu-id="3a0ef-126">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
</dt> <dt>

[<span data-ttu-id="3a0ef-127">**RB \_ DRAGMOVE**</span><span class="sxs-lookup"><span data-stu-id="3a0ef-127">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
</dt> </dl>

 

 





