---
title: 'WM_MENUDRAG 訊息 (Winuser .h) '
description: 當使用者拖曳功能表項目時，傳送至拖放功能表的擁有者。
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969826"
---
# <a name="wm_menudrag-message"></a><span data-ttu-id="ac672-104">WM \_ MENUDRAG 訊息</span><span class="sxs-lookup"><span data-stu-id="ac672-104">WM\_MENUDRAG message</span></span>

<span data-ttu-id="ac672-105">當使用者拖曳功能表項目時，傳送至拖放功能表的擁有者。</span><span class="sxs-lookup"><span data-stu-id="ac672-105">Sent to the owner of a drag-and-drop menu when the user drags a menu item.</span></span>


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a><span data-ttu-id="ac672-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac672-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac672-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac672-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac672-108">拖曳作業開始的專案位置。</span><span class="sxs-lookup"><span data-stu-id="ac672-108">The position of the item where the drag operation began.</span></span>

</dd> <dt>

<span data-ttu-id="ac672-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac672-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac672-110">包含專案之功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ac672-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac672-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac672-111">Return value</span></span>

<span data-ttu-id="ac672-112">應用程式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ac672-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="ac672-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ac672-113">Return code/value</span></span>                                                                                                                                   | <span data-ttu-id="ac672-114">Description</span><span class="sxs-lookup"><span data-stu-id="ac672-114">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac672-115"><dt>**MND \_繼續**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ac672-115"><dt>**MND\_CONTINUE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="ac672-116">功能表應維持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="ac672-116">Menu should remain active.</span></span> <span data-ttu-id="ac672-117">如果放開滑鼠，則應該予以忽略。</span><span class="sxs-lookup"><span data-stu-id="ac672-117">If the mouse is released, it should be ignored.</span></span><br/> |
| <dl> <span data-ttu-id="ac672-118"><dt>**MND \_ENDMENU**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ac672-118"><dt>**MND\_ENDMENU**</dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="ac672-119">應結束功能表。</span><span class="sxs-lookup"><span data-stu-id="ac672-119">Menu should be ended.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ac672-120">備註</span><span class="sxs-lookup"><span data-stu-id="ac672-120">Remarks</span></span>

<span data-ttu-id="ac672-121">應用程式可以呼叫 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 函式來回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="ac672-121">The application can call the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function in response to this message.</span></span>

<span data-ttu-id="ac672-122">若要建立拖放功能表，請使用 **MNS \_ System.windows.dragdrop.drop>** 呼叫 [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) 。</span><span class="sxs-lookup"><span data-stu-id="ac672-122">To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac672-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac672-123">Requirements</span></span>



| <span data-ttu-id="ac672-124">需求</span><span class="sxs-lookup"><span data-stu-id="ac672-124">Requirement</span></span> | <span data-ttu-id="ac672-125">值</span><span class="sxs-lookup"><span data-stu-id="ac672-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac672-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac672-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac672-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac672-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ac672-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac672-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac672-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac672-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac672-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ac672-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac672-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ac672-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac672-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac672-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac672-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="ac672-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ac672-134">**SetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="ac672-134">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

<span data-ttu-id="ac672-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="ac672-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ac672-136">功能表</span><span class="sxs-lookup"><span data-stu-id="ac672-136">Menus</span></span>](menus.md)
</dt> </dl>

 

