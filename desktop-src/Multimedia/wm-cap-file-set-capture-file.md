---
title: 'WM_CAP_FILE_SET_CAPTURE_FILE 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file] 訊息會將用於影片捕獲的檔案命名為。 您可以使用 capFileSetCaptureFile 宏明確地傳送此訊息。'
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933894"
---
# <a name="wm_cap_file_set_capture_file-message"></a><span data-ttu-id="3e8a5-105">WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file 訊息</span><span class="sxs-lookup"><span data-stu-id="3e8a5-105">WM\_CAP\_FILE\_SET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="3e8a5-106">[ **WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file** ] 訊息會將用於影片捕獲的檔案命名為。</span><span class="sxs-lookup"><span data-stu-id="3e8a5-106">The **WM\_CAP\_FILE\_SET\_CAPTURE\_FILE** message names the file used for video capture.</span></span> <span data-ttu-id="3e8a5-107">您可以使用 [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3e8a5-107">You can send this message explicitly or by using the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="3e8a5-108">參數</span><span class="sxs-lookup"><span data-stu-id="3e8a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8a5-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="3e8a5-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="3e8a5-110">以 null 結束的字串指標，其中包含要使用的捕獲檔案名。</span><span class="sxs-lookup"><span data-stu-id="3e8a5-110">Pointer to the null-terminated string that contains the name of the capture file to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8a5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e8a5-111">Return Value</span></span>

<span data-ttu-id="3e8a5-112">如果成功，則傳回 **TRUE** ; 如果檔案名無效，或如果正在進行資料流程或單一框架捕獲，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3e8a5-112">Returns **TRUE** if successful or **FALSE** if the filename is invalid, or if streaming or single-frame capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e8a5-113">備註</span><span class="sxs-lookup"><span data-stu-id="3e8a5-113">Remarks</span></span>

<span data-ttu-id="3e8a5-114">此訊息會將檔案名儲存在內部結構中。</span><span class="sxs-lookup"><span data-stu-id="3e8a5-114">This message stores the filename in an internal structure.</span></span> <span data-ttu-id="3e8a5-115">它不會建立、配置或開啟指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="3e8a5-115">It does not create, allocate, or open the specified file.</span></span> <span data-ttu-id="3e8a5-116">預設的捕獲檔案名為 C： \\CAPTURE.AVI。</span><span class="sxs-lookup"><span data-stu-id="3e8a5-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8a5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e8a5-117">Requirements</span></span>



| <span data-ttu-id="3e8a5-118">需求</span><span class="sxs-lookup"><span data-stu-id="3e8a5-118">Requirement</span></span> | <span data-ttu-id="3e8a5-119">值</span><span class="sxs-lookup"><span data-stu-id="3e8a5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e8a5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e8a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8a5-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e8a5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3e8a5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e8a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8a5-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e8a5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3e8a5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3e8a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e8a5-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e8a5-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8a5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e8a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8a5-127">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="3e8a5-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3e8a5-128">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="3e8a5-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





