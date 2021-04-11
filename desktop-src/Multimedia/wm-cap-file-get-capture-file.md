---
title: 'WM_CAP_FILE_GET_CAPTURE_FILE 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ 取得捕獲檔案訊息會傳回 \_ 目前 CAPTURE 檔案的 \_ \_ 名稱。 您可以使用 capFileGetCaptureFile 宏明確地傳送此訊息。
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843187"
---
# <a name="wm_cap_file_get_capture_file-message"></a><span data-ttu-id="bef6a-105">WM \_ CAP \_ 檔案 \_ 取得 \_ 捕獲檔案 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="bef6a-105">WM\_CAP\_FILE\_GET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="bef6a-106">**WM \_ CAP 檔案 \_ \_ 取得 \_ 捕獲 \_** 檔案訊息會傳回目前 CAPTURE 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="bef6a-106">The **WM\_CAP\_FILE\_GET\_CAPTURE\_FILE** message returns the name of the current capture file.</span></span> <span data-ttu-id="bef6a-107">您可以使用 [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="bef6a-107">You can send this message explicitly or by using the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="bef6a-108">參數</span><span class="sxs-lookup"><span data-stu-id="bef6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bef6a-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="bef6a-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="bef6a-110">**>szname** 所參考的應用程式定義緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bef6a-110">Size, in bytes, of the application-defined buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="bef6a-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="bef6a-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="bef6a-112">應用程式定義的緩衝區指標，用來將捕獲檔案的名稱當做以 null 終止的字串傳回。</span><span class="sxs-lookup"><span data-stu-id="bef6a-112">Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bef6a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bef6a-113">Return Value</span></span>

<span data-ttu-id="bef6a-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bef6a-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bef6a-115">備註</span><span class="sxs-lookup"><span data-stu-id="bef6a-115">Remarks</span></span>

<span data-ttu-id="bef6a-116">預設的捕獲檔案名為 C： \\CAPTURE.AVI。</span><span class="sxs-lookup"><span data-stu-id="bef6a-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="bef6a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bef6a-117">Requirements</span></span>



| <span data-ttu-id="bef6a-118">需求</span><span class="sxs-lookup"><span data-stu-id="bef6a-118">Requirement</span></span> | <span data-ttu-id="bef6a-119">值</span><span class="sxs-lookup"><span data-stu-id="bef6a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bef6a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bef6a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bef6a-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bef6a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bef6a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bef6a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bef6a-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bef6a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bef6a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bef6a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bef6a-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="bef6a-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef6a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bef6a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef6a-127">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="bef6a-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bef6a-128">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="bef6a-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





