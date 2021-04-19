---
description: 為 h.264 影片資料流程指定支援的速率控制模式。
ms.assetid: DAA62ECD-AFA2-40C2-9B52-F2D581F4D894
title: 'MF_MT_H264_SUPPORTED_RATE_CONTROL_MODES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b315bf41d662dd5abb283c346710f485789ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986362"
---
# <a name="mf_mt_h264_supported_rate_control_modes-attribute"></a><span data-ttu-id="b1a39-103">MF \_ MT \_ H264 \_ 支援的 \_ 速率 \_ 控制 \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="b1a39-103">MF\_MT\_H264\_SUPPORTED\_RATE\_CONTROL\_MODES attribute</span></span>

<span data-ttu-id="b1a39-104">為 h.264 影片資料流程指定支援的速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="b1a39-104">Specifies the supported rate-control modes for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1a39-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b1a39-105">Data type</span></span>

<span data-ttu-id="b1a39-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b1a39-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b1a39-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b1a39-107">Get/set</span></span>

<span data-ttu-id="b1a39-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="b1a39-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b1a39-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="b1a39-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b1a39-110">適用於</span><span class="sxs-lookup"><span data-stu-id="b1a39-110">Applies to</span></span>

[<span data-ttu-id="b1a39-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1a39-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b1a39-112">備註</span><span class="sxs-lookup"><span data-stu-id="b1a39-112">Remarks</span></span>

<span data-ttu-id="b1a39-113">此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b1a39-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="b1a39-114">值會對應至 UVC 1.5 h.264 視頻格式描述項中的 **bmSupportedRateControlModes** 欄位。</span><span class="sxs-lookup"><span data-stu-id="b1a39-114">The value corresponds to the **bmSupportedRateControlModes** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="b1a39-115">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="b1a39-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a39-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1a39-116">Requirements</span></span>



| <span data-ttu-id="b1a39-117">需求</span><span class="sxs-lookup"><span data-stu-id="b1a39-117">Requirement</span></span> | <span data-ttu-id="b1a39-118">值</span><span class="sxs-lookup"><span data-stu-id="b1a39-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a39-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1a39-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a39-120">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1a39-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b1a39-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1a39-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a39-122">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1a39-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b1a39-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b1a39-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a39-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a39-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a39-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1a39-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a39-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b1a39-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1a39-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="b1a39-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




