---
description: 應用程式會將 WM \_ MDIRESTORE 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以從最大化或最小化的大小還原 mdi 子視窗。
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: 'WM_MDIRESTORE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973829"
---
# <a name="wm_mdirestore-message"></a><span data-ttu-id="9f058-103">WM \_ MDIRESTORE 訊息</span><span class="sxs-lookup"><span data-stu-id="9f058-103">WM\_MDIRESTORE message</span></span>

<span data-ttu-id="9f058-104">應用程式會將 **WM \_ MDIRESTORE** 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以從最大化或最小化的大小還原 mdi 子視窗。</span><span class="sxs-lookup"><span data-stu-id="9f058-104">An application sends the **WM\_MDIRESTORE** message to a multiple-document interface (MDI) client window to restore an MDI child window from maximized or minimized size.</span></span>


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a><span data-ttu-id="9f058-105">參數</span><span class="sxs-lookup"><span data-stu-id="9f058-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f058-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f058-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f058-107">要還原的 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9f058-107">A handle to the MDI child window to be restored.</span></span>

</dd> <dt>

<span data-ttu-id="9f058-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f058-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f058-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="9f058-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f058-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f058-110">Return value</span></span>

<span data-ttu-id="9f058-111">類型： **零**</span><span class="sxs-lookup"><span data-stu-id="9f058-111">Type: **zero**</span></span>

<span data-ttu-id="9f058-112">傳回值永遠是零。</span><span class="sxs-lookup"><span data-stu-id="9f058-112">The return value is always zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f058-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f058-113">Requirements</span></span>



| <span data-ttu-id="9f058-114">需求</span><span class="sxs-lookup"><span data-stu-id="9f058-114">Requirement</span></span> | <span data-ttu-id="9f058-115">值</span><span class="sxs-lookup"><span data-stu-id="9f058-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f058-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f058-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f058-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f058-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9f058-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f058-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f058-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f058-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f058-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9f058-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f058-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9f058-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f058-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f058-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f058-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="9f058-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f058-124">**WM \_ MDIMAXIMIZE**</span><span class="sxs-lookup"><span data-stu-id="9f058-124">**WM\_MDIMAXIMIZE**</span></span>](wm-mdimaximize.md)
</dt> <dt>

<span data-ttu-id="9f058-125">**概念**</span><span class="sxs-lookup"><span data-stu-id="9f058-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9f058-126">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="9f058-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




