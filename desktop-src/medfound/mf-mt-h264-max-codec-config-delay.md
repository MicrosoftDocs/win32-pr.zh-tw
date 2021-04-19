---
description: H.264 編碼器回應命令所需的最大框架數目。
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: 'MF_MT_H264_MAX_CODEC_CONFIG_DELAY 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993086"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a><span data-ttu-id="23132-103">MF \_ MT \_ H264 \_ 最大 \_ 編解碼器設定 \_ \_ 延遲屬性</span><span class="sxs-lookup"><span data-stu-id="23132-103">MF\_MT\_H264\_MAX\_CODEC\_CONFIG\_DELAY attribute</span></span>

<span data-ttu-id="23132-104">H.264 編碼器回應命令所需的最大框架數目。</span><span class="sxs-lookup"><span data-stu-id="23132-104">The maximum number of frames the H.264 encoder takes to respond to a command.</span></span>

## <a name="data-type"></a><span data-ttu-id="23132-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="23132-105">Data type</span></span>

<span data-ttu-id="23132-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="23132-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="23132-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="23132-107">Get/set</span></span>

<span data-ttu-id="23132-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="23132-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="23132-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="23132-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="23132-110">適用於</span><span class="sxs-lookup"><span data-stu-id="23132-110">Applies to</span></span>

[<span data-ttu-id="23132-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="23132-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="23132-112">備註</span><span class="sxs-lookup"><span data-stu-id="23132-112">Remarks</span></span>

<span data-ttu-id="23132-113">此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="23132-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="23132-114">值會對應至 UVC 1.2 h.264 視頻格式描述項中的 **bMaxCodecConfigDelay** 欄位。</span><span class="sxs-lookup"><span data-stu-id="23132-114">The value corresponds to the **bMaxCodecConfigDelay** field in the UVC 1.2 H.264 video format descriptor.</span></span>

<span data-ttu-id="23132-115">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="23132-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23132-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="23132-116">Requirements</span></span>



| <span data-ttu-id="23132-117">需求</span><span class="sxs-lookup"><span data-stu-id="23132-117">Requirement</span></span> | <span data-ttu-id="23132-118">值</span><span class="sxs-lookup"><span data-stu-id="23132-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23132-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23132-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23132-120">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23132-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="23132-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23132-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23132-122">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23132-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="23132-123">標頭</span><span class="sxs-lookup"><span data-stu-id="23132-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23132-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="23132-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23132-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23132-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23132-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="23132-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="23132-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="23132-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




