---
title: 'CB_GETTOPINDEX 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ GETTOPINDEX 訊息，以抓取下拉式方塊的清單方塊部分中第一個可見專案的以零為起始的索引。
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934360"
---
# <a name="cb_gettopindex-message"></a><span data-ttu-id="af680-104">CB \_ GETTOPINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="af680-104">CB\_GETTOPINDEX message</span></span>

<span data-ttu-id="af680-105">應用程式會傳送 **CB \_ GETTOPINDEX** 訊息，以抓取下拉式方塊的清單方塊部分中第一個可見專案的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="af680-105">An application sends the **CB\_GETTOPINDEX** message to retrieve the zero-based index of the first visible item in the list box portion of a combo box.</span></span> <span data-ttu-id="af680-106">一開始，索引0的專案會在清單方塊的頂端，但是如果清單方塊內容已經過滾動，則其他專案可能會位於頂端。</span><span class="sxs-lookup"><span data-stu-id="af680-106">Initially, the item with index 0 is at the top of the list box, but if the list box contents have been scrolled, another item may be at the top.</span></span>

## <a name="parameters"></a><span data-ttu-id="af680-107">參數</span><span class="sxs-lookup"><span data-stu-id="af680-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af680-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af680-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af680-109">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="af680-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="af680-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af680-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af680-111">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="af680-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af680-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="af680-112">Return value</span></span>

<span data-ttu-id="af680-113">如果訊息成功，則傳回值是下拉式方塊清單方塊中第一個可見專案的索引。</span><span class="sxs-lookup"><span data-stu-id="af680-113">If the message is successful, the return value is the index of the first visible item in the list box of the combo box.</span></span>

<span data-ttu-id="af680-114">如果訊息失敗，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="af680-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="af680-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="af680-115">Requirements</span></span>



| <span data-ttu-id="af680-116">需求</span><span class="sxs-lookup"><span data-stu-id="af680-116">Requirement</span></span> | <span data-ttu-id="af680-117">值</span><span class="sxs-lookup"><span data-stu-id="af680-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af680-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af680-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af680-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af680-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="af680-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af680-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af680-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af680-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="af680-122">標頭</span><span class="sxs-lookup"><span data-stu-id="af680-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af680-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="af680-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af680-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af680-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af680-125">**CB \_ SETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="af680-125">**CB\_SETTOPINDEX**</span></span>](cb-settopindex.md)
</dt> </dl>

 

 





