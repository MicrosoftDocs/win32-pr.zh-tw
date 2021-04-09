---
title: 'LB_ITEMFROMPOINT 訊息 (Winuser .h) '
description: 取得最接近清單方塊中指定點之專案的以零為基底的索引。
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686288"
---
# <a name="lb_itemfrompoint-message"></a><span data-ttu-id="647c2-104">LB \_ ITEMFROMPOINT 訊息</span><span class="sxs-lookup"><span data-stu-id="647c2-104">LB\_ITEMFROMPOINT message</span></span>

<span data-ttu-id="647c2-105">取得最接近清單方塊中指定點之專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="647c2-105">Gets the zero-based index of the item nearest the specified point in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="647c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="647c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="647c2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="647c2-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="647c2-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="647c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="647c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="647c2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定某個點的 x 座標（相對於清單方塊的工作區左上角）。</span><span class="sxs-lookup"><span data-stu-id="647c2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

<span data-ttu-id="647c2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定點的 y 座標（相對於清單方塊的工作區左上角）。</span><span class="sxs-lookup"><span data-stu-id="647c2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647c2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="647c2-112">Return value</span></span>

<span data-ttu-id="647c2-113">傳回值包含 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))中最接近專案的索引。</span><span class="sxs-lookup"><span data-stu-id="647c2-113">The return value contains the index of the nearest item in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span> <span data-ttu-id="647c2-114">如果指定的點位於清單方塊的工作區中，則 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 為零，如果位於工作區之外，則為零。</span><span class="sxs-lookup"><span data-stu-id="647c2-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is zero if the specified point is in the client area of the list box, or one if it is outside the client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="647c2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="647c2-115">Requirements</span></span>



| <span data-ttu-id="647c2-116">需求</span><span class="sxs-lookup"><span data-stu-id="647c2-116">Requirement</span></span> | <span data-ttu-id="647c2-117">值</span><span class="sxs-lookup"><span data-stu-id="647c2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647c2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="647c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="647c2-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="647c2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="647c2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="647c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="647c2-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="647c2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="647c2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="647c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="647c2-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="647c2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="647c2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="647c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647c2-125">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="647c2-125">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

