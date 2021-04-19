---
title: 'LVN_ITEMCHANGED (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，指出專案已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980295"
---
# <a name="lvn_itemchanged-notification-code"></a><span data-ttu-id="45722-105">LVN \_ ITEMCHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="45722-105">LVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="45722-106">通知清單視圖控制項的父視窗，指出專案已變更。</span><span class="sxs-lookup"><span data-stu-id="45722-106">Notifies a list-view control's parent window that an item has changed.</span></span> <span data-ttu-id="45722-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="45722-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="45722-108">參數</span><span class="sxs-lookup"><span data-stu-id="45722-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45722-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45722-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45722-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標，該結構會識別專案並指定其屬性已變更。</span><span class="sxs-lookup"><span data-stu-id="45722-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes have changed.</span></span> <span data-ttu-id="45722-111">如果 *lParam* 所指向之結構的 **iItem** 成員為-1，則變更已套用至清單視圖中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="45722-111">If the **iItem** member of the structure pointed to by *lParam* is -1, the change has been applied to all items in the list view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45722-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="45722-112">Return value</span></span>

<span data-ttu-id="45722-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="45722-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45722-114">備註</span><span class="sxs-lookup"><span data-stu-id="45722-114">Remarks</span></span>

<span data-ttu-id="45722-115">如果清單視圖控制項有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式，且使用者按住 SHIFT 鍵並按一下滑鼠來選取某個範圍的專案，則 \_ 不會針對每個選取或取消選取的專案傳送 LVN ITEMCHANGED 通知碼。</span><span class="sxs-lookup"><span data-stu-id="45722-115">If a list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, and the user selects a range of items by holding down the SHIFT key and clicking the mouse, LVN\_ITEMCHANGED notification codes are not sent for each selected or deselected item.</span></span> <span data-ttu-id="45722-116">相反地，您會收到單一 [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) 通知碼，指出某個範圍的專案已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="45722-116">Instead, you will receive a single [LVN\_ODSTATECHANGED](lvn-odstatechanged.md) notification code, indicating that a range of items has changed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="45722-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="45722-117">Requirements</span></span>



| <span data-ttu-id="45722-118">需求</span><span class="sxs-lookup"><span data-stu-id="45722-118">Requirement</span></span> | <span data-ttu-id="45722-119">值</span><span class="sxs-lookup"><span data-stu-id="45722-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45722-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45722-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45722-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45722-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45722-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45722-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45722-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45722-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45722-124">標頭</span><span class="sxs-lookup"><span data-stu-id="45722-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="45722-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="45722-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





