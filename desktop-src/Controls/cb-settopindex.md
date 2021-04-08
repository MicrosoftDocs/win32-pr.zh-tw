---
title: 'CB_SETTOPINDEX 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETTOPINDEX 訊息，確保下拉式方塊的清單方塊中會顯示特定的專案。
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685562"
---
# <a name="cb_settopindex-message"></a><span data-ttu-id="3a211-104">CB \_ SETTOPINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="3a211-104">CB\_SETTOPINDEX message</span></span>

<span data-ttu-id="3a211-105">應用程式會傳送 **CB \_ SETTOPINDEX** 訊息，確保下拉式方塊的清單方塊中會顯示特定的專案。</span><span class="sxs-lookup"><span data-stu-id="3a211-105">An application sends the **CB\_SETTOPINDEX** message to ensure that a particular item is visible in the list box of a combo box.</span></span> <span data-ttu-id="3a211-106">系統會將清單方塊內容滾動，讓指定的專案出現在清單方塊的頂端，或達到最大捲軸範圍。</span><span class="sxs-lookup"><span data-stu-id="3a211-106">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a211-107">參數</span><span class="sxs-lookup"><span data-stu-id="3a211-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a211-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a211-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a211-109">指定清單專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="3a211-109">Specifies the zero-based index of the list item.</span></span>

</dd> <dt>

<span data-ttu-id="3a211-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a211-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a211-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3a211-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a211-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a211-112">Return value</span></span>

<span data-ttu-id="3a211-113">如果訊息成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="3a211-113">If the message is successful, the return value is zero.</span></span>

<span data-ttu-id="3a211-114">如果訊息失敗，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="3a211-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a211-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a211-115">Requirements</span></span>



| <span data-ttu-id="3a211-116">需求</span><span class="sxs-lookup"><span data-stu-id="3a211-116">Requirement</span></span> | <span data-ttu-id="3a211-117">值</span><span class="sxs-lookup"><span data-stu-id="3a211-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a211-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a211-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a211-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a211-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a211-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a211-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a211-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a211-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a211-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3a211-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a211-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3a211-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a211-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a211-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a211-125">**CB \_ GETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="3a211-125">**CB\_GETTOPINDEX**</span></span>](cb-gettopindex.md)
</dt> </dl>

 

 





