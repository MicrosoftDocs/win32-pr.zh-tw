---
title: 'NM_RCLICK (清單視圖) 通知碼 (Commctrl) '
description: 當使用者以滑鼠右鍵按一下專案時，由清單視圖控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: dc7f97b3-4aec-4a8f-a87c-62cef5ba4c40
keywords:
- NM_RCLICK (清單視圖) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01c21f1b1e869a909dd41dcfce693bf084f2fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103914"
---
# <a name="nm_rclick-list-view-notification-code"></a><span data-ttu-id="a7888-105">NM \_ RCLICK (清單視圖) 通知碼</span><span class="sxs-lookup"><span data-stu-id="a7888-105">NM\_RCLICK (list view) notification code</span></span>

<span data-ttu-id="a7888-106">當使用者以滑鼠右鍵按一下專案時，由清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="a7888-106">Sent by a list-view control when the user clicks an item with the right mouse button.</span></span> <span data-ttu-id="a7888-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a7888-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a7888-108">參數</span><span class="sxs-lookup"><span data-stu-id="a7888-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7888-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7888-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7888-110">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="a7888-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="a7888-111">[**NMITEMACTI加值稅E**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a7888-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="a7888-112">此結構的 **iItem**、 **iSubItem** 和 **ptAction** 成員包含專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a7888-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7888-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7888-113">Return value</span></span>

<span data-ttu-id="a7888-114">傳回非零以允許預設處理，或零以允許預設處理。</span><span class="sxs-lookup"><span data-stu-id="a7888-114">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7888-115">備註</span><span class="sxs-lookup"><span data-stu-id="a7888-115">Remarks</span></span>

<span data-ttu-id="a7888-116">只有在按一下圖示或第一個資料行的標籤時， *lParam* 的 **iItem** 成員才有效。</span><span class="sxs-lookup"><span data-stu-id="a7888-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="a7888-117">若要判斷在某個資料列中的其他地方發生按一下時所要選取的專案，請傳送 [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a7888-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7888-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7888-118">Requirements</span></span>



| <span data-ttu-id="a7888-119">需求</span><span class="sxs-lookup"><span data-stu-id="a7888-119">Requirement</span></span> | <span data-ttu-id="a7888-120">值</span><span class="sxs-lookup"><span data-stu-id="a7888-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7888-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7888-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a7888-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7888-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7888-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7888-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a7888-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7888-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7888-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a7888-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7888-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7888-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





