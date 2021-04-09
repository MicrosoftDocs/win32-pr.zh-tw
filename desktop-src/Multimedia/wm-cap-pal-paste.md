---
title: 'WM_CAP_PAL_PASTE 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL \_ 貼上訊息會從剪貼簿複製元件，並將它傳遞至 capture 驅動程式。 您可以使用 capPalettePaste 宏明確地傳送此訊息。
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934175"
---
# <a name="wm_cap_pal_paste-message"></a><span data-ttu-id="9f6a9-105">WM \_ CAP \_ PAL \_ 貼上訊息</span><span class="sxs-lookup"><span data-stu-id="9f6a9-105">WM\_CAP\_PAL\_PASTE message</span></span>

<span data-ttu-id="9f6a9-106">**WM \_ CAP \_ PAL \_ 貼** 上訊息會從剪貼簿複製元件，並將它傳遞至 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="9f6a9-106">The **WM\_CAP\_PAL\_PASTE** message copies the palette from the clipboard and passes it to a capture driver.</span></span> <span data-ttu-id="9f6a9-107">您可以使用 [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9f6a9-107">You can send this message explicitly or by using the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) macro.</span></span>


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="9f6a9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f6a9-108">Return Value</span></span>

<span data-ttu-id="9f6a9-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9f6a9-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="9f6a9-110">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="9f6a9-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f6a9-111">備註</span><span class="sxs-lookup"><span data-stu-id="9f6a9-111">Remarks</span></span>

<span data-ttu-id="9f6a9-112">捕捉驅動程式會在指定的數位化影片格式需要時使用調色板。</span><span class="sxs-lookup"><span data-stu-id="9f6a9-112">A capture driver uses a palette when required by the specified digitized video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6a9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f6a9-113">Requirements</span></span>



| <span data-ttu-id="9f6a9-114">需求</span><span class="sxs-lookup"><span data-stu-id="9f6a9-114">Requirement</span></span> | <span data-ttu-id="9f6a9-115">值</span><span class="sxs-lookup"><span data-stu-id="9f6a9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9f6a9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f6a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f6a9-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f6a9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9f6a9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f6a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f6a9-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f6a9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9f6a9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9f6a9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f6a9-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f6a9-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6a9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f6a9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6a9-123">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="9f6a9-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9f6a9-124">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="9f6a9-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





