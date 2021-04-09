---
description: 指定影片捕獲來源上的資料流程是否為靜止影像資料流程。
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: 'MF_DEVICESTREAM_IMAGE_STREAM 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690900"
---
# <a name="mf_devicestream_image_stream-attribute"></a><span data-ttu-id="cec86-103">MF \_ DEVICESTREAM \_ 影像 \_ 資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="cec86-103">MF\_DEVICESTREAM\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="cec86-104">指定影片捕獲來源上的資料流程是否為靜止影像資料流程。</span><span class="sxs-lookup"><span data-stu-id="cec86-104">Specifies whether a stream on a video capture source is a still-image stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="cec86-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="cec86-105">Data type</span></span>

<span data-ttu-id="cec86-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="cec86-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cec86-107">備註</span><span class="sxs-lookup"><span data-stu-id="cec86-107">Remarks</span></span>

<span data-ttu-id="cec86-108">有些攝影機會公開可產生高解析度影像的靜止影像串流。</span><span class="sxs-lookup"><span data-stu-id="cec86-108">Some video cameras expose a still-image stream that produces high-resolution images.</span></span> <span data-ttu-id="cec86-109">影像串流可能會產生未壓縮的影像或 JPEG 影像。</span><span class="sxs-lookup"><span data-stu-id="cec86-109">The image stream might produce uncompressed images or JPEG images.</span></span> <span data-ttu-id="cec86-110">如果相機有影像串流，則在影像串流上，capture 裝置的媒體來源會將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="cec86-110">If the camera has an image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="cec86-111">若要取得這個屬性，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="cec86-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="cec86-112">查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cec86-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="cec86-113">呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得資料流程的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="cec86-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="cec86-114">呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 以取得屬性。</span><span class="sxs-lookup"><span data-stu-id="cec86-114">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec86-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cec86-115">Requirements</span></span>



| <span data-ttu-id="cec86-116">需求</span><span class="sxs-lookup"><span data-stu-id="cec86-116">Requirement</span></span> | <span data-ttu-id="cec86-117">值</span><span class="sxs-lookup"><span data-stu-id="cec86-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cec86-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cec86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cec86-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec86-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cec86-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cec86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cec86-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec86-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cec86-122">標頭</span><span class="sxs-lookup"><span data-stu-id="cec86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cec86-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cec86-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec86-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cec86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec86-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="cec86-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




