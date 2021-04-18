---
description: 指定成功連接至媒體接收器的串流。
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: 'MFP_PKEY_StreamRenderingResults 屬性 (Mfplay) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318547"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a><span data-ttu-id="6e96e-103">MFP \_ PKEY \_ StreamRenderingResults 屬性</span><span class="sxs-lookup"><span data-stu-id="6e96e-103">MFP\_PKEY\_StreamRenderingResults property</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e96e-104">已取代。</span><span class="sxs-lookup"><span data-stu-id="6e96e-104">Deprecated.</span></span> <span data-ttu-id="6e96e-105">此 API 可能會從 Windows 的未來版本中移除。</span><span class="sxs-lookup"><span data-stu-id="6e96e-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="6e96e-106">應用程式應該使用 [媒體會話](media-session.md) 來播放。</span><span class="sxs-lookup"><span data-stu-id="6e96e-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="6e96e-107">指定成功連接至媒體接收器的串流。</span><span class="sxs-lookup"><span data-stu-id="6e96e-107">Specifies which streams were connected successfully to a media sink.</span></span>



<span data-ttu-id="6e96e-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="6e96e-108">Data type</span></span>

<span data-ttu-id="6e96e-109">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="6e96e-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6e96e-110">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="6e96e-110">PROPVARIANT member</span></span>

<span data-ttu-id="6e96e-111">**DWORD** 值的陣列 (**CAUL**) </span><span class="sxs-lookup"><span data-stu-id="6e96e-111">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="6e96e-112">VT \_ 向量 \| vt \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6e96e-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="6e96e-113">**科爾**</span><span class="sxs-lookup"><span data-stu-id="6e96e-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="6e96e-114">備註</span><span class="sxs-lookup"><span data-stu-id="6e96e-114">Remarks</span></span>

<span data-ttu-id="6e96e-115">這個屬性可以使用 [MFP] **\_ 事件 \_ 類型 \_ MEDIAITEM \_ SET** 事件來傳送。</span><span class="sxs-lookup"><span data-stu-id="6e96e-115">This property can be sent with the **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event.</span></span>

<span data-ttu-id="6e96e-116">屬性的值是 **HRESULT** s 的陣列。</span><span class="sxs-lookup"><span data-stu-id="6e96e-116">The value of the property is an array of **HRESULT** s.</span></span> <span data-ttu-id="6e96e-117">陣列專案對應到目前媒體專案上的資料流程。</span><span class="sxs-lookup"><span data-stu-id="6e96e-117">The array entries correspond to streams on the current media item.</span></span> <span data-ttu-id="6e96e-118">陣列中的每個專案都會指出對應的資料流程是否已連接到媒體接收器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6e96e-118">Each entry in the array indicates whether the corresponding stream was connected to a media sink, as follows:</span></span>

-   <span data-ttu-id="6e96e-119">如果資料流程連接到媒體接收器，則值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6e96e-119">If the stream is connected to a media sink, the value is **S\_OK**.</span></span>
-   <span data-ttu-id="6e96e-120">如果未選取資料流程，則值為 **S \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6e96e-120">If the stream is not selected, the value is **S\_FALSE**.</span></span>
-   <span data-ttu-id="6e96e-121">如果嘗試連接資料流程時發生錯誤，此值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6e96e-121">If an error occurred while attempting to connect the stream, the value is an error code.</span></span>

<span data-ttu-id="6e96e-122">如果至少有一個資料流程連接成功，就可以播放。</span><span class="sxs-lookup"><span data-stu-id="6e96e-122">If at least one stream was connected successfully, playback is possible.</span></span> <span data-ttu-id="6e96e-123">例如，使用者可能會有播放音訊串流所需的編解碼器，但無法播放影片串流。</span><span class="sxs-lookup"><span data-stu-id="6e96e-123">For example, the user might have the codec needed to play the audio stream but not to play the video stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e96e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e96e-124">Requirements</span></span>



| <span data-ttu-id="6e96e-125">需求</span><span class="sxs-lookup"><span data-stu-id="6e96e-125">Requirement</span></span> | <span data-ttu-id="6e96e-126">值</span><span class="sxs-lookup"><span data-stu-id="6e96e-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6e96e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e96e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6e96e-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e96e-128">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6e96e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e96e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6e96e-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e96e-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e96e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6e96e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e96e-132"><dt>Mfplay。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e96e-132"><dt>Mfplay.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e96e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e96e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e96e-134">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="6e96e-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6e96e-135">**MFP \_ MEDIAITEM \_ 設定 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="6e96e-135">**MFP\_MEDIAITEM\_SET\_EVENT**</span></span>](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




