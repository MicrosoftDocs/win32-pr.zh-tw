---
title: 'WM_CAP_PAL_OPEN 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL 開啟的 \_ 訊息會從調色板檔案載入新的元件，並將它傳遞至 capture 驅動程式。
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968946"
---
# <a name="wm_cap_pal_open-message"></a><span data-ttu-id="28e60-104">WM \_ CAP \_ PAL \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="28e60-104">WM\_CAP\_PAL\_OPEN message</span></span>

<span data-ttu-id="28e60-105">**WM \_ CAP \_ PAL \_ 開啟** 的訊息會從調色板檔案載入新的元件，並將它傳遞至 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="28e60-105">The **WM\_CAP\_PAL\_OPEN** message loads a new palette from a palette file and passes it to a capture driver.</span></span> <span data-ttu-id="28e60-106">調色板檔案通常會使用副檔名。朋友。</span><span class="sxs-lookup"><span data-stu-id="28e60-106">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="28e60-107">捕捉驅動程式會在指定的數位化影像格式需要時使用調色板。</span><span class="sxs-lookup"><span data-stu-id="28e60-107">A capture driver uses a palette when required by the specified digitized image format.</span></span> <span data-ttu-id="28e60-108">您可以使用 [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="28e60-108">You can send this message explicitly or by using the [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro.</span></span>


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="28e60-109">參數</span><span class="sxs-lookup"><span data-stu-id="28e60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e60-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="28e60-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="28e60-111">包含調色板檔案名之以 null 結尾的字串指標。</span><span class="sxs-lookup"><span data-stu-id="28e60-111">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e60-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="28e60-112">Return Value</span></span>

<span data-ttu-id="28e60-113">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="28e60-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="28e60-114">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="28e60-114">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e60-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="28e60-115">Requirements</span></span>



| <span data-ttu-id="28e60-116">需求</span><span class="sxs-lookup"><span data-stu-id="28e60-116">Requirement</span></span> | <span data-ttu-id="28e60-117">值</span><span class="sxs-lookup"><span data-stu-id="28e60-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28e60-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28e60-118">Minimum supported client</span></span><br/> | <span data-ttu-id="28e60-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28e60-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="28e60-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28e60-120">Minimum supported server</span></span><br/> | <span data-ttu-id="28e60-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28e60-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="28e60-122">標頭</span><span class="sxs-lookup"><span data-stu-id="28e60-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e60-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="28e60-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e60-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28e60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e60-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="28e60-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="28e60-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="28e60-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





