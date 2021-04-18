---
title: 'WM_CAP_DRIVER_GET_NAME 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式名稱。 您可以使用 capDriverGetName 宏明確地傳送此訊息。'
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464736"
---
# <a name="wm_cap_driver_get_name-message"></a><span data-ttu-id="e88c9-105">WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱訊息</span><span class="sxs-lookup"><span data-stu-id="e88c9-105">WM\_CAP\_DRIVER\_GET\_NAME message</span></span>

<span data-ttu-id="e88c9-106">[ **WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱** ] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e88c9-106">The **WM\_CAP\_DRIVER\_GET\_NAME** message returns the name of the capture driver connected to the capture window.</span></span> <span data-ttu-id="e88c9-107">您可以使用 [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e88c9-107">You can send this message explicitly or by using the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="e88c9-108">參數</span><span class="sxs-lookup"><span data-stu-id="e88c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e88c9-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="e88c9-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="e88c9-110">**>szname** 所參考的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e88c9-110">Size, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="e88c9-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="e88c9-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="e88c9-112">應用程式定義的緩衝區指標，用來將裝置名稱傳回為以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="e88c9-112">Pointer to an application-defined buffer used to return the device name as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e88c9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e88c9-113">Return Value</span></span>

<span data-ttu-id="e88c9-114">如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e88c9-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="e88c9-115">備註</span><span class="sxs-lookup"><span data-stu-id="e88c9-115">Remarks</span></span>

<span data-ttu-id="e88c9-116">名稱是取自驅動程式資源區域的文字字串。</span><span class="sxs-lookup"><span data-stu-id="e88c9-116">The name is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="e88c9-117">應用程式應該為此字串配置大約80個位元組。</span><span class="sxs-lookup"><span data-stu-id="e88c9-117">Applications should allocate approximately 80 bytes for this string.</span></span> <span data-ttu-id="e88c9-118">如果驅動程式未包含名稱資源，則會傳回登錄或 SYSTEM.INI 檔中所列之驅動程式的完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="e88c9-118">If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e88c9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e88c9-119">Requirements</span></span>



| <span data-ttu-id="e88c9-120">需求</span><span class="sxs-lookup"><span data-stu-id="e88c9-120">Requirement</span></span> | <span data-ttu-id="e88c9-121">值</span><span class="sxs-lookup"><span data-stu-id="e88c9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e88c9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e88c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e88c9-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e88c9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e88c9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e88c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e88c9-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e88c9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e88c9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e88c9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e88c9-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="e88c9-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e88c9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e88c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e88c9-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="e88c9-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e88c9-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="e88c9-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





