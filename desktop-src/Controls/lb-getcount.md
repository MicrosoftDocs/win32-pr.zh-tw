---
title: 'LB_GETCOUNT 訊息 (Winuser .h) '
description: 取得清單方塊中的專案數。
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- LB_GETCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466805"
---
# <a name="lb_getcount-message"></a><span data-ttu-id="d1aa3-104">LB \_ GETCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="d1aa3-104">LB\_GETCOUNT message</span></span>

<span data-ttu-id="d1aa3-105">取得清單方塊中的專案數。</span><span class="sxs-lookup"><span data-stu-id="d1aa3-105">Gets the number of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1aa3-106">參數</span><span class="sxs-lookup"><span data-stu-id="d1aa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1aa3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1aa3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1aa3-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="d1aa3-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d1aa3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1aa3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1aa3-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="d1aa3-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1aa3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1aa3-111">Return value</span></span>

<span data-ttu-id="d1aa3-112">傳回值是清單方塊中的專案數，如果發生錯誤，則為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="d1aa3-112">The return value is the number of items in the list box, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1aa3-113">備註</span><span class="sxs-lookup"><span data-stu-id="d1aa3-113">Remarks</span></span>

<span data-ttu-id="d1aa3-114">傳回的計數大於最後一個專案的索引值， (索引是以零為基底的) 。</span><span class="sxs-lookup"><span data-stu-id="d1aa3-114">The returned count is one greater than the index value of the last item (the index is zero-based).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1aa3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1aa3-115">Requirements</span></span>



| <span data-ttu-id="d1aa3-116">需求</span><span class="sxs-lookup"><span data-stu-id="d1aa3-116">Requirement</span></span> | <span data-ttu-id="d1aa3-117">值</span><span class="sxs-lookup"><span data-stu-id="d1aa3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1aa3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1aa3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1aa3-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1aa3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1aa3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1aa3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d1aa3-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1aa3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1aa3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d1aa3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1aa3-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1aa3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1aa3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1aa3-125">**LB \_ SETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="d1aa3-125">**LB\_SETCOUNT**</span></span>](lb-setcount.md)
</dt> </dl>

 

 





