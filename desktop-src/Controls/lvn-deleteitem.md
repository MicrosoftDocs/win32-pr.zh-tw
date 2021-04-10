---
title: 'LVN_DELETEITEM (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，指出即將刪除的專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106673"
---
# <a name="lvn_deleteitem-notification-code"></a><span data-ttu-id="53d11-105">LVN \_ DELETEITEM 通知碼</span><span class="sxs-lookup"><span data-stu-id="53d11-105">LVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="53d11-106">通知清單視圖控制項的父視窗，指出即將刪除的專案。</span><span class="sxs-lookup"><span data-stu-id="53d11-106">Notifies a list-view control's parent window that an item is about to be deleted.</span></span> <span data-ttu-id="53d11-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="53d11-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="53d11-108">參數</span><span class="sxs-lookup"><span data-stu-id="53d11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d11-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53d11-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53d11-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="53d11-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="53d11-111">**IItem** 成員會識別正在刪除的專案。</span><span class="sxs-lookup"><span data-stu-id="53d11-111">The **iItem** member identifies the item being deleted.</span></span> <span data-ttu-id="53d11-112">如果控制項沒有 **lvs) \_ OWNERDATA** 樣式，則 *lParam* 是與專案相關聯的應用程式定義資料。</span><span class="sxs-lookup"><span data-stu-id="53d11-112">If the control does not have the **LVS\_OWNERDATA** style, then the *lParam* is the application-defined data associated with the item.</span></span> <span data-ttu-id="53d11-113">此結構的所有其他成員都是零。</span><span class="sxs-lookup"><span data-stu-id="53d11-113">All other members of this structure are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d11-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="53d11-114">Return value</span></span>

<span data-ttu-id="53d11-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="53d11-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53d11-116">備註</span><span class="sxs-lookup"><span data-stu-id="53d11-116">Remarks</span></span>

<span data-ttu-id="53d11-117">處理此通知碼時，請勿新增、刪除或重新排列清單視圖中的專案。</span><span class="sxs-lookup"><span data-stu-id="53d11-117">Do not add, delete, or rearrange items in the list view while processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d11-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="53d11-118">Requirements</span></span>



| <span data-ttu-id="53d11-119">需求</span><span class="sxs-lookup"><span data-stu-id="53d11-119">Requirement</span></span> | <span data-ttu-id="53d11-120">值</span><span class="sxs-lookup"><span data-stu-id="53d11-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53d11-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53d11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53d11-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53d11-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53d11-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53d11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53d11-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53d11-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53d11-125">標頭</span><span class="sxs-lookup"><span data-stu-id="53d11-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="53d11-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="53d11-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





