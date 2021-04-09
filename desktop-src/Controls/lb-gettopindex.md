---
title: 'LB_GETTOPINDEX 訊息 (Winuser .h) '
description: 取得清單方塊中第一個可見專案的索引。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- LB_GETTOPINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934413"
---
# <a name="lb_gettopindex-message"></a><span data-ttu-id="ebdc6-104">LB \_ GETTOPINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="ebdc6-104">LB\_GETTOPINDEX message</span></span>

<span data-ttu-id="ebdc6-105">取得清單方塊中第一個可見專案的索引。</span><span class="sxs-lookup"><span data-stu-id="ebdc6-105">Gets the index of the first visible item in a list box.</span></span> <span data-ttu-id="ebdc6-106">一開始，索引0的專案會出現在清單方塊的頂端，但如果清單方塊內容已滾動至另一個專案，則會位於最上方。</span><span class="sxs-lookup"><span data-stu-id="ebdc6-106">Initially the item with index 0 is at the top of the list box, but if the list box contents have been scrolled another item may be at the top.</span></span> <span data-ttu-id="ebdc6-107">多重資料行清單方塊中第一個可見的專案是左上方的專案。</span><span class="sxs-lookup"><span data-stu-id="ebdc6-107">The first visible item in a multiple-column list box is the top-left item.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebdc6-108">參數</span><span class="sxs-lookup"><span data-stu-id="ebdc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebdc6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebdc6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebdc6-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="ebdc6-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ebdc6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebdc6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebdc6-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="ebdc6-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebdc6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebdc6-113">Return value</span></span>

<span data-ttu-id="ebdc6-114">傳回值是清單方塊中第一個可見專案的索引。</span><span class="sxs-lookup"><span data-stu-id="ebdc6-114">The return value is the index of the first visible item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebdc6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebdc6-115">Requirements</span></span>



| <span data-ttu-id="ebdc6-116">需求</span><span class="sxs-lookup"><span data-stu-id="ebdc6-116">Requirement</span></span> | <span data-ttu-id="ebdc6-117">值</span><span class="sxs-lookup"><span data-stu-id="ebdc6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebdc6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebdc6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ebdc6-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebdc6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ebdc6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebdc6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ebdc6-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebdc6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebdc6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ebdc6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebdc6-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ebdc6-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebdc6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebdc6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebdc6-125">**LB \_ SETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="ebdc6-125">**LB\_SETTOPINDEX**</span></span>](lb-settopindex.md)
</dt> </dl>

 

 





