---
title: 'MM_MIXM_LINE_CHANGE 訊息 (Mmsystem .h) '
description: '\_MIXM \_ 線路 \_ 變更訊息會由混音器裝置傳送，以通知應用程式，指定裝置上的音訊行狀態已變更。 應用程式應該針對指定的音訊行重新整理其顯示和快取的值。'
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968975"
---
# <a name="mm_mixm_line_change-message"></a><span data-ttu-id="dba7c-105">MM \_ MIXM \_ 行 \_ 變更訊息</span><span class="sxs-lookup"><span data-stu-id="dba7c-105">MM\_MIXM\_LINE\_CHANGE message</span></span>

<span data-ttu-id="dba7c-106">**\_ MIXM \_ 線路 \_ 變更** 訊息會由混音器裝置傳送，以通知應用程式，指定裝置上的音訊行狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="dba7c-106">The **MM\_MIXM\_LINE\_CHANGE** message is sent by a mixer device to notify an application that the state of an audio line on the specified device has changed.</span></span> <span data-ttu-id="dba7c-107">應用程式應該針對指定的音訊行重新整理其顯示和快取的值。</span><span class="sxs-lookup"><span data-stu-id="dba7c-107">The application should refresh its display and cached values for the specified audio line.</span></span>


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a><span data-ttu-id="dba7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="dba7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba7c-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="dba7c-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="dba7c-110">傳送通知訊息的混音器裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dba7c-110">Handle to the mixer device that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="dba7c-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span><span class="sxs-lookup"><span data-stu-id="dba7c-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span></span>
</dt> <dd>

<span data-ttu-id="dba7c-112">已變更狀態之音訊行的行識別碼。</span><span class="sxs-lookup"><span data-stu-id="dba7c-112">Line identifier for the audio line that has changed state.</span></span> <span data-ttu-id="dba7c-113">此識別碼與 **mixerGetLineInfo** 函數所傳回之 **MIXERLINE** 結構的 **dwLineID** 成員相同。</span><span class="sxs-lookup"><span data-stu-id="dba7c-113">This identifier is the same as the **dwLineID** member of the **MIXERLINE** structure returned by the **mixerGetLineInfo** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dba7c-114">備註</span><span class="sxs-lookup"><span data-stu-id="dba7c-114">Remarks</span></span>

<span data-ttu-id="dba7c-115">應用程式必須開啟混音器裝置，並指定要接收 **MM \_ MIXM \_ 線路 \_ 變更** 訊息的回呼視窗。</span><span class="sxs-lookup"><span data-stu-id="dba7c-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_LINE\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba7c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dba7c-116">Requirements</span></span>



| <span data-ttu-id="dba7c-117">需求</span><span class="sxs-lookup"><span data-stu-id="dba7c-117">Requirement</span></span> | <span data-ttu-id="dba7c-118">值</span><span class="sxs-lookup"><span data-stu-id="dba7c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dba7c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dba7c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dba7c-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dba7c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dba7c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dba7c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dba7c-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dba7c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dba7c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="dba7c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dba7c-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="dba7c-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dba7c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dba7c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba7c-126">音訊 Mixers</span><span class="sxs-lookup"><span data-stu-id="dba7c-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="dba7c-127">音訊混音器訊息</span><span class="sxs-lookup"><span data-stu-id="dba7c-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





