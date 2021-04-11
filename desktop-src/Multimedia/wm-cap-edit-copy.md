---
title: 'WM_CAP_EDIT_COPY 訊息 (Vfw .h) '
description: WM \_ CAP \_ 編輯 \_ 複製訊息會將影片框架緩衝區和相關聯的調色板內容複寫到剪貼簿。 您可以使用 capEditCopy 宏明確地傳送此訊息。
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104700"
---
# <a name="wm_cap_edit_copy-message"></a><span data-ttu-id="d72d0-105">WM \_ CAP \_ 編輯 \_ 複製訊息</span><span class="sxs-lookup"><span data-stu-id="d72d0-105">WM\_CAP\_EDIT\_COPY message</span></span>

<span data-ttu-id="d72d0-106">**WM \_ CAP \_ 編輯 \_ 複製** 訊息會將影片框架緩衝區和相關聯的調色板內容複寫到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="d72d0-106">The **WM\_CAP\_EDIT\_COPY** message copies the contents of the video frame buffer and associated palette to the clipboard.</span></span> <span data-ttu-id="d72d0-107">您可以使用 [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d72d0-107">You can send this message explicitly or by using the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro.</span></span>


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="d72d0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d72d0-108">Return Value</span></span>

<span data-ttu-id="d72d0-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d72d0-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d72d0-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d72d0-110">Requirements</span></span>



| <span data-ttu-id="d72d0-111">需求</span><span class="sxs-lookup"><span data-stu-id="d72d0-111">Requirement</span></span> | <span data-ttu-id="d72d0-112">值</span><span class="sxs-lookup"><span data-stu-id="d72d0-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d72d0-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d72d0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d72d0-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d72d0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d72d0-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d72d0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d72d0-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d72d0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d72d0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d72d0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d72d0-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="d72d0-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d72d0-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d72d0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d72d0-120">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="d72d0-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d72d0-121">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="d72d0-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





