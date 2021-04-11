---
title: 'LVM_SETITEMTEXT 訊息 (Commctrl .h) '
description: 變更清單視圖專案或子專案的文字。 您可以明確地傳送此訊息，或使用 ListView \_ SetItemText 宏來傳送。
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843664"
---
# <a name="lvm_setitemtext-message"></a><span data-ttu-id="d505e-105">LVM \_ SETITEMTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="d505e-105">LVM\_SETITEMTEXT message</span></span>

<span data-ttu-id="d505e-106">變更清單視圖專案或子專案的文字。</span><span class="sxs-lookup"><span data-stu-id="d505e-106">Changes the text of a list-view item or subitem.</span></span> <span data-ttu-id="d505e-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="d505e-107">You can send this message explicitly or by using the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d505e-108">參數</span><span class="sxs-lookup"><span data-stu-id="d505e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d505e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d505e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d505e-110">清單視圖專案的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="d505e-110">Zero-based index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="d505e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d505e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d505e-112">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d505e-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="d505e-113">**ISubItem** 成員是子專案的索引，或者可以是零來設定專案標籤。</span><span class="sxs-lookup"><span data-stu-id="d505e-113">The **iSubItem** member is the index of the subitem, or it can be zero to set the item label.</span></span> <span data-ttu-id="d505e-114">**PszText** 成員是以 null 終止之字串的位址，其中包含新的文字;它也可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d505e-114">The **pszText** member is the address of a null-terminated string containing the new text; it can also be **NULL**.</span></span> <span data-ttu-id="d505e-115">**PszText** 成員也可以是 LPSTR \_ TEXTCALLBACK，以表示父視窗儲存文字的回撥專案。</span><span class="sxs-lookup"><span data-stu-id="d505e-115">The **pszText** member can also be LPSTR\_TEXTCALLBACK to indicate a callback item for which the parent window stores the text.</span></span> <span data-ttu-id="d505e-116">在此情況下，清單視圖控制項會在需要文字時，傳送 [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) 通知碼給父系。</span><span class="sxs-lookup"><span data-stu-id="d505e-116">In this case, the list-view control sends the parent an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code when it needs the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d505e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d505e-117">Return value</span></span>

<span data-ttu-id="d505e-118">如果您明確傳送此訊息，則會在成功時傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d505e-118">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d505e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d505e-119">Requirements</span></span>



| <span data-ttu-id="d505e-120">需求</span><span class="sxs-lookup"><span data-stu-id="d505e-120">Requirement</span></span> | <span data-ttu-id="d505e-121">值</span><span class="sxs-lookup"><span data-stu-id="d505e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d505e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d505e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d505e-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d505e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d505e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d505e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d505e-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d505e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d505e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d505e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d505e-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d505e-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d505e-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d505e-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d505e-129">**LVM \_SETITEMTEXTW** (Unicode) 和 **LVM \_ SETITEMTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d505e-129">**LVM\_SETITEMTEXTW** (Unicode) and **LVM\_SETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





