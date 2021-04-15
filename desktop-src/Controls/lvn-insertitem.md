---
title: 'LVN_INSERTITEM (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，指出已插入新專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba70ba806dea2725385badee4b5c57e927a9d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467120"
---
# <a name="lvn_insertitem-notification-code"></a><span data-ttu-id="e2ea8-105">LVN \_ INSERTITEM 通知碼</span><span class="sxs-lookup"><span data-stu-id="e2ea8-105">LVN\_INSERTITEM notification code</span></span>

<span data-ttu-id="e2ea8-106">通知清單視圖控制項的父視窗，指出已插入新專案。</span><span class="sxs-lookup"><span data-stu-id="e2ea8-106">Notifies a list-view control's parent window that a new item was inserted.</span></span> <span data-ttu-id="e2ea8-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e2ea8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e2ea8-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2ea8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ea8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2ea8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2ea8-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e2ea8-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="e2ea8-111">**IItem** 成員會識別新的專案，而其他成員則為零。</span><span class="sxs-lookup"><span data-stu-id="e2ea8-111">The **iItem** member identifies the new item, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ea8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2ea8-112">Return value</span></span>

<span data-ttu-id="e2ea8-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e2ea8-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ea8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2ea8-114">Requirements</span></span>



| <span data-ttu-id="e2ea8-115">需求</span><span class="sxs-lookup"><span data-stu-id="e2ea8-115">Requirement</span></span> | <span data-ttu-id="e2ea8-116">值</span><span class="sxs-lookup"><span data-stu-id="e2ea8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ea8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2ea8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ea8-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2ea8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2ea8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2ea8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ea8-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2ea8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2ea8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e2ea8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2ea8-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ea8-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





