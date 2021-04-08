---
title: 'WM_EXITMENULOOP 訊息 (Winuser .h) '
description: 通知應用程式的主視窗程式，表示已結束功能表強制回應迴圈。
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685959"
---
# <a name="wm_exitmenuloop-message"></a><span data-ttu-id="344a7-104">WM \_ EXITMENULOOP 訊息</span><span class="sxs-lookup"><span data-stu-id="344a7-104">WM\_EXITMENULOOP message</span></span>

<span data-ttu-id="344a7-105">通知應用程式的主視窗程式，表示已結束功能表強制回應迴圈。</span><span class="sxs-lookup"><span data-stu-id="344a7-105">Notifies an application's main window procedure that a menu modal loop has been exited.</span></span>


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a><span data-ttu-id="344a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="344a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="344a7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="344a7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="344a7-108">指定功能表是否為快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="344a7-108">Specifies whether the menu is a shortcut menu.</span></span> <span data-ttu-id="344a7-109">如果這個參數是快捷方式功能表，則此參數的值為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="344a7-109">This parameter has a value of **TRUE** if it is a shortcut menu, **FALSE** if it is not.</span></span>

</dd> <dt>

<span data-ttu-id="344a7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="344a7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="344a7-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="344a7-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="344a7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="344a7-112">Return value</span></span>

<span data-ttu-id="344a7-113">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="344a7-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="344a7-114">備註</span><span class="sxs-lookup"><span data-stu-id="344a7-114">Remarks</span></span>

<span data-ttu-id="344a7-115">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="344a7-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="344a7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="344a7-116">Requirements</span></span>



| <span data-ttu-id="344a7-117">需求</span><span class="sxs-lookup"><span data-stu-id="344a7-117">Requirement</span></span> | <span data-ttu-id="344a7-118">值</span><span class="sxs-lookup"><span data-stu-id="344a7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="344a7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="344a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="344a7-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="344a7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="344a7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="344a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="344a7-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="344a7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="344a7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="344a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="344a7-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="344a7-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="344a7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="344a7-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="344a7-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="344a7-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="344a7-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="344a7-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="344a7-128">**WM \_ ENTERMENULOOP**</span><span class="sxs-lookup"><span data-stu-id="344a7-128">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
</dt> <dt>

<span data-ttu-id="344a7-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="344a7-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="344a7-130">功能表</span><span class="sxs-lookup"><span data-stu-id="344a7-130">Menus</span></span>](menus.md)
</dt> </dl>

 

