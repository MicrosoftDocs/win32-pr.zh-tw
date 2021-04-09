---
title: 'LVN_HOTTRACK (Commctrl 的通知碼) '
description: 當使用者將滑鼠移到專案上時，由清單視圖控制項所傳送。 只有具有 LVS) \_ EX \_ TRACKSELECT 擴充清單視圖樣式的清單視圖控制項才會傳送此通知碼。 它是以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844475"
---
# <a name="lvn_hottrack-notification-code"></a><span data-ttu-id="14da9-106">LVN \_ HOTTRACK 通知碼</span><span class="sxs-lookup"><span data-stu-id="14da9-106">LVN\_HOTTRACK notification code</span></span>

<span data-ttu-id="14da9-107">當使用者將滑鼠移到專案上時，由清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="14da9-107">Sent by a list-view control when the user moves the mouse over an item.</span></span> <span data-ttu-id="14da9-108">只有具有 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) 擴充清單視圖樣式的清單視圖控制項才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="14da9-108">This notification code is only sent by list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) extended list-view style.</span></span> <span data-ttu-id="14da9-109">它是以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="14da9-109">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="14da9-110">參數</span><span class="sxs-lookup"><span data-stu-id="14da9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14da9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14da9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14da9-112">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14da9-112">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that contains information about this notification code.</span></span> <span data-ttu-id="14da9-113">此結構的 **iItem**、 **iSubItem** 和 **ptAction** 成員包含專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14da9-113">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span> <span data-ttu-id="14da9-114">接收應用程式可以修改 **iItem** 成員，以指定將選取的專案。</span><span class="sxs-lookup"><span data-stu-id="14da9-114">The receiving application can modify the **iItem** member to specify the item that will be selected.</span></span> <span data-ttu-id="14da9-115">如果 **iItem** 設為-1，則不會選取任何專案。</span><span class="sxs-lookup"><span data-stu-id="14da9-115">If **iItem** is set to -1, no item will be selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14da9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="14da9-116">Return value</span></span>

<span data-ttu-id="14da9-117">傳回零以允許清單視圖執行其一般追蹤選取處理。</span><span class="sxs-lookup"><span data-stu-id="14da9-117">Return zero to allow the list view to perform its normal track select processing.</span></span> <span data-ttu-id="14da9-118">如果應用程式傳回非零值，則不會選取該專案。</span><span class="sxs-lookup"><span data-stu-id="14da9-118">If the application returns nonzero, the item will not be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="14da9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="14da9-119">Requirements</span></span>



| <span data-ttu-id="14da9-120">需求</span><span class="sxs-lookup"><span data-stu-id="14da9-120">Requirement</span></span> | <span data-ttu-id="14da9-121">值</span><span class="sxs-lookup"><span data-stu-id="14da9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14da9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14da9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14da9-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14da9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14da9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14da9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14da9-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14da9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14da9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="14da9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="14da9-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="14da9-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





