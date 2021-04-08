---
title: 'NM_DBLCLK (清單視圖) 通知碼 (Commctrl) '
description: 當使用者使用滑鼠左鍵按兩下專案時，由清單視圖控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- NM_DBLCLK (清單視圖) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add6af24b4272631be7c2be387a7ffda899469b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843080"
---
# <a name="nm_dblclk-list-view-notification-code"></a><span data-ttu-id="e49d7-105">NM \_ DBLCLK (清單視圖) 通知碼</span><span class="sxs-lookup"><span data-stu-id="e49d7-105">NM\_DBLCLK (list view) notification code</span></span>

<span data-ttu-id="e49d7-106">當使用者使用滑鼠左鍵按兩下專案時，由清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="e49d7-106">Sent by a list-view control when the user double-clicks an item with the left mouse button.</span></span> <span data-ttu-id="e49d7-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e49d7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e49d7-108">參數</span><span class="sxs-lookup"><span data-stu-id="e49d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e49d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e49d7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e49d7-110">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="e49d7-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="e49d7-111">[**NMITEMACTI加值稅E**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e49d7-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="e49d7-112">此結構的 **iItem**、 **iSubItem** 和 **ptAction** 成員包含專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e49d7-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e49d7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e49d7-113">Return value</span></span>

<span data-ttu-id="e49d7-114">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e49d7-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e49d7-115">備註</span><span class="sxs-lookup"><span data-stu-id="e49d7-115">Remarks</span></span>

<span data-ttu-id="e49d7-116">只有在按一下圖示或第一個資料行的標籤時， *lParam* 的 **iItem** 成員才有效。</span><span class="sxs-lookup"><span data-stu-id="e49d7-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="e49d7-117">若要判斷在某個資料列中的其他地方發生按一下時所要選取的專案，請傳送 [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="e49d7-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e49d7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e49d7-118">Requirements</span></span>



| <span data-ttu-id="e49d7-119">需求</span><span class="sxs-lookup"><span data-stu-id="e49d7-119">Requirement</span></span> | <span data-ttu-id="e49d7-120">值</span><span class="sxs-lookup"><span data-stu-id="e49d7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e49d7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e49d7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e49d7-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e49d7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e49d7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e49d7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e49d7-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e49d7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e49d7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e49d7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e49d7-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e49d7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





