---
title: 'LB_SELITEMRANGE 訊息 (Winuser .h) '
description: 選取或取消選取多重選取清單方塊中的一或多個連續專案。
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025384"
---
# <a name="lb_selitemrange-message"></a><span data-ttu-id="81b10-104">LB \_ SELITEMRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="81b10-104">LB\_SELITEMRANGE message</span></span>

<span data-ttu-id="81b10-105">選取或取消選取多重選取清單方塊中的一或多個連續專案。</span><span class="sxs-lookup"><span data-stu-id="81b10-105">Selects or deselects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="81b10-106">參數</span><span class="sxs-lookup"><span data-stu-id="81b10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81b10-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81b10-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81b10-108">**TRUE** 表示選取專案的範圍，或選取 [ **FALSE** ] 以取消選取專案。</span><span class="sxs-lookup"><span data-stu-id="81b10-108">**TRUE** to select the range of items, or **FALSE** to deselect it.</span></span>

</dd> <dt>

<span data-ttu-id="81b10-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81b10-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81b10-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定要選取的第一個專案之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="81b10-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the first item to select.</span></span> <span data-ttu-id="81b10-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定要選取之最後一個專案的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="81b10-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81b10-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="81b10-112">Return value</span></span>

<span data-ttu-id="81b10-113">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="81b10-113">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="81b10-114">備註</span><span class="sxs-lookup"><span data-stu-id="81b10-114">Remarks</span></span>

<span data-ttu-id="81b10-115">此訊息只能搭配多重選取清單方塊使用。</span><span class="sxs-lookup"><span data-stu-id="81b10-115">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="81b10-116">此訊息只能選取前65536個專案內的範圍。</span><span class="sxs-lookup"><span data-stu-id="81b10-116">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b10-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="81b10-117">Requirements</span></span>



| <span data-ttu-id="81b10-118">需求</span><span class="sxs-lookup"><span data-stu-id="81b10-118">Requirement</span></span> | <span data-ttu-id="81b10-119">值</span><span class="sxs-lookup"><span data-stu-id="81b10-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b10-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81b10-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81b10-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81b10-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81b10-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81b10-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81b10-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81b10-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81b10-124">標頭</span><span class="sxs-lookup"><span data-stu-id="81b10-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="81b10-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="81b10-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81b10-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81b10-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="81b10-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="81b10-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81b10-128">**LB \_ SELITEMRANGEEX**</span><span class="sxs-lookup"><span data-stu-id="81b10-128">**LB\_SELITEMRANGEEX**</span></span>](lb-selitemrangeex.md)
</dt> <dt>

[<span data-ttu-id="81b10-129">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="81b10-129">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> <dt>

<span data-ttu-id="81b10-130">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="81b10-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="81b10-131">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="81b10-131">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

