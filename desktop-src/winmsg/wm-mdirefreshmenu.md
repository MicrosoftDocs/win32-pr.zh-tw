---
description: 應用程式會將 WM \_ MDIREFRESHMENU 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以重新整理 mdi 框架視窗的 [視窗] 功能表。
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: 'WM_MDIREFRESHMENU 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976913"
---
# <a name="wm_mdirefreshmenu-message"></a><span data-ttu-id="ef37d-103">WM \_ MDIREFRESHMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="ef37d-103">WM\_MDIREFRESHMENU message</span></span>

<span data-ttu-id="ef37d-104">應用程式會將 **WM \_ MDIREFRESHMENU** 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以重新整理 mdi 框架視窗的 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="ef37d-104">An application sends the **WM\_MDIREFRESHMENU** message to a multiple-document interface (MDI) client window to refresh the window menu of the MDI frame window.</span></span>


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a><span data-ttu-id="ef37d-105">參數</span><span class="sxs-lookup"><span data-stu-id="ef37d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef37d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef37d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef37d-107">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="ef37d-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ef37d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef37d-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef37d-109">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="ef37d-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef37d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef37d-110">Return value</span></span>

<span data-ttu-id="ef37d-111">類型： **HMENU**</span><span class="sxs-lookup"><span data-stu-id="ef37d-111">Type: **HMENU**</span></span>

<span data-ttu-id="ef37d-112">如果訊息成功，則傳回值是框架視窗功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ef37d-112">If the message succeeds, the return value is the handle to the frame window menu.</span></span>

<span data-ttu-id="ef37d-113">如果訊息失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ef37d-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef37d-114">備註</span><span class="sxs-lookup"><span data-stu-id="ef37d-114">Remarks</span></span>

<span data-ttu-id="ef37d-115">傳送此訊息之後，應用程式必須呼叫 [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) 函式來更新功能表列。</span><span class="sxs-lookup"><span data-stu-id="ef37d-115">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef37d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef37d-116">Requirements</span></span>



| <span data-ttu-id="ef37d-117">需求</span><span class="sxs-lookup"><span data-stu-id="ef37d-117">Requirement</span></span> | <span data-ttu-id="ef37d-118">值</span><span class="sxs-lookup"><span data-stu-id="ef37d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef37d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef37d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef37d-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef37d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ef37d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef37d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef37d-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef37d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ef37d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ef37d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef37d-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ef37d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef37d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef37d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef37d-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="ef37d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ef37d-127">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="ef37d-127">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="ef37d-128">**WM \_ MDISETMENU**</span><span class="sxs-lookup"><span data-stu-id="ef37d-128">**WM\_MDISETMENU**</span></span>](wm-mdisetmenu.md)
</dt> <dt>

<span data-ttu-id="ef37d-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="ef37d-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ef37d-130">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="ef37d-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
