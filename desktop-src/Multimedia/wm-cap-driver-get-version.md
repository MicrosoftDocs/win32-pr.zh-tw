---
title: 'WM_CAP_DRIVER_GET_VERSION 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式版本資訊。 您可以使用 capDriverGetVersion 宏明確地傳送此訊息。'
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970000"
---
# <a name="wm_cap_driver_get_version-message"></a><span data-ttu-id="a12fa-105">WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本訊息</span><span class="sxs-lookup"><span data-stu-id="a12fa-105">WM\_CAP\_DRIVER\_GET\_VERSION message</span></span>

<span data-ttu-id="a12fa-106">[ **WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本** ] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式版本資訊。</span><span class="sxs-lookup"><span data-stu-id="a12fa-106">The **WM\_CAP\_DRIVER\_GET\_VERSION** message returns the version information of the capture driver connected to a capture window.</span></span> <span data-ttu-id="a12fa-107">您可以使用 [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a12fa-107">You can send this message explicitly or by using the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a><span data-ttu-id="a12fa-108">參數</span><span class="sxs-lookup"><span data-stu-id="a12fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12fa-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="a12fa-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="a12fa-110">**SzVer** 所參考的應用程式定義緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a12fa-110">Size, in bytes, of the application-defined buffer referenced by **szVer**.</span></span>

</dd> <dt>

<span data-ttu-id="a12fa-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span><span class="sxs-lookup"><span data-stu-id="a12fa-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span></span>
</dt> <dd>

<span data-ttu-id="a12fa-112">應用程式定義的緩衝區指標，用來以 null 終止字串的形式傳回版本資訊。</span><span class="sxs-lookup"><span data-stu-id="a12fa-112">Pointer to an application-defined buffer used to return the version information as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a12fa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a12fa-113">Return Value</span></span>

<span data-ttu-id="a12fa-114">如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a12fa-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="a12fa-115">備註</span><span class="sxs-lookup"><span data-stu-id="a12fa-115">Remarks</span></span>

<span data-ttu-id="a12fa-116">版本資訊是取自驅動程式資源區域的文字字串。</span><span class="sxs-lookup"><span data-stu-id="a12fa-116">The version information is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="a12fa-117">應用程式應該為此字串配置大約40個位元組。</span><span class="sxs-lookup"><span data-stu-id="a12fa-117">Applications should allocate approximately 40 bytes for this string.</span></span> <span data-ttu-id="a12fa-118">如果版本資訊無法使用，則會傳回 **Null** 字串。</span><span class="sxs-lookup"><span data-stu-id="a12fa-118">If version information is not available, a **NULL** string is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a12fa-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a12fa-119">Requirements</span></span>



| <span data-ttu-id="a12fa-120">需求</span><span class="sxs-lookup"><span data-stu-id="a12fa-120">Requirement</span></span> | <span data-ttu-id="a12fa-121">值</span><span class="sxs-lookup"><span data-stu-id="a12fa-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a12fa-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a12fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a12fa-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a12fa-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a12fa-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a12fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a12fa-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a12fa-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a12fa-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a12fa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a12fa-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="a12fa-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a12fa-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a12fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12fa-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="a12fa-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="a12fa-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="a12fa-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





