---
title: 'LVM_GETITEM 訊息 (Commctrl .h) '
description: 抓取部分或全部清單視圖專案的屬性。 您可以明確地傳送此訊息，或使用 ListView \_ GetItem 宏來傳送。
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686281"
---
# <a name="lvm_getitem-message"></a><span data-ttu-id="db1e6-105">LVM \_ GETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="db1e6-105">LVM\_GETITEM message</span></span>

<span data-ttu-id="db1e6-106">抓取部分或全部清單視圖專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="db1e6-106">Retrieves some or all of a list-view item's attributes.</span></span> <span data-ttu-id="db1e6-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="db1e6-107">You can send this message explicitly or by using the [**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="db1e6-108">參數</span><span class="sxs-lookup"><span data-stu-id="db1e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db1e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db1e6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="db1e6-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="db1e6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="db1e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db1e6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db1e6-112">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標，此結構會指定要取出的資訊，並接收清單視圖專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="db1e6-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the information to retrieve and receives information about the list-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db1e6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="db1e6-113">Return value</span></span>

<span data-ttu-id="db1e6-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="db1e6-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="db1e6-115">備註</span><span class="sxs-lookup"><span data-stu-id="db1e6-115">Remarks</span></span>

<span data-ttu-id="db1e6-116">當 **LVM \_ GETITEM** 訊息傳送時， **iItem** 和 **iSubItem** 成員會識別要抓取相關資訊的專案或子專案，而 **遮罩** 成員會指定要取出哪些屬性。</span><span class="sxs-lookup"><span data-stu-id="db1e6-116">When the **LVM\_GETITEM** message is sent, the **iItem** and **iSubItem** members identify the item or subitem to retrieve information about and the **mask** member specifies which attributes to retrieve.</span></span> <span data-ttu-id="db1e6-117">如需可能值的清單，請參閱 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的描述。</span><span class="sxs-lookup"><span data-stu-id="db1e6-117">For a list of possible values, see the description of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

<span data-ttu-id="db1e6-118">如果 LVIF \_ 文字旗標是在 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **mask** 成員中設定，則 **pszText** 成員必須指向有效的緩衝區，而且 **cchTextMax** 成員必須設定為該緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="db1e6-118">If the LVIF\_TEXT flag is set in the **mask** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span> <span data-ttu-id="db1e6-119">應用程式不應假設文字一定會放在指定的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="db1e6-119">Applications should not assume that the text will necessarily be placed in the specified buffer.</span></span> <span data-ttu-id="db1e6-120">控制項可以改為將結構的 **pszText** 成員變更為指向新的文字，而不是將它放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="db1e6-120">The control may instead change the **pszText** member of the structure to point to the new text, rather than place it in the buffer.</span></span>

<span data-ttu-id="db1e6-121">如果 **mask** 成員指定 LVIF \_ 狀態值， **stateMask** 成員就必須指定要取出的專案狀態位。</span><span class="sxs-lookup"><span data-stu-id="db1e6-121">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member must specify the item state bits to retrieve.</span></span> <span data-ttu-id="db1e6-122">在輸出時， **狀態** 成員會包含指定之狀態位的值。</span><span class="sxs-lookup"><span data-stu-id="db1e6-122">On output, the **state** member contains the values of the specified state bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="db1e6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="db1e6-123">Requirements</span></span>



| <span data-ttu-id="db1e6-124">需求</span><span class="sxs-lookup"><span data-stu-id="db1e6-124">Requirement</span></span> | <span data-ttu-id="db1e6-125">值</span><span class="sxs-lookup"><span data-stu-id="db1e6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db1e6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db1e6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="db1e6-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db1e6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db1e6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db1e6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="db1e6-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db1e6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db1e6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="db1e6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="db1e6-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="db1e6-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="db1e6-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="db1e6-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db1e6-133">**LVM \_GETITEMW** (Unicode) 和 **LVM \_ GETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="db1e6-133">**LVM\_GETITEMW** (Unicode) and **LVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





