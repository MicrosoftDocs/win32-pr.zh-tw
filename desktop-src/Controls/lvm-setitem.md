---
title: 'LVM_SETITEM 訊息 (Commctrl .h) '
description: 設定部分或全部清單視圖專案的屬性。 您也可以傳送 LVM \_ SETITEM 來設定子內容的文字。 您可以明確地傳送此訊息，或使用 ListView \_ SetItem 宏來傳送。
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024859"
---
# <a name="lvm_setitem-message"></a><span data-ttu-id="102ef-106">LVM \_ SETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="102ef-106">LVM\_SETITEM message</span></span>

<span data-ttu-id="102ef-107">設定部分或全部清單視圖專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="102ef-107">Sets some or all of a list-view item's attributes.</span></span> <span data-ttu-id="102ef-108">您也可以傳送 LVM \_ SETITEM 來設定子內容的文字。</span><span class="sxs-lookup"><span data-stu-id="102ef-108">You can also send LVM\_SETITEM to set the text of a subitem.</span></span> <span data-ttu-id="102ef-109">您可以明確地傳送此訊息，或使用 [**ListView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="102ef-109">You can send this message explicitly or by using the [**ListView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="102ef-110">參數</span><span class="sxs-lookup"><span data-stu-id="102ef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102ef-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="102ef-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="102ef-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="102ef-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="102ef-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="102ef-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="102ef-114">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標，其中包含新的專案屬性。</span><span class="sxs-lookup"><span data-stu-id="102ef-114">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="102ef-115">**IItem** 和 **iSubItem** 成員會識別專案或子專案，而 **遮罩** 成員會指定要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="102ef-115">The **iItem** and **iSubItem** members identify the item or subitem, and the **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="102ef-116">如果 **遮罩** 成員指定 LVIF \_ 文字值，則 **pszText** 成員是以 null 結束之字串的位址，而且會忽略 **cchTextMax** 成員。</span><span class="sxs-lookup"><span data-stu-id="102ef-116">If the **mask** member specifies the LVIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span> <span data-ttu-id="102ef-117">如果 **遮罩** 成員指定 LVIF \_ 狀態值， **stateMask** 成員就會指定要變更的專案狀態，而 **狀態** 成員會包含這些狀態的值。</span><span class="sxs-lookup"><span data-stu-id="102ef-117">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member specifies which item states to change and the **state** member contains the values for those states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102ef-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="102ef-118">Return value</span></span>

<span data-ttu-id="102ef-119">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="102ef-119">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="102ef-120">備註</span><span class="sxs-lookup"><span data-stu-id="102ef-120">Remarks</span></span>

<span data-ttu-id="102ef-121">若要設定清單視圖專案的屬性，請將 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **iItem** 成員設定為專案的索引，並將 **iSubItem** 成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="102ef-121">To set the attributes of a list-view item, set the **iItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the index of the item, and set the **iSubItem** member to zero.</span></span> <span data-ttu-id="102ef-122">針對某個專案，您可以設定 **LVITEM** 結構的 **state**、 **pszText**、 **iImage** 和 **lParam** 成員。</span><span class="sxs-lookup"><span data-stu-id="102ef-122">For an item, you can set the **state**, **pszText**, **iImage**, and **lParam** members of the **LVITEM** structure.</span></span>

<span data-ttu-id="102ef-123">若要設定子集合的文字，請設定 **iItem** 和 **iSubItem** 成員來指出特定的子工作，並使用 **pszText** 成員來指定文字。</span><span class="sxs-lookup"><span data-stu-id="102ef-123">To set the text of a subitem, set the **iItem** and **iSubItem** members to indicate the specific subitem, and use the **pszText** member to specify the text.</span></span> <span data-ttu-id="102ef-124">或者，您也可以使用 [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) 宏來設定子內容的文字。</span><span class="sxs-lookup"><span data-stu-id="102ef-124">Alternatively, you can use the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro to set the text of a subitem.</span></span> <span data-ttu-id="102ef-125">您無法設定子屬性的 **狀態** 或 **lParam** 成員，因為子集合沒有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="102ef-125">You cannot set the **state** or **lParam** members for subitems because subitems do not have these attributes.</span></span> <span data-ttu-id="102ef-126">在4.70 版和更新版本中，您可以設定子集合的 **iImage** 成員。</span><span class="sxs-lookup"><span data-stu-id="102ef-126">In version 4.70 and later, you can set the **iImage** member for subitems.</span></span> <span data-ttu-id="102ef-127">如果清單視圖控制項具有 [**lvs) \_ EX \_ SUBITEMIMAGES**](extended-list-view-styles.md) 擴充樣式，則會顯示子元件映射。</span><span class="sxs-lookup"><span data-stu-id="102ef-127">The subitem image will be displayed if the list-view control has the [**LVS\_EX\_SUBITEMIMAGES**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="102ef-128">先前的版本會忽略子工作映射。</span><span class="sxs-lookup"><span data-stu-id="102ef-128">Previous versions will ignore the subitem image.</span></span>

## <a name="requirements"></a><span data-ttu-id="102ef-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="102ef-129">Requirements</span></span>



| <span data-ttu-id="102ef-130">需求</span><span class="sxs-lookup"><span data-stu-id="102ef-130">Requirement</span></span> | <span data-ttu-id="102ef-131">值</span><span class="sxs-lookup"><span data-stu-id="102ef-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="102ef-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="102ef-132">Minimum supported client</span></span><br/> | <span data-ttu-id="102ef-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="102ef-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="102ef-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="102ef-134">Minimum supported server</span></span><br/> | <span data-ttu-id="102ef-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="102ef-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="102ef-136">標頭</span><span class="sxs-lookup"><span data-stu-id="102ef-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="102ef-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="102ef-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="102ef-138">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="102ef-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="102ef-139">**LVM \_SETITEMW** (Unicode) 和 **LVM \_ SETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="102ef-139">**LVM\_SETITEMW** (Unicode) and **LVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





