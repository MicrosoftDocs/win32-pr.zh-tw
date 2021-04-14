---
title: 'WM_MENUCOMMAND 訊息 (Winuser .h) '
description: 當使用者從功能表進行選取時傳送。
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385278"
---
# <a name="wm_menucommand-message"></a><span data-ttu-id="0c926-104">WM \_ MENUCOMMAND 訊息</span><span class="sxs-lookup"><span data-stu-id="0c926-104">WM\_MENUCOMMAND message</span></span>

<span data-ttu-id="0c926-105">當使用者從功能表進行選取時傳送。</span><span class="sxs-lookup"><span data-stu-id="0c926-105">Sent when the user makes a selection from a menu.</span></span>


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a><span data-ttu-id="0c926-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c926-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c926-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c926-108">所選取專案之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="0c926-108">The zero-based index of the item selected.</span></span>

</dd> <dt>

<span data-ttu-id="0c926-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c926-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c926-110">已選取專案之功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0c926-110">A handle to the menu for the item selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c926-111">備註</span><span class="sxs-lookup"><span data-stu-id="0c926-111">Remarks</span></span>

<span data-ttu-id="0c926-112">**WM \_ MENUCOMMAND** 訊息會提供您功能表的控制碼，讓您可以存取 [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)結構中的功能表資料，也會提供所選取專案的索引，這通常是應用程式所需的專案。</span><span class="sxs-lookup"><span data-stu-id="0c926-112">The **WM\_MENUCOMMAND** message gives you a handle to the menu so you can access the menu data in the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure and also gives you the index of the selected item, which is typically what applications need.</span></span> <span data-ttu-id="0c926-113">相反地， [**WM \_ 命令**](wm-command.md) 訊息會提供您功能表項目識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c926-113">In contrast, the [**WM\_COMMAND**](wm-command.md) message gives you the menu item identifier.</span></span>

<span data-ttu-id="0c926-114">只有在 [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)結構的 **dwStyle** 成員中設定的 **MNS \_ NOTIFYBYPOS** 旗標所定義的功能表上，才會傳送 **WM \_ MENUCOMMAND** 訊息。</span><span class="sxs-lookup"><span data-stu-id="0c926-114">The **WM\_MENUCOMMAND** message is sent only for menus that are defined with the **MNS\_NOTIFYBYPOS** flag set in the **dwStyle** member of the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c926-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c926-115">Requirements</span></span>



| <span data-ttu-id="0c926-116">需求</span><span class="sxs-lookup"><span data-stu-id="0c926-116">Requirement</span></span> | <span data-ttu-id="0c926-117">值</span><span class="sxs-lookup"><span data-stu-id="0c926-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c926-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c926-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0c926-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c926-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0c926-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c926-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0c926-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c926-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c926-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0c926-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c926-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0c926-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c926-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c926-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c926-125">功能表總覽</span><span class="sxs-lookup"><span data-stu-id="0c926-125">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





