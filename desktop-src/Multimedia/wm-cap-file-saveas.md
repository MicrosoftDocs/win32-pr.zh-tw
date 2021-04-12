---
title: 'WM_CAP_FILE_SAVEAS 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ 的 \_ SAVEAS 訊息會將 capture 檔案的內容複寫到另一個檔案。 您可以使用 capFileSaveAs 宏明確地傳送此訊息。
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384258"
---
# <a name="wm_cap_file_saveas-message"></a><span data-ttu-id="05bb1-105">WM \_ CAP \_ FILE \_ SAVEAS 訊息</span><span class="sxs-lookup"><span data-stu-id="05bb1-105">WM\_CAP\_FILE\_SAVEAS message</span></span>

<span data-ttu-id="05bb1-106">**WM CAP 檔案的 \_ \_ \_ SAVEAS** 訊息會將 capture 檔案的內容複寫到另一個檔案。</span><span class="sxs-lookup"><span data-stu-id="05bb1-106">The **WM\_CAP\_FILE\_SAVEAS** message copies the contents of the capture file to another file.</span></span> <span data-ttu-id="05bb1-107">您可以使用 [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="05bb1-107">You can send this message explicitly or by using the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro.</span></span>


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="05bb1-108">參數</span><span class="sxs-lookup"><span data-stu-id="05bb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05bb1-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="05bb1-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="05bb1-110">以 null 結束的字串指標，其中包含用來複製檔案的目的地檔案名。</span><span class="sxs-lookup"><span data-stu-id="05bb1-110">Pointer to the null-terminated string that contains the name of the destination file used to copy the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05bb1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="05bb1-111">Return Value</span></span>

<span data-ttu-id="05bb1-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="05bb1-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="05bb1-113">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="05bb1-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="05bb1-114">備註</span><span class="sxs-lookup"><span data-stu-id="05bb1-114">Remarks</span></span>

<span data-ttu-id="05bb1-115">此訊息不會變更目前 capture 檔案的名稱或內容。</span><span class="sxs-lookup"><span data-stu-id="05bb1-115">This message does not change the name or contents of the current capture file.</span></span>

<span data-ttu-id="05bb1-116">如果複製作業因為磁片已滿錯誤而失敗，則會自動刪除目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="05bb1-116">If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.</span></span>

<span data-ttu-id="05bb1-117">通常會針對預期的最大 capture 區段預先配置 capture 檔案，而且只會使用其中一部分來捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="05bb1-117">Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="05bb1-118">此訊息只會複製包含 capture 資料之檔案的部分。</span><span class="sxs-lookup"><span data-stu-id="05bb1-118">This message copies only the portion of the file containing the capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="05bb1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="05bb1-119">Requirements</span></span>



| <span data-ttu-id="05bb1-120">需求</span><span class="sxs-lookup"><span data-stu-id="05bb1-120">Requirement</span></span> | <span data-ttu-id="05bb1-121">值</span><span class="sxs-lookup"><span data-stu-id="05bb1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="05bb1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05bb1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05bb1-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05bb1-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="05bb1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05bb1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05bb1-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05bb1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05bb1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="05bb1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="05bb1-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="05bb1-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05bb1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05bb1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05bb1-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="05bb1-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="05bb1-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="05bb1-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





