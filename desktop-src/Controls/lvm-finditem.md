---
title: 'LVM_FINDITEM 訊息 (Commctrl .h) '
description: 搜尋具有指定特性的清單視圖專案。 您可以明確地傳送此訊息，或使用 ListView \_ FindItem 宏來傳送。
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- LVM_FINDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464288"
---
# <a name="lvm_finditem-message"></a><span data-ttu-id="7a489-105">LVM \_ FINDITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="7a489-105">LVM\_FINDITEM message</span></span>

<span data-ttu-id="7a489-106">搜尋具有指定特性的清單視圖專案。</span><span class="sxs-lookup"><span data-stu-id="7a489-106">Searches for a list-view item with the specified characteristics.</span></span> <span data-ttu-id="7a489-107">您可以明確地傳送此訊息，或使用 [**ListView \_ FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="7a489-107">You can send this message explicitly or by using the [**ListView\_FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a489-108">參數</span><span class="sxs-lookup"><span data-stu-id="7a489-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a489-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a489-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a489-110">要開始搜尋的專案索引，或-1 會從頭開始。</span><span class="sxs-lookup"><span data-stu-id="7a489-110">The index of the item to begin the search with or -1 to start from the beginning.</span></span> <span data-ttu-id="7a489-111">從搜尋中排除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="7a489-111">The specified item is itself excluded from the search.</span></span>

</dd> <dt>

<span data-ttu-id="7a489-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a489-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a489-113">[**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa)結構的指標，其中包含要搜尋之內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7a489-113">A pointer to an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure that contains information about what to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a489-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a489-114">Return value</span></span>

<span data-ttu-id="7a489-115">如果成功，則傳回專案的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="7a489-115">Returns the index of the item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a489-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a489-116">Requirements</span></span>



| <span data-ttu-id="7a489-117">需求</span><span class="sxs-lookup"><span data-stu-id="7a489-117">Requirement</span></span> | <span data-ttu-id="7a489-118">值</span><span class="sxs-lookup"><span data-stu-id="7a489-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a489-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a489-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a489-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a489-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a489-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a489-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a489-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a489-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a489-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7a489-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a489-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a489-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7a489-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7a489-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7a489-126">**LVM \_FINDITEMW** (Unicode) 和 **LVM \_ FINDITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7a489-126">**LVM\_FINDITEMW** (Unicode) and **LVM\_FINDITEMA** (ANSI)</span></span><br/>                 |



 

 





