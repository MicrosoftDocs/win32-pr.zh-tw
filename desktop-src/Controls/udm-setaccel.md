---
title: 'UDM_SETACCEL 訊息 (Commctrl .h) '
description: 設定上下按鈕控制項的加速。
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025493"
---
# <a name="udm_setaccel-message"></a><span data-ttu-id="7be1d-104">UDM \_ SETACCEL 訊息</span><span class="sxs-lookup"><span data-stu-id="7be1d-104">UDM\_SETACCEL message</span></span>

<span data-ttu-id="7be1d-105">設定上下按鈕控制項的加速。</span><span class="sxs-lookup"><span data-stu-id="7be1d-105">Sets the acceleration for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7be1d-106">參數</span><span class="sxs-lookup"><span data-stu-id="7be1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7be1d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7be1d-108">*AAccels* 所指定的 [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)結構數目。</span><span class="sxs-lookup"><span data-stu-id="7be1d-108">Number of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures specified by *aAccels*.</span></span>

</dd> <dt>

<span data-ttu-id="7be1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7be1d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7be1d-110">[**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)結構陣列的指標，其中包含加速資訊。</span><span class="sxs-lookup"><span data-stu-id="7be1d-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that contain acceleration information.</span></span> <span data-ttu-id="7be1d-111">元素應以每個 **nSec** 成員的遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="7be1d-111">Elements should be sorted in ascending order based on the **nSec** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be1d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7be1d-112">Return value</span></span>

<span data-ttu-id="7be1d-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7be1d-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be1d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7be1d-114">Requirements</span></span>



| <span data-ttu-id="7be1d-115">需求</span><span class="sxs-lookup"><span data-stu-id="7be1d-115">Requirement</span></span> | <span data-ttu-id="7be1d-116">值</span><span class="sxs-lookup"><span data-stu-id="7be1d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7be1d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7be1d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7be1d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7be1d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7be1d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7be1d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7be1d-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7be1d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7be1d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7be1d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be1d-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7be1d-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be1d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7be1d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be1d-124">**UDM \_ GETACCEL**</span><span class="sxs-lookup"><span data-stu-id="7be1d-124">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)
</dt> </dl>

 

 





