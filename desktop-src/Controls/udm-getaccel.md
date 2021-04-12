---
title: 'UDM_GETACCEL 訊息 (Commctrl .h) '
description: 抓取上下按鈕控制項的加速資訊。
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464653"
---
# <a name="udm_getaccel-message"></a><span data-ttu-id="73e1e-104">UDM \_ GETACCEL 訊息</span><span class="sxs-lookup"><span data-stu-id="73e1e-104">UDM\_GETACCEL message</span></span>

<span data-ttu-id="73e1e-105">抓取上下按鈕控制項的加速資訊。</span><span class="sxs-lookup"><span data-stu-id="73e1e-105">Retrieves acceleration information for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="73e1e-106">參數</span><span class="sxs-lookup"><span data-stu-id="73e1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e1e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73e1e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73e1e-108">*LParam* 所指定陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="73e1e-108">Number of elements in the array specified by *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="73e1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73e1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73e1e-110">接收加速資訊之 [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="73e1e-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that receive acceleration information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e1e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="73e1e-111">Return value</span></span>

<span data-ttu-id="73e1e-112">傳回值是目前為控制項設定的快速鍵數目。</span><span class="sxs-lookup"><span data-stu-id="73e1e-112">The return value is the number of accelerators currently set for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e1e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="73e1e-113">Requirements</span></span>



| <span data-ttu-id="73e1e-114">需求</span><span class="sxs-lookup"><span data-stu-id="73e1e-114">Requirement</span></span> | <span data-ttu-id="73e1e-115">值</span><span class="sxs-lookup"><span data-stu-id="73e1e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73e1e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73e1e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="73e1e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73e1e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73e1e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73e1e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="73e1e-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73e1e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73e1e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="73e1e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="73e1e-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="73e1e-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e1e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73e1e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e1e-123">**UDM \_ SETACCEL**</span><span class="sxs-lookup"><span data-stu-id="73e1e-123">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)
</dt> </dl>

 

 





