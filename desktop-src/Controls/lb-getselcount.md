---
title: 'LB_GETSELCOUNT 訊息 (Winuser .h) '
description: 取得多重選取清單方塊中選取的專案總數。
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- LB_GETSELCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094316"
---
# <a name="lb_getselcount-message"></a><span data-ttu-id="23163-104">LB \_ GETSELCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="23163-104">LB\_GETSELCOUNT message</span></span>

<span data-ttu-id="23163-105">取得多重選取清單方塊中選取的專案總數。</span><span class="sxs-lookup"><span data-stu-id="23163-105">Gets the total number of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="23163-106">參數</span><span class="sxs-lookup"><span data-stu-id="23163-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23163-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23163-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23163-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="23163-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="23163-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23163-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23163-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="23163-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23163-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="23163-111">Return value</span></span>

<span data-ttu-id="23163-112">傳回值是清單方塊中已選取專案的計數。</span><span class="sxs-lookup"><span data-stu-id="23163-112">The return value is the count of selected items in the list box.</span></span> <span data-ttu-id="23163-113">如果清單方塊是單一選取清單方塊，則傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="23163-113">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="23163-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="23163-114">Requirements</span></span>



| <span data-ttu-id="23163-115">需求</span><span class="sxs-lookup"><span data-stu-id="23163-115">Requirement</span></span> | <span data-ttu-id="23163-116">值</span><span class="sxs-lookup"><span data-stu-id="23163-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23163-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23163-117">Minimum supported client</span></span><br/> | <span data-ttu-id="23163-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23163-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="23163-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23163-119">Minimum supported server</span></span><br/> | <span data-ttu-id="23163-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23163-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="23163-121">標頭</span><span class="sxs-lookup"><span data-stu-id="23163-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="23163-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="23163-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23163-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23163-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23163-124">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="23163-124">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





