---
title: 'LB_RESETCONTENT 訊息 (Winuser .h) '
description: 從清單方塊中移除所有專案。
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- LB_RESETCONTENT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844120"
---
# <a name="lb_resetcontent-message"></a><span data-ttu-id="82e1d-104">LB \_ RESETCONTENT 訊息</span><span class="sxs-lookup"><span data-stu-id="82e1d-104">LB\_RESETCONTENT message</span></span>

<span data-ttu-id="82e1d-105">從清單方塊中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="82e1d-105">Removes all items from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="82e1d-106">參數</span><span class="sxs-lookup"><span data-stu-id="82e1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82e1d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82e1d-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="82e1d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="82e1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82e1d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82e1d-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="82e1d-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e1d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="82e1d-111">Return value</span></span>

<span data-ttu-id="82e1d-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="82e1d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82e1d-113">備註</span><span class="sxs-lookup"><span data-stu-id="82e1d-113">Remarks</span></span>

<span data-ttu-id="82e1d-114">如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，清單方塊的擁有者會收到清單方塊中每個專案的 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="82e1d-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the owner of the list box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="82e1d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="82e1d-115">Requirements</span></span>



| <span data-ttu-id="82e1d-116">需求</span><span class="sxs-lookup"><span data-stu-id="82e1d-116">Requirement</span></span> | <span data-ttu-id="82e1d-117">值</span><span class="sxs-lookup"><span data-stu-id="82e1d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e1d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82e1d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82e1d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82e1d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="82e1d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82e1d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82e1d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82e1d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="82e1d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="82e1d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="82e1d-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="82e1d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82e1d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82e1d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e1d-125">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="82e1d-125">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





