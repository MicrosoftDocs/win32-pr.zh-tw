---
title: 'WM_MENURBUTTONUP 訊息 (Winuser .h) '
description: 當使用者放開滑鼠右鍵，而游標位於功能表項目上時傳送。
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317516"
---
# <a name="wm_menurbuttonup-message"></a><span data-ttu-id="a8705-104">WM \_ MENURBUTTONUP 訊息</span><span class="sxs-lookup"><span data-stu-id="a8705-104">WM\_MENURBUTTONUP message</span></span>

<span data-ttu-id="a8705-105">當使用者放開滑鼠右鍵，而游標位於功能表項目上時傳送。</span><span class="sxs-lookup"><span data-stu-id="a8705-105">Sent when the user releases the right mouse button while the cursor is on a menu item.</span></span>


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a><span data-ttu-id="a8705-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8705-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8705-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8705-108">功能表項目以零為起始的索引，也就是用來釋放滑鼠右鍵的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="a8705-108">The zero-based index of the menu item on which the right mouse button was released.</span></span>

</dd> <dt>

<span data-ttu-id="a8705-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8705-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8705-110">包含專案之功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8705-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8705-111">備註</span><span class="sxs-lookup"><span data-stu-id="a8705-111">Remarks</span></span>

<span data-ttu-id="a8705-112">**WM \_ MENURBUTTONUP** 訊息可讓應用程式提供內容相關功能表，也稱為此訊息中指定之功能表項目的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="a8705-112">The **WM\_MENURBUTTONUP** message allows applications to provide a context-sensitive menu also known as a shortcut menu for the menu item specified in this message.</span></span> <span data-ttu-id="a8705-113">若要顯示功能表項目的內容相關功能表，請使用 **TPM \_ 遞迴** 呼叫 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)函數。</span><span class="sxs-lookup"><span data-stu-id="a8705-113">To display a context-sensitive menu for a menu item, call the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function with **TPM\_RECURSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8705-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8705-114">Requirements</span></span>



| <span data-ttu-id="a8705-115">需求</span><span class="sxs-lookup"><span data-stu-id="a8705-115">Requirement</span></span> | <span data-ttu-id="a8705-116">值</span><span class="sxs-lookup"><span data-stu-id="a8705-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8705-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8705-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8705-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8705-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a8705-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8705-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8705-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8705-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8705-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a8705-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8705-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a8705-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8705-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8705-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8705-124">功能表總覽</span><span class="sxs-lookup"><span data-stu-id="a8705-124">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





