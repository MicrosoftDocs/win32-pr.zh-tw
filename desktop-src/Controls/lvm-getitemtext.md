---
title: 'LVM_GETITEMTEXT 訊息 (Commctrl .h) '
description: 抓取清單視圖專案或子專案的文字。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemText 宏來傳送。
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105503"
---
# <a name="lvm_getitemtext-message"></a><span data-ttu-id="6506a-105">LVM \_ GETITEMTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="6506a-105">LVM\_GETITEMTEXT message</span></span>

<span data-ttu-id="6506a-106">抓取清單視圖專案或子專案的文字。</span><span class="sxs-lookup"><span data-stu-id="6506a-106">Retrieves the text of a list-view item or subitem.</span></span> <span data-ttu-id="6506a-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="6506a-107">You can send this message explicitly or by using the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6506a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6506a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6506a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6506a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6506a-110">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="6506a-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="6506a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6506a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6506a-112">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6506a-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="6506a-113">若要取出專案文字，請將 **iSubItem** 設定為零。</span><span class="sxs-lookup"><span data-stu-id="6506a-113">To retrieve the item text, set **iSubItem** to zero.</span></span> <span data-ttu-id="6506a-114">若要取出子工作的文字，請將 **iSubItem** 設定為子索引。</span><span class="sxs-lookup"><span data-stu-id="6506a-114">To retrieve the text of a subitem, set **iSubItem** to the subitem's index.</span></span> <span data-ttu-id="6506a-115">**PszText** 成員指向接收文字的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6506a-115">The **pszText** member points to a buffer that receives the text.</span></span> <span data-ttu-id="6506a-116">**CchTextMax** 成員會指定緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="6506a-116">The **cchTextMax** member specifies the number of characters in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6506a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6506a-117">Return value</span></span>

<span data-ttu-id="6506a-118">如果您明確地傳送此訊息，它會傳回 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構之 **pszText** 成員中的字元數。</span><span class="sxs-lookup"><span data-stu-id="6506a-118">If you send this message explicitly, it returns the number of characters in the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6506a-119">備註</span><span class="sxs-lookup"><span data-stu-id="6506a-119">Remarks</span></span>

<span data-ttu-id="6506a-120">您也可以藉由呼叫 [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="6506a-120">You can also send this message by calling the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span> <span data-ttu-id="6506a-121">不過，此宏不會傳回字串長度。</span><span class="sxs-lookup"><span data-stu-id="6506a-121">However, this macro does not return the string length.</span></span>

<span data-ttu-id="6506a-122">**LVM \_** [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)樣式下不支援 GETITEMTEXT。</span><span class="sxs-lookup"><span data-stu-id="6506a-122">**LVM\_GETITEMTEXT** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6506a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6506a-123">Requirements</span></span>



| <span data-ttu-id="6506a-124">需求</span><span class="sxs-lookup"><span data-stu-id="6506a-124">Requirement</span></span> | <span data-ttu-id="6506a-125">值</span><span class="sxs-lookup"><span data-stu-id="6506a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6506a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6506a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6506a-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6506a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6506a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6506a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6506a-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6506a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6506a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6506a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6506a-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6506a-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6506a-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6506a-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6506a-133">**LVM \_GETITEMTEXTW** (Unicode) 和 **LVM \_ GETITEMTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6506a-133">**LVM\_GETITEMTEXTW** (Unicode) and **LVM\_GETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





