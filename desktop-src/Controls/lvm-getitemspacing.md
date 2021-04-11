---
title: 'LVM_GETITEMSPACING 訊息 (Commctrl .h) '
description: 決定清單視圖控制項中專案之間的間距。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemSpacing 宏來傳送。
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934898"
---
# <a name="lvm_getitemspacing-message"></a><span data-ttu-id="82b71-105">LVM \_ GETITEMSPACING 訊息</span><span class="sxs-lookup"><span data-stu-id="82b71-105">LVM\_GETITEMSPACING message</span></span>

<span data-ttu-id="82b71-106">決定清單視圖控制項中專案之間的間距。</span><span class="sxs-lookup"><span data-stu-id="82b71-106">Determines the spacing between items in a list-view control.</span></span> <span data-ttu-id="82b71-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="82b71-107">You can send this message explicitly or by using the [**ListView\_GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="82b71-108">參數</span><span class="sxs-lookup"><span data-stu-id="82b71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b71-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82b71-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82b71-110">要取得其專案間距的視圖。</span><span class="sxs-lookup"><span data-stu-id="82b71-110">View for which to retrieve the item spacing.</span></span> <span data-ttu-id="82b71-111">此參數適用 **于小型** 圖示視圖，或針對圖示視圖則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="82b71-111">This parameter is **TRUE** for small icon view, or **FALSE** for icon view.</span></span>

</dd> <dt>

<span data-ttu-id="82b71-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82b71-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="82b71-113">必須為零。</span><span class="sxs-lookup"><span data-stu-id="82b71-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b71-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="82b71-114">Return value</span></span>

<span data-ttu-id="82b71-115">傳回專案之間的間距量。</span><span class="sxs-lookup"><span data-stu-id="82b71-115">Returns the amount of spacing between items.</span></span> <span data-ttu-id="82b71-116">水準間距會包含在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中，而且垂直間距會包含在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中。</span><span class="sxs-lookup"><span data-stu-id="82b71-116">The horizontal spacing is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical spacing is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="82b71-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="82b71-117">Requirements</span></span>



| <span data-ttu-id="82b71-118">需求</span><span class="sxs-lookup"><span data-stu-id="82b71-118">Requirement</span></span> | <span data-ttu-id="82b71-119">值</span><span class="sxs-lookup"><span data-stu-id="82b71-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82b71-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82b71-120">Minimum supported client</span></span><br/> | <span data-ttu-id="82b71-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b71-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82b71-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82b71-122">Minimum supported server</span></span><br/> | <span data-ttu-id="82b71-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b71-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82b71-124">標頭</span><span class="sxs-lookup"><span data-stu-id="82b71-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b71-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="82b71-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

