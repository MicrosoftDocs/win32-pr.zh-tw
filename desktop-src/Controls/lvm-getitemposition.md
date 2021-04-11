---
title: 'LVM_GETITEMPOSITION 訊息 (Commctrl .h) '
description: 抓取清單視圖專案的位置。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemPosition 宏來傳送。
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844100"
---
# <a name="lvm_getitemposition-message"></a><span data-ttu-id="5be1b-105">LVM \_ GETITEMPOSITION 訊息</span><span class="sxs-lookup"><span data-stu-id="5be1b-105">LVM\_GETITEMPOSITION message</span></span>

<span data-ttu-id="5be1b-106">抓取清單視圖專案的位置。</span><span class="sxs-lookup"><span data-stu-id="5be1b-106">Retrieves the position of a list-view item.</span></span> <span data-ttu-id="5be1b-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="5be1b-107">You can send this message explicitly or by using the [**ListView\_GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5be1b-108">參數</span><span class="sxs-lookup"><span data-stu-id="5be1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be1b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5be1b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5be1b-110">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="5be1b-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="5be1b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5be1b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5be1b-112">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，該結構會接收專案左上角的位置（在視圖座標中）。</span><span class="sxs-lookup"><span data-stu-id="5be1b-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5be1b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5be1b-113">Return value</span></span>

<span data-ttu-id="5be1b-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5be1b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5be1b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5be1b-115">Requirements</span></span>



| <span data-ttu-id="5be1b-116">需求</span><span class="sxs-lookup"><span data-stu-id="5be1b-116">Requirement</span></span> | <span data-ttu-id="5be1b-117">值</span><span class="sxs-lookup"><span data-stu-id="5be1b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5be1b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5be1b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5be1b-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5be1b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5be1b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5be1b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5be1b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5be1b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5be1b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5be1b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5be1b-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5be1b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

