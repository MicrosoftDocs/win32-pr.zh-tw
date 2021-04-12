---
title: 'WM_MENUGETOBJECT 訊息 (Winuser .h) '
description: 當滑鼠游標進入功能表項目，或從專案的中央移至專案的頂端或底部時，傳送至拖放功能表的擁有者。
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509463"
---
# <a name="wm_menugetobject-message"></a><span data-ttu-id="a553a-104">WM \_ MENUGETOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="a553a-104">WM\_MENUGETOBJECT message</span></span>

<span data-ttu-id="a553a-105">當滑鼠游標進入功能表項目，或從專案的中央移至專案的頂端或底部時，傳送至拖放功能表的擁有者。</span><span class="sxs-lookup"><span data-stu-id="a553a-105">Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.</span></span>


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a><span data-ttu-id="a553a-106">參數</span><span class="sxs-lookup"><span data-stu-id="a553a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a553a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a553a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a553a-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="a553a-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a553a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a553a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a553a-110">[**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a553a-110">A pointer to a [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a553a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a553a-111">Return value</span></span>

<span data-ttu-id="a553a-112">應用程式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a553a-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="a553a-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="a553a-113">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="a553a-114">Description</span><span class="sxs-lookup"><span data-stu-id="a553a-114">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a553a-115"><dt>**MNGO \_>AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a553a-115"><dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt></span></span> </dl>     | <span data-ttu-id="a553a-116">在 [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)的 **pvObj** 成員中傳回介面指標</span><span class="sxs-lookup"><span data-stu-id="a553a-116">An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span></span><br/> |
| <dl> <span data-ttu-id="a553a-117"><dt>**MNGO \_NOINTERFACE**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="a553a-117"><dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="a553a-118">不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="a553a-118">The interface is not supported.</span></span><br/>                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="a553a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a553a-119">Requirements</span></span>



| <span data-ttu-id="a553a-120">需求</span><span class="sxs-lookup"><span data-stu-id="a553a-120">Requirement</span></span> | <span data-ttu-id="a553a-121">值</span><span class="sxs-lookup"><span data-stu-id="a553a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a553a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a553a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a553a-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a553a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a553a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a553a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a553a-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a553a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a553a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a553a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a553a-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a553a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a553a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a553a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a553a-129">功能表總覽</span><span class="sxs-lookup"><span data-stu-id="a553a-129">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





