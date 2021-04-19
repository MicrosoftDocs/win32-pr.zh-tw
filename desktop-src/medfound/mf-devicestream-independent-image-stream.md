---
description: 指定影片捕獲來源上的影像資料流程是否與影片資料流程無關。
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: 'MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982324"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a><span data-ttu-id="e0624-103">MF \_ DEVICESTREAM \_ 獨立 \_ 映射 \_ 資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="e0624-103">MF\_DEVICESTREAM\_INDEPENDENT\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="e0624-104">指定影片捕獲來源上的影像資料流程是否與影片資料流程無關。</span><span class="sxs-lookup"><span data-stu-id="e0624-104">Specifies whether the image stream on a video capture source is independent of the video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e0624-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e0624-105">Data type</span></span>

<span data-ttu-id="e0624-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e0624-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e0624-107">備註</span><span class="sxs-lookup"><span data-stu-id="e0624-107">Remarks</span></span>

<span data-ttu-id="e0624-108">某些 USB 攝影機會公開產生仍為影像的資料流程。</span><span class="sxs-lookup"><span data-stu-id="e0624-108">Some USB video cameras expose a stream that produces still images.</span></span> <span data-ttu-id="e0624-109">在某些相機中，影像串流只會傳回影片串流中的下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="e0624-109">In some cameras, the image stream simply returns the next frame from the video stream.</span></span> <span data-ttu-id="e0624-110">在其他相機中，影像串流會獨立于影片串流。</span><span class="sxs-lookup"><span data-stu-id="e0624-110">In other cameras, the image stream functions independently of the video stream.</span></span> <span data-ttu-id="e0624-111">如果相機有獨立的影像串流，則在影像串流上，capture 裝置的媒體來源會將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e0624-111">If the camera has an independent image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="e0624-112">若要取得這個屬性，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e0624-112">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="e0624-113">查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="e0624-113">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="e0624-114">呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得資料流程的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="e0624-114">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="e0624-115">呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 以取得屬性。</span><span class="sxs-lookup"><span data-stu-id="e0624-115">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

<span data-ttu-id="e0624-116">只有當 [MF \_ DEVICESTREAM \_ 影像 \_ 資料流程](mf-devicestream-image-stream.md) 屬性為 **TRUE** 時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="e0624-116">This attribute applies only when the [MF\_DEVICESTREAM\_IMAGE\_STREAM](mf-devicestream-image-stream.md) attribute is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0624-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0624-117">Requirements</span></span>



| <span data-ttu-id="e0624-118">需求</span><span class="sxs-lookup"><span data-stu-id="e0624-118">Requirement</span></span> | <span data-ttu-id="e0624-119">值</span><span class="sxs-lookup"><span data-stu-id="e0624-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0624-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0624-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0624-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0624-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e0624-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0624-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0624-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0624-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0624-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e0624-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0624-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0624-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0624-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0624-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0624-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e0624-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




