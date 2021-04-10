---
title: 'IPM_SETRANGE 訊息 (Commctrl .h) '
description: 在 IP 位址控制項中，設定指定之欄位的有效範圍。
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025344"
---
# <a name="ipm_setrange-message"></a><span data-ttu-id="3d517-104">IPM \_ SETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="3d517-104">IPM\_SETRANGE message</span></span>

<span data-ttu-id="3d517-105">在 IP 位址控制項中，設定指定之欄位的有效範圍。</span><span class="sxs-lookup"><span data-stu-id="3d517-105">Sets the valid range for the specified field in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d517-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d517-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d517-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d517-108">以零為基底的欄位索引，將套用此範圍。</span><span class="sxs-lookup"><span data-stu-id="3d517-108">A zero-based field index to which the range will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="3d517-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d517-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d517-110">**文字** 值，包含低序位位元組中範圍的下限，以及高序位位元組的上限。</span><span class="sxs-lookup"><span data-stu-id="3d517-110">A **WORD** value that contains the lower limit of the range in the low-order byte and the upper limit in the high-order byte.</span></span> <span data-ttu-id="3d517-111">這兩個值都包含在內。</span><span class="sxs-lookup"><span data-stu-id="3d517-111">Both of these values are inclusive.</span></span> <span data-ttu-id="3d517-112">[**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)宏也可以用來建立範圍。</span><span class="sxs-lookup"><span data-stu-id="3d517-112">The [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) macro can also be used to create the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d517-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d517-113">Return value</span></span>

<span data-ttu-id="3d517-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="3d517-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d517-115">備註</span><span class="sxs-lookup"><span data-stu-id="3d517-115">Remarks</span></span>

<span data-ttu-id="3d517-116">如果使用者在此範圍外的欄位中輸入值，控制項將會傳送具有所輸入值的 [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="3d517-116">If the user enters a value in the field that is outside of this range, the control will send the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification with the entered value.</span></span> <span data-ttu-id="3d517-117">如果值在傳送通知之後仍超出範圍，控制項將嘗試將輸入的值變更為最接近的範圍限制。</span><span class="sxs-lookup"><span data-stu-id="3d517-117">If the value is still outside of the range after sending the notification, the control will attempt to change the entered value to the closest range limit.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d517-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d517-118">Requirements</span></span>



| <span data-ttu-id="3d517-119">需求</span><span class="sxs-lookup"><span data-stu-id="3d517-119">Requirement</span></span> | <span data-ttu-id="3d517-120">值</span><span class="sxs-lookup"><span data-stu-id="3d517-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d517-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d517-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d517-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d517-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d517-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d517-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d517-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d517-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d517-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3d517-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d517-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d517-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





