---
title: 'HDM_SETORDERARRAY 訊息 (Commctrl .h) '
description: 設定標頭專案的由左到右順序。 您可以明確地傳送此訊息，或使用標頭 \_ SetOrderArray 宏。
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465480"
---
# <a name="hdm_setorderarray-message"></a><span data-ttu-id="3d66a-105">HDM \_ SETORDERARRAY 訊息</span><span class="sxs-lookup"><span data-stu-id="3d66a-105">HDM\_SETORDERARRAY message</span></span>

<span data-ttu-id="3d66a-106">設定標頭專案的由左到右順序。</span><span class="sxs-lookup"><span data-stu-id="3d66a-106">Sets the left-to-right order of header items.</span></span> <span data-ttu-id="3d66a-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) 宏。</span><span class="sxs-lookup"><span data-stu-id="3d66a-107">You can send this message explicitly or use the [**Header\_SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d66a-108">參數</span><span class="sxs-lookup"><span data-stu-id="3d66a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d66a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d66a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d66a-110">*LParam* 中的緩衝區大小（以元素為限）。</span><span class="sxs-lookup"><span data-stu-id="3d66a-110">The size of the buffer at *lParam*, in elements.</span></span> <span data-ttu-id="3d66a-111">此值必須等於 [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="3d66a-111">This value must equal the value returned by [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d66a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d66a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d66a-113">陣列的指標，這個陣列會指定專案的顯示順序（從左至右）。</span><span class="sxs-lookup"><span data-stu-id="3d66a-113">A pointer to an array that specifies the order in which items should be displayed, from left to right.</span></span> <span data-ttu-id="3d66a-114">例如，如果陣列的內容是 {2,0,1} ，控制項會從左至右顯示專案2、專案0和專案1。</span><span class="sxs-lookup"><span data-stu-id="3d66a-114">For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d66a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d66a-115">Return value</span></span>

<span data-ttu-id="3d66a-116">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="3d66a-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d66a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d66a-117">Requirements</span></span>



| <span data-ttu-id="3d66a-118">需求</span><span class="sxs-lookup"><span data-stu-id="3d66a-118">Requirement</span></span> | <span data-ttu-id="3d66a-119">值</span><span class="sxs-lookup"><span data-stu-id="3d66a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d66a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d66a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d66a-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d66a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d66a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d66a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d66a-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d66a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d66a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3d66a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d66a-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d66a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





