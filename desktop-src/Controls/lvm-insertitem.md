---
title: 'LVM_INSERTITEM 訊息 (Commctrl .h) '
description: 在清單視圖控制項中插入新專案。 您可以明確地傳送此訊息，或使用 ListView \_ InsertItem 宏來傳送。
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969809"
---
# <a name="lvm_insertitem-message"></a><span data-ttu-id="a9f95-105">LVM \_ INSERTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="a9f95-105">LVM\_INSERTITEM message</span></span>

<span data-ttu-id="a9f95-106">在清單視圖控制項中插入新專案。</span><span class="sxs-lookup"><span data-stu-id="a9f95-106">Inserts a new item in a list-view control.</span></span> <span data-ttu-id="a9f95-107">您可以明確地傳送此訊息，或使用 [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="a9f95-107">You can send this message explicitly or by using the [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9f95-108">參數</span><span class="sxs-lookup"><span data-stu-id="a9f95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f95-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9f95-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a9f95-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a9f95-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a9f95-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9f95-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9f95-112">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標，指定清單視圖專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9f95-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the attributes of the list-view item.</span></span> <span data-ttu-id="a9f95-113">您可以使用 **iItem** 成員來指定以零為基底的索引，這是應該插入新專案的位置。</span><span class="sxs-lookup"><span data-stu-id="a9f95-113">Use the **iItem** member to specify the zero-based index at which the new item should be inserted.</span></span> <span data-ttu-id="a9f95-114">如果這個值大於 listview 目前所包含的專案數目，新的專案會附加至清單結尾並指派正確的索引。</span><span class="sxs-lookup"><span data-stu-id="a9f95-114">If this value is greater than the number of items currently contained by the listview, the new item will be appended to the end of the list and assigned the correct index.</span></span> <span data-ttu-id="a9f95-115">檢查訊息的傳回值，以判斷指派給專案的實際索引。</span><span class="sxs-lookup"><span data-stu-id="a9f95-115">Examine the message's return value to determine the actual index assigned to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f95-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9f95-116">Return value</span></span>

<span data-ttu-id="a9f95-117">如果成功，則傳回新專案的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="a9f95-117">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9f95-118">備註</span><span class="sxs-lookup"><span data-stu-id="a9f95-118">Remarks</span></span>

<span data-ttu-id="a9f95-119">您無法使用 [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) 或 **LVM \_ InsertItem** 插入子。</span><span class="sxs-lookup"><span data-stu-id="a9f95-119">You cannot use [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) or **LVM\_INSERTITEM** to insert subitems.</span></span> <span data-ttu-id="a9f95-120">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **iSubItem** 成員必須為零。</span><span class="sxs-lookup"><span data-stu-id="a9f95-120">The **iSubItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure must be zero.</span></span> <span data-ttu-id="a9f95-121">請參閱 [**LVM \_ SETITEM**](lvm-setitem.md) ，以取得設定子內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9f95-121">See [**LVM\_SETITEM**](lvm-setitem.md) for information on setting subitems.</span></span>

<span data-ttu-id="a9f95-122">如果清單視圖控制項已設定 [**lvs) \_ EX \_ 核取方塊**](extended-list-view-styles.md)樣式，則會忽略任何在 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構之 **狀態** 成員的位12到15中放置的值。</span><span class="sxs-lookup"><span data-stu-id="a9f95-122">If a list-view control has the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style set, any value placed in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure will be ignored.</span></span> <span data-ttu-id="a9f95-123">使用這個樣式集加入專案時，一律會將它設定為未核取的狀態。</span><span class="sxs-lookup"><span data-stu-id="a9f95-123">When an item is added with this style set, it will always be set to the unchecked state.</span></span>

<span data-ttu-id="a9f95-124">如果清單視圖控制項有 [ [**lvs) \_ SORTASCENDING**](list-view-window-styles.md) ] 或 [ [**lvs) \_ SORTDESCENDING**](list-view-window-styles.md) ] 視窗樣式，則當您嘗試插入具有 INSERTITEM LPSTR 的專案做為其 TEXTCALLBACK 成員的值時， **LVM \_ pszText** 訊息將會失敗 \_ 。 </span><span class="sxs-lookup"><span data-stu-id="a9f95-124">If a list-view control has either the [**LVS\_SORTASCENDING**](list-view-window-styles.md) or [**LVS\_SORTDESCENDING**](list-view-window-styles.md) window style, an **LVM\_INSERTITEM** message will fail if you try to insert an item that has LPSTR\_TEXTCALLBACK as the value for its **pszText** member.</span></span>

<span data-ttu-id="a9f95-125">如果下列條件成立， **LVM \_ INSERTITEM** 訊息會將新的專案插入排序次序中的適當位置：</span><span class="sxs-lookup"><span data-stu-id="a9f95-125">The **LVM\_INSERTITEM** message will insert the new item in the proper position in the sort order if the following conditions hold:</span></span>

-   <span data-ttu-id="a9f95-126">您使用的是其中一個 LVS) \_ SORTXXX 樣式。</span><span class="sxs-lookup"><span data-stu-id="a9f95-126">You are using one of the LVS\_SORTXXX styles.</span></span>
-   <span data-ttu-id="a9f95-127">您未使用 [**lvs) \_ OWNERDRAW**](list-view-window-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="a9f95-127">You are not using the [**LVS\_OWNERDRAW**](list-view-window-styles.md) style.</span></span>
-   <span data-ttu-id="a9f95-128">**Pitem** 所指向之結構的 **pszText** 成員未設定為 LPSTR \_ TEXTCALLBACK。</span><span class="sxs-lookup"><span data-stu-id="a9f95-128">The **pszText** member of the structure pointed to by **pitem** is not set to LPSTR\_TEXTCALLBACK.</span></span>

<span data-ttu-id="a9f95-129">如果 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構未 \_ 在 **遮罩** 成員中包含 LVIF GROUPID，則 **iGroupId** 成員的值預設為 I \_ GROUPIDCALLBACK。</span><span class="sxs-lookup"><span data-stu-id="a9f95-129">If the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure does not contain LVIF\_GROUPID in the **mask** member, the value of the **iGroupId** member is I\_GROUPIDCALLBACK by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f95-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9f95-130">Requirements</span></span>



| <span data-ttu-id="a9f95-131">需求</span><span class="sxs-lookup"><span data-stu-id="a9f95-131">Requirement</span></span> | <span data-ttu-id="a9f95-132">值</span><span class="sxs-lookup"><span data-stu-id="a9f95-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f95-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9f95-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f95-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9f95-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9f95-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9f95-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f95-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9f95-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9f95-137">標頭</span><span class="sxs-lookup"><span data-stu-id="a9f95-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9f95-138"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f95-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a9f95-139">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a9f95-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a9f95-140">**LVM \_INSERTITEMW** (Unicode) 和 **LVM \_ INSERTITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a9f95-140">**LVM\_INSERTITEMW** (Unicode) and **LVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





