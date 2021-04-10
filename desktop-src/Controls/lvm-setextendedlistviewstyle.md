---
title: 'LVM_SETEXTENDEDLISTVIEWSTYLE 訊息 (Commctrl .h) '
description: 在清單視圖控制項中設定延伸樣式。 您可以明確地傳送此訊息，或使用 ListView \_ SetExtendedListViewStyle 或 listview \_ SetExtendedListViewStyleEx 宏。
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933921"
---
# <a name="lvm_setextendedlistviewstyle-message"></a><span data-ttu-id="e20b1-105">LVM \_ SETEXTENDEDLISTVIEWSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="e20b1-105">LVM\_SETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="e20b1-106">在清單視圖控制項中設定延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="e20b1-106">Sets extended styles in list-view controls.</span></span> <span data-ttu-id="e20b1-107">您可以明確地傳送此訊息，或使用 [**listview \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) 或 [**listview \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) 宏。</span><span class="sxs-lookup"><span data-stu-id="e20b1-107">You can send this message explicitly or use the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) or [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e20b1-108">參數</span><span class="sxs-lookup"><span data-stu-id="e20b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e20b1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e20b1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e20b1-110">**DWORD** 值，指定要對 *lParam* 中的哪些樣式造成影響。</span><span class="sxs-lookup"><span data-stu-id="e20b1-110">**DWORD** value that specifies which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="e20b1-111">這個參數可以是 [**延伸 List-View 樣式**](extended-list-view-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="e20b1-111">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="e20b1-112">只有 *wParam* 中的擴充樣式會變更。</span><span class="sxs-lookup"><span data-stu-id="e20b1-112">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="e20b1-113">所有其他樣式都會維持不變。</span><span class="sxs-lookup"><span data-stu-id="e20b1-113">All other styles will be maintained as they are.</span></span> <span data-ttu-id="e20b1-114">如果此參數為零，則 *lParam* 中的所有樣式都會受到影響。</span><span class="sxs-lookup"><span data-stu-id="e20b1-114">If this parameter is zero, all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="e20b1-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e20b1-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e20b1-116">**DWORD** 值，指定要設定的擴充清單視圖控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="e20b1-116">**DWORD** value that specifies the extended list-view control styles to set.</span></span> <span data-ttu-id="e20b1-117">這個參數可以是 [**延伸 List-View 樣式**](extended-list-view-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="e20b1-117">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="e20b1-118">未設定，但在 *wParam* 中指定的樣式會被移除。</span><span class="sxs-lookup"><span data-stu-id="e20b1-118">Styles that are not set, but that are specified in *wParam*, are removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e20b1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e20b1-119">Return value</span></span>

<span data-ttu-id="e20b1-120">傳回包含先前的擴充清單視圖控制項樣式的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="e20b1-120">Returns a **DWORD** value that contains the previous extended list-view control styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="e20b1-121">備註</span><span class="sxs-lookup"><span data-stu-id="e20b1-121">Remarks</span></span>

<span data-ttu-id="e20b1-122">*WParam* 參數可讓您修改一或多個擴充樣式，而不需要先取出現有的樣式。</span><span class="sxs-lookup"><span data-stu-id="e20b1-122">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="e20b1-123">例如，如果您傳遞 [**lvs) 的 \_ \_ FULLROWSELECT**](extended-list-view-styles.md) for *wParam* 和0（ *lParam*），將會清除 **lvs) \_ EX \_ FULLROWSELECT** 樣式，但所有其他樣式都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="e20b1-123">For example, if you pass [**LVS\_EX\_FULLROWSELECT**](extended-list-view-styles.md) for *wParam* and 0 for *lParam*, the **LVS\_EX\_FULLROWSELECT** style will be cleared but all other styles will remain the same.</span></span>

<span data-ttu-id="e20b1-124">基於回溯相容性的理由， [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) 宏尚未更新為使用 *wParam*。</span><span class="sxs-lookup"><span data-stu-id="e20b1-124">For backward compatibility reasons, the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) macro has not been updated to use *wParam*.</span></span> <span data-ttu-id="e20b1-125">若要使用 *wParam* 值，請使用 [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) 宏。</span><span class="sxs-lookup"><span data-stu-id="e20b1-125">To use the *wParam* value, use the [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

<span data-ttu-id="e20b1-126">當您使用此訊息來設定 [**lvs) \_ EX \_ 核取方塊**](extended-list-view-styles.md) 樣式時，將會捨棄任何先前設定的狀態影像索引。</span><span class="sxs-lookup"><span data-stu-id="e20b1-126">When you use this message to set the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style, any previously set state image index will be discarded.</span></span> <span data-ttu-id="e20b1-127">所有核取方塊都會初始化為未核取的狀態。</span><span class="sxs-lookup"><span data-stu-id="e20b1-127">All check boxes will be initialized to the unchecked state.</span></span> <span data-ttu-id="e20b1-128">狀態影像索引是包含在 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **state** 成員中的位12到15。</span><span class="sxs-lookup"><span data-stu-id="e20b1-128">The state image index is contained in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e20b1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e20b1-129">Requirements</span></span>



| <span data-ttu-id="e20b1-130">需求</span><span class="sxs-lookup"><span data-stu-id="e20b1-130">Requirement</span></span> | <span data-ttu-id="e20b1-131">值</span><span class="sxs-lookup"><span data-stu-id="e20b1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e20b1-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e20b1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e20b1-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e20b1-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e20b1-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e20b1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e20b1-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e20b1-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e20b1-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e20b1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20b1-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e20b1-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





