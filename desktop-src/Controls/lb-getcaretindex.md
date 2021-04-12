---
title: 'LB_GETCARETINDEX 訊息 (Winuser .h) '
description: 抓取在多重選取清單方塊中具有焦點之專案的索引。 您可以或可能不會選取此專案。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025442"
---
# <a name="lb_getcaretindex-message"></a><span data-ttu-id="0e826-105">LB \_ GETCARETINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="0e826-105">LB\_GETCARETINDEX message</span></span>

<span data-ttu-id="0e826-106">抓取在多重選取清單方塊中具有焦點之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="0e826-106">Retrieves the index of the item that has the focus in a multiple-selection list box.</span></span> <span data-ttu-id="0e826-107">您可以或可能不會選取此專案。</span><span class="sxs-lookup"><span data-stu-id="0e826-107">The item may or may not be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e826-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e826-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e826-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e826-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e826-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="0e826-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0e826-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e826-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e826-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="0e826-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e826-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e826-113">Return value</span></span>

<span data-ttu-id="0e826-114">傳回值是聚焦清單方塊專案以零為起始的索引，如果沒有任何專案具有焦點，則為0。</span><span class="sxs-lookup"><span data-stu-id="0e826-114">The return value is the zero-based index of the focused list box item, or 0 if no item has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e826-115">備註</span><span class="sxs-lookup"><span data-stu-id="0e826-115">Remarks</span></span>

<span data-ttu-id="0e826-116">此訊息也可以用來取得目前在單一選取清單方塊中選取之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="0e826-116">This message can also be used to get the index of the item that is currently selected in a single-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e826-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e826-117">Requirements</span></span>



| <span data-ttu-id="0e826-118">需求</span><span class="sxs-lookup"><span data-stu-id="0e826-118">Requirement</span></span> | <span data-ttu-id="0e826-119">值</span><span class="sxs-lookup"><span data-stu-id="0e826-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e826-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e826-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e826-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e826-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0e826-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e826-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e826-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e826-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e826-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0e826-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e826-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0e826-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e826-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e826-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e826-127">**LB \_ SETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="0e826-127">**LB\_SETCARETINDEX**</span></span>](lb-setcaretindex.md)
</dt> </dl>

 

 





