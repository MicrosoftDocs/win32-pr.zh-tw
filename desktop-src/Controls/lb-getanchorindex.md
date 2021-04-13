---
title: 'LB_GETANCHORINDEX 訊息 (Winuser .h) '
description: 取得錨定專案 \ 郵件的索引，也就是從中開始多重選取的專案。 多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getanchorindex.htm
keywords:
- LB_GETANCHORINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5502a234424b818bb46e9c4326839b5aff2f83d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509303"
---
# <a name="lb_getanchorindex-message"></a><span data-ttu-id="6bd95-105">LB \_ GETANCHORINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="6bd95-105">LB\_GETANCHORINDEX message</span></span>

<span data-ttu-id="6bd95-106">取得錨定專案的索引，也就是多個選取範圍開始的專案。</span><span class="sxs-lookup"><span data-stu-id="6bd95-106">Gets the index of the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="6bd95-107">多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。</span><span class="sxs-lookup"><span data-stu-id="6bd95-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bd95-108">參數</span><span class="sxs-lookup"><span data-stu-id="6bd95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bd95-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bd95-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bd95-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="6bd95-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6bd95-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bd95-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bd95-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="6bd95-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bd95-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bd95-113">Return value</span></span>

<span data-ttu-id="6bd95-114">傳回值是錨點專案的索引。</span><span class="sxs-lookup"><span data-stu-id="6bd95-114">The return value is the index of the anchor item.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd95-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bd95-115">Requirements</span></span>



| <span data-ttu-id="6bd95-116">需求</span><span class="sxs-lookup"><span data-stu-id="6bd95-116">Requirement</span></span> | <span data-ttu-id="6bd95-117">值</span><span class="sxs-lookup"><span data-stu-id="6bd95-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd95-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bd95-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6bd95-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bd95-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6bd95-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bd95-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6bd95-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bd95-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6bd95-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6bd95-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bd95-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6bd95-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bd95-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bd95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd95-125">**LB \_ SETANCHORINDEX**</span><span class="sxs-lookup"><span data-stu-id="6bd95-125">**LB\_SETANCHORINDEX**</span></span>](lb-setanchorindex.md)
</dt> </dl>

 

 





