---
description: 指定 h.264 影片資料流程的功能旗標。
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: 'MF_MT_H264_CAPABILITIES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67f796e09d4b57667a3d8f7c7c0fa888eba7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852436"
---
# <a name="mf_mt_h264_capabilities-attribute"></a><span data-ttu-id="500f1-103">MF \_ MT \_ H264 \_ 功能屬性</span><span class="sxs-lookup"><span data-stu-id="500f1-103">MF\_MT\_H264\_CAPABILITIES attribute</span></span>

<span data-ttu-id="500f1-104">指定 h.264 影片資料流程的功能旗標。</span><span class="sxs-lookup"><span data-stu-id="500f1-104">Specifies the capabilities flags for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="500f1-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="500f1-105">Data type</span></span>

<span data-ttu-id="500f1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="500f1-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="500f1-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="500f1-107">Get/set</span></span>

<span data-ttu-id="500f1-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="500f1-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="500f1-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="500f1-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="500f1-110">適用於</span><span class="sxs-lookup"><span data-stu-id="500f1-110">Applies to</span></span>

[<span data-ttu-id="500f1-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="500f1-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="500f1-112">備註</span><span class="sxs-lookup"><span data-stu-id="500f1-112">Remarks</span></span>

<span data-ttu-id="500f1-113">此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="500f1-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="500f1-114">值會對應至 UVC 1.5 h.264 影片框架描述項中的 **bmCapabilities** 欄位。</span><span class="sxs-lookup"><span data-stu-id="500f1-114">The value corresponds to the **bmCapabilities** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="500f1-115">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="500f1-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="500f1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="500f1-116">Requirements</span></span>



| <span data-ttu-id="500f1-117">需求</span><span class="sxs-lookup"><span data-stu-id="500f1-117">Requirement</span></span> | <span data-ttu-id="500f1-118">值</span><span class="sxs-lookup"><span data-stu-id="500f1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="500f1-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="500f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="500f1-120">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="500f1-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="500f1-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="500f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="500f1-122">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="500f1-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="500f1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="500f1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="500f1-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="500f1-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="500f1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="500f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500f1-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="500f1-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="500f1-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="500f1-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




