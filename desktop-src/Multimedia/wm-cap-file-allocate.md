---
title: 'WM_CAP_FILE_ALLOCATE 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ \_ 配置訊息會建立 (會預先配置) 指定大小的捕捉檔。 您可以使用 capFileAlloc 宏明確地傳送此訊息。
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464733"
---
# <a name="wm_cap_file_allocate-message"></a><span data-ttu-id="66114-105">WM \_ CAP \_ FILE \_ 配置訊息</span><span class="sxs-lookup"><span data-stu-id="66114-105">WM\_CAP\_FILE\_ALLOCATE message</span></span>

<span data-ttu-id="66114-106">**WM \_ CAP 檔案 \_ \_ 配置** 訊息會建立 (會預先配置) 指定大小的捕捉檔。</span><span class="sxs-lookup"><span data-stu-id="66114-106">The **WM\_CAP\_FILE\_ALLOCATE** message creates (preallocates) a capture file of a specified size.</span></span> <span data-ttu-id="66114-107">您可以使用 [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="66114-107">You can send this message explicitly or by using the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro.</span></span>


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a><span data-ttu-id="66114-108">參數</span><span class="sxs-lookup"><span data-stu-id="66114-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66114-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span><span class="sxs-lookup"><span data-stu-id="66114-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span></span>
</dt> <dd>

<span data-ttu-id="66114-110">建立 capture 檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="66114-110">Size, in bytes, to create the capture file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66114-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="66114-111">Return Value</span></span>

<span data-ttu-id="66114-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="66114-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="66114-113">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="66114-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="66114-114">備註</span><span class="sxs-lookup"><span data-stu-id="66114-114">Remarks</span></span>

<span data-ttu-id="66114-115">您可以藉由預先配置夠大的捕獲檔案來儲存整個影片剪輯，以及在捕獲剪輯之前重組 capture 檔案，以大幅改善串流捕獲效能。</span><span class="sxs-lookup"><span data-stu-id="66114-115">You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="66114-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="66114-116">Requirements</span></span>



| <span data-ttu-id="66114-117">需求</span><span class="sxs-lookup"><span data-stu-id="66114-117">Requirement</span></span> | <span data-ttu-id="66114-118">值</span><span class="sxs-lookup"><span data-stu-id="66114-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="66114-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66114-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66114-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66114-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="66114-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66114-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66114-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66114-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66114-123">標頭</span><span class="sxs-lookup"><span data-stu-id="66114-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66114-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="66114-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66114-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66114-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66114-126">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="66114-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="66114-127">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="66114-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





