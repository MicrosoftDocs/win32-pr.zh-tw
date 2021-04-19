---
title: 'WM_CAP_PAL_SAVE 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL 儲存訊息會將 \_ 目前的調色板儲存至元件檔案。 調色板檔案通常會使用副檔名。朋友。 您可以使用 capPaletteSave 宏明確地傳送此訊息。
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966934"
---
# <a name="wm_cap_pal_save-message"></a><span data-ttu-id="7cf4a-106">WM \_ CAP \_ PAL \_ 儲存訊息</span><span class="sxs-lookup"><span data-stu-id="7cf4a-106">WM\_CAP\_PAL\_SAVE message</span></span>

<span data-ttu-id="7cf4a-107">**WM \_ CAP \_ PAL \_ 儲存** 訊息會將目前的調色板儲存至元件檔案。</span><span class="sxs-lookup"><span data-stu-id="7cf4a-107">The **WM\_CAP\_PAL\_SAVE** message saves the current palette to a palette file.</span></span> <span data-ttu-id="7cf4a-108">調色板檔案通常會使用副檔名。朋友。</span><span class="sxs-lookup"><span data-stu-id="7cf4a-108">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="7cf4a-109">您可以使用 [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="7cf4a-109">You can send this message explicitly or by using the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro.</span></span>


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="7cf4a-110">參數</span><span class="sxs-lookup"><span data-stu-id="7cf4a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf4a-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="7cf4a-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="7cf4a-112">包含調色板檔案名之以 null 結尾的字串指標。</span><span class="sxs-lookup"><span data-stu-id="7cf4a-112">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf4a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cf4a-113">Return Value</span></span>

<span data-ttu-id="7cf4a-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7cf4a-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="7cf4a-115">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="7cf4a-115">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf4a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cf4a-116">Requirements</span></span>



| <span data-ttu-id="7cf4a-117">需求</span><span class="sxs-lookup"><span data-stu-id="7cf4a-117">Requirement</span></span> | <span data-ttu-id="7cf4a-118">值</span><span class="sxs-lookup"><span data-stu-id="7cf4a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7cf4a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cf4a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf4a-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cf4a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7cf4a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cf4a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf4a-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cf4a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7cf4a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7cf4a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cf4a-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="7cf4a-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf4a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cf4a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf4a-126">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="7cf4a-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7cf4a-127">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="7cf4a-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





