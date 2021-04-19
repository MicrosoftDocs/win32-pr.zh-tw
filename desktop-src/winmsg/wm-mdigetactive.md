---
description: 應用程式會將 WM \_ MDIGETACTIVE 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以抓取作用中 MDI 子視窗的控制碼。
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: 'WM_MDIGETACTIVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979923"
---
# <a name="wm_mdigetactive-message"></a><span data-ttu-id="834b8-103">WM \_ MDIGETACTIVE 訊息</span><span class="sxs-lookup"><span data-stu-id="834b8-103">WM\_MDIGETACTIVE message</span></span>

<span data-ttu-id="834b8-104">應用程式會將 **WM \_ MDIGETACTIVE** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以抓取作用中 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="834b8-104">An application sends the **WM\_MDIGETACTIVE** message to a multiple-document interface (MDI) client window to retrieve the handle to the active MDI child window.</span></span>


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a><span data-ttu-id="834b8-105">參數</span><span class="sxs-lookup"><span data-stu-id="834b8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834b8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="834b8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="834b8-107">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="834b8-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="834b8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="834b8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="834b8-109">最大化的狀態。</span><span class="sxs-lookup"><span data-stu-id="834b8-109">The maximized state.</span></span> <span data-ttu-id="834b8-110">如果這個參數不是 **Null**，它就是值的指標，指出 MDI 子視窗最大化的狀態。</span><span class="sxs-lookup"><span data-stu-id="834b8-110">If this parameter is not **NULL**, it is a pointer to a value that indicates the maximized state of the MDI child window.</span></span> <span data-ttu-id="834b8-111">如果值為 **TRUE**，則會將視窗最大化; **FALSE** 值表示它不是。</span><span class="sxs-lookup"><span data-stu-id="834b8-111">If the value is **TRUE**, the window is maximized; a value of **FALSE** indicates that it is not.</span></span> <span data-ttu-id="834b8-112">如果此參數為 **Null**，則會忽略參數。</span><span class="sxs-lookup"><span data-stu-id="834b8-112">If this parameter is **NULL**, the parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="834b8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="834b8-113">Return value</span></span>

<span data-ttu-id="834b8-114">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="834b8-114">Type: **HWND**</span></span>

<span data-ttu-id="834b8-115">傳回值是現用 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="834b8-115">The return value is the handle to the active MDI child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="834b8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="834b8-116">Requirements</span></span>



| <span data-ttu-id="834b8-117">需求</span><span class="sxs-lookup"><span data-stu-id="834b8-117">Requirement</span></span> | <span data-ttu-id="834b8-118">值</span><span class="sxs-lookup"><span data-stu-id="834b8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="834b8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="834b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="834b8-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="834b8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="834b8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="834b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="834b8-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="834b8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="834b8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="834b8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="834b8-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="834b8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="834b8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="834b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834b8-126">多重文件介面總覽</span><span class="sxs-lookup"><span data-stu-id="834b8-126">Multiple Document Interface Overview</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




