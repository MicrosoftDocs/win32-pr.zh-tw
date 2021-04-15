---
title: 'WM_CAP_FILE_SAVEDIB 訊息 (Vfw .h) '
description: WM \_ CAP \_ file \_ SAVEDIB 訊息會將目前的畫面格複製到 DIB 檔案。 您可以使用 capFileSaveDIB 宏明確地傳送此訊息。
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466869"
---
# <a name="wm_cap_file_savedib-message"></a><span data-ttu-id="aca7f-105">WM \_ CAP \_ FILE \_ SAVEDIB 訊息</span><span class="sxs-lookup"><span data-stu-id="aca7f-105">WM\_CAP\_FILE\_SAVEDIB message</span></span>

<span data-ttu-id="aca7f-106">**WM \_ CAP \_ file \_ SAVEDIB** 訊息會將目前的畫面格複製到 DIB 檔案。</span><span class="sxs-lookup"><span data-stu-id="aca7f-106">The **WM\_CAP\_FILE\_SAVEDIB** message copies the current frame to a DIB file.</span></span> <span data-ttu-id="aca7f-107">您可以使用 [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="aca7f-107">You can send this message explicitly or by using the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro.</span></span>


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="aca7f-108">參數</span><span class="sxs-lookup"><span data-stu-id="aca7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca7f-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="aca7f-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="aca7f-110">以 null 結束的字串指標，其中包含目的地 DIB 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="aca7f-110">Pointer to the null-terminated string that contains the name of the destination DIB file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aca7f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aca7f-111">Return Value</span></span>

<span data-ttu-id="aca7f-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="aca7f-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="aca7f-113">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="aca7f-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="aca7f-114">備註</span><span class="sxs-lookup"><span data-stu-id="aca7f-114">Remarks</span></span>

<span data-ttu-id="aca7f-115">如果捕捉驅動程式提供壓縮格式的框架，此呼叫會先嘗試解壓縮框架再寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="aca7f-115">If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca7f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="aca7f-116">Requirements</span></span>



| <span data-ttu-id="aca7f-117">需求</span><span class="sxs-lookup"><span data-stu-id="aca7f-117">Requirement</span></span> | <span data-ttu-id="aca7f-118">值</span><span class="sxs-lookup"><span data-stu-id="aca7f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aca7f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aca7f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aca7f-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aca7f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aca7f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aca7f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aca7f-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aca7f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aca7f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="aca7f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca7f-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="aca7f-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aca7f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aca7f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca7f-126">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="aca7f-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="aca7f-127">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="aca7f-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





