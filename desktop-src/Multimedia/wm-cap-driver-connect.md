---
title: 'WM_CAP_DRIVER_CONNECT 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式連線 \_ ] 訊息會將捕獲視窗連接至 capture 驅動程式。 您可以使用 capDriverConnect 宏明確地傳送此訊息。'
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384470"
---
# <a name="wm_cap_driver_connect-message"></a><span data-ttu-id="5d993-105">WM \_ CAP \_ 驅動程式 \_ 連接訊息</span><span class="sxs-lookup"><span data-stu-id="5d993-105">WM\_CAP\_DRIVER\_CONNECT message</span></span>

<span data-ttu-id="5d993-106">[ **WM \_ CAP \_ 驅動程式連線 \_ ]** 訊息會將捕獲視窗連接至 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5d993-106">The **WM\_CAP\_DRIVER\_CONNECT** message connects a capture window to a capture driver.</span></span> <span data-ttu-id="5d993-107">您可以使用 [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="5d993-107">You can send this message explicitly or by using the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="5d993-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d993-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d993-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="5d993-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="5d993-110">Capture 驅動程式的索引。</span><span class="sxs-lookup"><span data-stu-id="5d993-110">Index of the capture driver.</span></span> <span data-ttu-id="5d993-111">索引的範圍可以從0到9。</span><span class="sxs-lookup"><span data-stu-id="5d993-111">The index can range from 0 through 9.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d993-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d993-112">Return Value</span></span>

<span data-ttu-id="5d993-113">如果成功，則傳回 **TRUE** ，如果指定的捕獲驅動程式無法連接到捕捉視窗，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5d993-113">Returns **TRUE** if successful or **FALSE** if the specified capture driver cannot be connected to the capture window.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d993-114">備註</span><span class="sxs-lookup"><span data-stu-id="5d993-114">Remarks</span></span>

<span data-ttu-id="5d993-115">將捕獲驅動程式連接到「捕獲」視窗，會自動中斷任何先前連線的捕獲驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5d993-115">Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d993-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d993-116">Requirements</span></span>



| <span data-ttu-id="5d993-117">需求</span><span class="sxs-lookup"><span data-stu-id="5d993-117">Requirement</span></span> | <span data-ttu-id="5d993-118">值</span><span class="sxs-lookup"><span data-stu-id="5d993-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5d993-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d993-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5d993-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d993-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5d993-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d993-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5d993-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d993-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d993-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5d993-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d993-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d993-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d993-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d993-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d993-126">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="5d993-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5d993-127">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="5d993-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





