---
title: 'LVM_SETCOLUMN 訊息 (Commctrl .h) '
description: 設定清單視圖資料行的屬性。 您可以明確地傳送此訊息，或使用 ListView \_ SetColumn 宏來傳送。
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934412"
---
# <a name="lvm_setcolumn-message"></a><span data-ttu-id="d6787-105">LVM \_ SETCOLUMN 訊息</span><span class="sxs-lookup"><span data-stu-id="d6787-105">LVM\_SETCOLUMN message</span></span>

<span data-ttu-id="d6787-106">設定清單視圖資料行的屬性。</span><span class="sxs-lookup"><span data-stu-id="d6787-106">Sets the attributes of a list-view column.</span></span> <span data-ttu-id="d6787-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="d6787-107">You can send this message explicitly or by using the [**ListView\_SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6787-108">參數</span><span class="sxs-lookup"><span data-stu-id="d6787-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6787-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6787-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6787-110">資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="d6787-110">Index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="d6787-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6787-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6787-112">[**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構的指標，其中包含新的資料行屬性。</span><span class="sxs-lookup"><span data-stu-id="d6787-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the new column attributes.</span></span> <span data-ttu-id="d6787-113">**遮罩** 成員會指定要設定的資料行屬性。</span><span class="sxs-lookup"><span data-stu-id="d6787-113">The **mask** member specifies which column attributes to set.</span></span> <span data-ttu-id="d6787-114">如果 **遮罩** 成員指定 LVCF \_ 文字值，則 **pszText** 成員是以 null 結束之字串的位址，而且會忽略 **cchTextMax** 成員。</span><span class="sxs-lookup"><span data-stu-id="d6787-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6787-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6787-115">Return value</span></span>

<span data-ttu-id="d6787-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d6787-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6787-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6787-117">Requirements</span></span>



| <span data-ttu-id="d6787-118">需求</span><span class="sxs-lookup"><span data-stu-id="d6787-118">Requirement</span></span> | <span data-ttu-id="d6787-119">值</span><span class="sxs-lookup"><span data-stu-id="d6787-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6787-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6787-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d6787-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6787-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6787-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6787-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d6787-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6787-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6787-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d6787-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6787-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6787-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d6787-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d6787-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d6787-127">**LVM \_SETCOLUMNW** (Unicode) 和 **LVM \_ SETCOLUMNW** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d6787-127">**LVM\_SETCOLUMNW** (Unicode) and **LVM\_SETCOLUMNW** (ANSI)</span></span><br/>               |



 

 





