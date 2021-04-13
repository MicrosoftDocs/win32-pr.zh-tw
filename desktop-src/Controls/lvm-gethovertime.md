---
title: 'LVM_GETHOVERTIME 訊息 (Commctrl .h) '
description: 抓取在選取專案之前，滑鼠游標必須停留在某個專案上的時間量。 您可以明確地傳送此訊息，或使用 ListView \_ GetHoverTime 宏。
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465880"
---
# <a name="lvm_gethovertime-message"></a><span data-ttu-id="002e4-105">LVM \_ GETHOVERTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="002e4-105">LVM\_GETHOVERTIME message</span></span>

<span data-ttu-id="002e4-106">抓取在選取專案之前，滑鼠游標必須停留在某個專案上的時間量。</span><span class="sxs-lookup"><span data-stu-id="002e4-106">Retrieves the amount of time that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="002e4-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) 宏。</span><span class="sxs-lookup"><span data-stu-id="002e4-107">You can send this message explicitly or use the [**ListView\_GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="002e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="002e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002e4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="002e4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="002e4-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="002e4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="002e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="002e4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="002e4-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="002e4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002e4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="002e4-113">Return value</span></span>

<span data-ttu-id="002e4-114">傳回在選取專案之前，滑鼠游標必須停留在某個專案上的時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="002e4-114">Returns the amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="002e4-115">如果傳回值是 (**DWORD**) -1，則停留時間是預設的停留時間。</span><span class="sxs-lookup"><span data-stu-id="002e4-115">If the return value is (**DWORD**)-1, then the hover time is the default hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="002e4-116">備註</span><span class="sxs-lookup"><span data-stu-id="002e4-116">Remarks</span></span>

<span data-ttu-id="002e4-117">暫止的時間只會影響具有 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md)、 [**lvs) \_ ex \_ ONECLICKACTI加值稅E**](extended-list-view-styles.md)或 [**lvs) \_ ex \_ TWOCLICKACTI加值稅E**](extended-list-view-styles.md) 擴充清單視圖樣式的清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="002e4-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="002e4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="002e4-118">Requirements</span></span>



| <span data-ttu-id="002e4-119">需求</span><span class="sxs-lookup"><span data-stu-id="002e4-119">Requirement</span></span> | <span data-ttu-id="002e4-120">值</span><span class="sxs-lookup"><span data-stu-id="002e4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="002e4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="002e4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="002e4-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="002e4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="002e4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="002e4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="002e4-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="002e4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="002e4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="002e4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="002e4-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="002e4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





