---
title: 'MM_MIXM_CONTROL_CHANGE 訊息 (Mmsystem .h) '
description: '\_MIXM \_ 控制項 \_ 變更訊息是由混音器裝置傳送，以通知應用程式，與音訊行相關聯的控制項狀態已變更。 應用程式應該針對指定的控制項重新整理其顯示和快取的值。'
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965506"
---
# <a name="mm_mixm_control_change-message"></a><span data-ttu-id="66f0d-105">MM \_ MIXM \_ 控制項 \_ 變更訊息</span><span class="sxs-lookup"><span data-stu-id="66f0d-105">MM\_MIXM\_CONTROL\_CHANGE message</span></span>

<span data-ttu-id="66f0d-106">**\_ MIXM \_ 控制項 \_ 變更** 訊息是由混音器裝置傳送，以通知應用程式，與音訊行相關聯的控制項狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="66f0d-106">The **MM\_MIXM\_CONTROL\_CHANGE** message is sent by a mixer device to notify an application that the state of a control associated with an audio line has changed.</span></span> <span data-ttu-id="66f0d-107">應用程式應該針對指定的控制項重新整理其顯示和快取的值。</span><span class="sxs-lookup"><span data-stu-id="66f0d-107">The application should refresh its display and cached values for the specified control.</span></span>


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a><span data-ttu-id="66f0d-108">參數</span><span class="sxs-lookup"><span data-stu-id="66f0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f0d-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="66f0d-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="66f0d-110">混音器裝置的控制碼 (**HMIXER** 傳送通知訊息的) 。</span><span class="sxs-lookup"><span data-stu-id="66f0d-110">Handle to the mixer device (**HMIXER**) that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="66f0d-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span><span class="sxs-lookup"><span data-stu-id="66f0d-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span></span>
</dt> <dd>

<span data-ttu-id="66f0d-112">已變更狀態之混音器控制項的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="66f0d-112">Control identifier for the mixer control that has changed state.</span></span> <span data-ttu-id="66f0d-113">此識別碼與 **mixerGetLineControls** 函數所傳回之 **MIXERCONTROL** 結構的 **dwControlID** 成員相同。</span><span class="sxs-lookup"><span data-stu-id="66f0d-113">This identifier is the same as the **dwControlID** member of the **MIXERCONTROL** structure returned by the **mixerGetLineControls** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66f0d-114">備註</span><span class="sxs-lookup"><span data-stu-id="66f0d-114">Remarks</span></span>

<span data-ttu-id="66f0d-115">應用程式必須開啟混音器裝置，並指定要接收 **MM \_ MIXM \_ 控制項 \_ 變更** 訊息的回呼視窗。</span><span class="sxs-lookup"><span data-stu-id="66f0d-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_CONTROL\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f0d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="66f0d-116">Requirements</span></span>



| <span data-ttu-id="66f0d-117">需求</span><span class="sxs-lookup"><span data-stu-id="66f0d-117">Requirement</span></span> | <span data-ttu-id="66f0d-118">值</span><span class="sxs-lookup"><span data-stu-id="66f0d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f0d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66f0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66f0d-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66f0d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66f0d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66f0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66f0d-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66f0d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="66f0d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="66f0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66f0d-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="66f0d-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f0d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66f0d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f0d-126">音訊 Mixers</span><span class="sxs-lookup"><span data-stu-id="66f0d-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="66f0d-127">音訊混音器訊息</span><span class="sxs-lookup"><span data-stu-id="66f0d-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





