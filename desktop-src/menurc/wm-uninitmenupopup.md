---
title: 'WM_UNINITMENUPOPUP 訊息 (Winuser .h) '
description: 當下拉式選單或子功能表已終結時傳送。
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509460"
---
# <a name="wm_uninitmenupopup-message"></a><span data-ttu-id="c28ff-104">WM \_ UNINITMENUPOPUP 訊息</span><span class="sxs-lookup"><span data-stu-id="c28ff-104">WM\_UNINITMENUPOPUP message</span></span>

<span data-ttu-id="c28ff-105">當下拉式選單或子功能表已終結時傳送。</span><span class="sxs-lookup"><span data-stu-id="c28ff-105">Sent when a drop-down menu or submenu has been destroyed.</span></span>


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a><span data-ttu-id="c28ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="c28ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c28ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c28ff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c28ff-108">功能表的控制碼</span><span class="sxs-lookup"><span data-stu-id="c28ff-108">A handle to the menu</span></span>

</dd> <dt>

<span data-ttu-id="c28ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c28ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c28ff-110">高序位單字會識別已終結的功能表。</span><span class="sxs-lookup"><span data-stu-id="c28ff-110">The high-order word identifies the menu that was destroyed.</span></span> <span data-ttu-id="c28ff-111">目前，這個參數只能是 (視窗功能表) 的 **MF \_ SYSMENU** 。</span><span class="sxs-lookup"><span data-stu-id="c28ff-111">Currently, this parameter can only be **MF\_SYSMENU** (the window menu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c28ff-112">備註</span><span class="sxs-lookup"><span data-stu-id="c28ff-112">Remarks</span></span>

<span data-ttu-id="c28ff-113">如果應用程式收到 [**wm \_ INITMENUPOPUP**](wm-initmenupopup.md) 訊息，則會收到 **wm \_ UNINITMENUPOPUP** 訊息。</span><span class="sxs-lookup"><span data-stu-id="c28ff-113">If an application receives a [**WM\_INITMENUPOPUP**](wm-initmenupopup.md) message, it will receive a **WM\_UNINITMENUPOPUP** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c28ff-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c28ff-114">Requirements</span></span>



| <span data-ttu-id="c28ff-115">需求</span><span class="sxs-lookup"><span data-stu-id="c28ff-115">Requirement</span></span> | <span data-ttu-id="c28ff-116">值</span><span class="sxs-lookup"><span data-stu-id="c28ff-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c28ff-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c28ff-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c28ff-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c28ff-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c28ff-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c28ff-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c28ff-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c28ff-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c28ff-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c28ff-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c28ff-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c28ff-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c28ff-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c28ff-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="c28ff-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="c28ff-124">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="c28ff-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c28ff-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c28ff-126">**概念**</span><span class="sxs-lookup"><span data-stu-id="c28ff-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c28ff-127">功能表</span><span class="sxs-lookup"><span data-stu-id="c28ff-127">Menus</span></span>](menus.md)
</dt> </dl>

 

