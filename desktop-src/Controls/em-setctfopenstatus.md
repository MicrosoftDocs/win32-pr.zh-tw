---
title: 'EM_SETCTFOPENSTATUS 訊息 (Richedit .h) '
description: 開啟或關閉文字服務架構 (TSF) 鍵盤。
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025387"
---
# <a name="em_setctfopenstatus-message"></a><span data-ttu-id="6b153-104">EM \_ SETCTFOPENSTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="6b153-104">EM\_SETCTFOPENSTATUS message</span></span>

<span data-ttu-id="6b153-105">開啟或關閉文字服務架構 (TSF) 鍵盤。</span><span class="sxs-lookup"><span data-stu-id="6b153-105">Opens or closes the Text Services Framework (TSF) keyboard.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b153-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b153-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b153-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b153-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b153-108">若要開啟 TSF 鍵盤，請使用 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6b153-108">To turn on the TSF keyboard, use **TRUE**.</span></span> <span data-ttu-id="6b153-109">若要關閉 TSF 鍵盤，請使用 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6b153-109">To turn off the TSF keyboard, use **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b153-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b153-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b153-111">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="6b153-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b153-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b153-112">Return value</span></span>

<span data-ttu-id="6b153-113">如果成功，此訊息會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6b153-113">If successful, this message returns **TRUE**.</span></span> <span data-ttu-id="6b153-114">如果不成功，則此訊息會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6b153-114">If unsuccessful, this message returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b153-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b153-115">Requirements</span></span>



| <span data-ttu-id="6b153-116">需求</span><span class="sxs-lookup"><span data-stu-id="6b153-116">Requirement</span></span> | <span data-ttu-id="6b153-117">值</span><span class="sxs-lookup"><span data-stu-id="6b153-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b153-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b153-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b153-119">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b153-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b153-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b153-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b153-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b153-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b153-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6b153-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b153-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b153-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b153-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b153-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b153-125">**EM \_ GETCTFOPENSTATUS**</span><span class="sxs-lookup"><span data-stu-id="6b153-125">**EM\_GETCTFOPENSTATUS**</span></span>](em-getctfopenstatus.md)
</dt> </dl>

 

 





