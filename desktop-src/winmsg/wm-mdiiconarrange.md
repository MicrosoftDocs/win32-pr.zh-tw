---
description: 應用程式會將 WM \_ MDIICONARRANGE 訊息傳送至多重文件介面， (mdi) 用戶端視窗來排列所有最小化的 mdi 子視窗。 它不會影響未最小化的子視窗。
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: 'WM_MDIICONARRANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468964"
---
# <a name="wm_mdiiconarrange-message"></a><span data-ttu-id="f2d14-104">WM \_ MDIICONARRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="f2d14-104">WM\_MDIICONARRANGE message</span></span>

<span data-ttu-id="f2d14-105">應用程式會將 **WM \_ MDIICONARRANGE** 訊息傳送至多重文件介面， (mdi) 用戶端視窗來排列所有最小化的 mdi 子視窗。</span><span class="sxs-lookup"><span data-stu-id="f2d14-105">An application sends the **WM\_MDIICONARRANGE** message to a multiple-document interface (MDI) client window to arrange all minimized MDI child windows.</span></span> <span data-ttu-id="f2d14-106">它不會影響未最小化的子視窗。</span><span class="sxs-lookup"><span data-stu-id="f2d14-106">It does not affect child windows that are not minimized.</span></span>


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a><span data-ttu-id="f2d14-107">參數</span><span class="sxs-lookup"><span data-stu-id="f2d14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d14-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2d14-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d14-109">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="f2d14-109">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f2d14-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2d14-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d14-111">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="f2d14-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2d14-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2d14-112">Requirements</span></span>



| <span data-ttu-id="f2d14-113">需求</span><span class="sxs-lookup"><span data-stu-id="f2d14-113">Requirement</span></span> | <span data-ttu-id="f2d14-114">值</span><span class="sxs-lookup"><span data-stu-id="f2d14-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d14-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2d14-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d14-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2d14-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2d14-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2d14-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d14-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2d14-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2d14-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f2d14-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d14-120"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f2d14-120"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d14-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2d14-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2d14-122">**參考**</span><span class="sxs-lookup"><span data-stu-id="f2d14-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2d14-123">**WM \_ MDICASCADE**</span><span class="sxs-lookup"><span data-stu-id="f2d14-123">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="f2d14-124">**WM \_ MDITILE**</span><span class="sxs-lookup"><span data-stu-id="f2d14-124">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="f2d14-125">**概念**</span><span class="sxs-lookup"><span data-stu-id="f2d14-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2d14-126">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="f2d14-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




