---
title: 'LVM_GETCOUNTPERPAGE 訊息 (Commctrl .h) '
description: 當在清單或報表檢視中時，計算可在清單視圖控制項可見區域中垂直容納的專案數。 只會計算完全可見的專案。 您可以明確地傳送此訊息，或使用 ListView \_ GetCountPerPage 宏來傳送。
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024594"
---
# <a name="lvm_getcountperpage-message"></a><span data-ttu-id="8baac-106">LVM \_ GETCOUNTPERPAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="8baac-106">LVM\_GETCOUNTPERPAGE message</span></span>

<span data-ttu-id="8baac-107">當在清單或報表檢視中時，計算可在清單視圖控制項可見區域中垂直容納的專案數。</span><span class="sxs-lookup"><span data-stu-id="8baac-107">Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view.</span></span> <span data-ttu-id="8baac-108">只會計算完全可見的專案。</span><span class="sxs-lookup"><span data-stu-id="8baac-108">Only fully visible items are counted.</span></span> <span data-ttu-id="8baac-109">您可以明確地傳送此訊息，或使用 [**ListView \_ GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="8baac-109">You can send this message explicitly or by using the [**ListView\_GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8baac-110">參數</span><span class="sxs-lookup"><span data-stu-id="8baac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8baac-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8baac-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8baac-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8baac-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8baac-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8baac-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8baac-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8baac-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8baac-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8baac-115">Return value</span></span>

<span data-ttu-id="8baac-116">如果成功，則傳回完整可見專案的數目。</span><span class="sxs-lookup"><span data-stu-id="8baac-116">Returns the number of fully visible items if successful.</span></span> <span data-ttu-id="8baac-117">如果目前的視圖是圖示或小型圖示視圖，則傳回值是清單視圖控制項中的專案總數。</span><span class="sxs-lookup"><span data-stu-id="8baac-117">If the current view is icon or small icon view, the return value is the total number of items in the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8baac-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8baac-118">Requirements</span></span>



| <span data-ttu-id="8baac-119">需求</span><span class="sxs-lookup"><span data-stu-id="8baac-119">Requirement</span></span> | <span data-ttu-id="8baac-120">值</span><span class="sxs-lookup"><span data-stu-id="8baac-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8baac-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8baac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8baac-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8baac-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8baac-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8baac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8baac-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8baac-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8baac-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8baac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8baac-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8baac-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





