---
title: 'LB_GETSEL 訊息 (Winuser .h) '
description: 取得專案的選取狀態。
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- LB_GETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843796"
---
# <a name="lb_getsel-message"></a><span data-ttu-id="cd081-104">LB \_ GETSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="cd081-104">LB\_GETSEL message</span></span>

<span data-ttu-id="cd081-105">取得專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="cd081-105">Gets the selection state of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd081-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd081-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd081-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd081-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd081-108">項目之以零起始的索引。</span><span class="sxs-lookup"><span data-stu-id="cd081-108">The zero-based index of the item.</span></span>

<span data-ttu-id="cd081-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="cd081-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="cd081-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="cd081-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="cd081-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cd081-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="cd081-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd081-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd081-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="cd081-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd081-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd081-114">Return value</span></span>

<span data-ttu-id="cd081-115">如果選取專案，則傳回值大於零;否則，它是零。</span><span class="sxs-lookup"><span data-stu-id="cd081-115">If an item is selected, the return value is greater than zero; otherwise, it is zero.</span></span> <span data-ttu-id="cd081-116">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="cd081-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd081-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd081-117">Requirements</span></span>



| <span data-ttu-id="cd081-118">需求</span><span class="sxs-lookup"><span data-stu-id="cd081-118">Requirement</span></span> | <span data-ttu-id="cd081-119">值</span><span class="sxs-lookup"><span data-stu-id="cd081-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd081-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd081-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd081-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd081-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd081-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd081-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd081-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd081-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd081-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cd081-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd081-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cd081-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd081-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd081-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd081-127">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="cd081-127">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





