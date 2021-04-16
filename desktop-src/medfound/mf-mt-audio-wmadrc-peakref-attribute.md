---
description: 參考 Windows Media 音訊檔案的尖峰磁片區層級。
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: 'MF_MT_AUDIO_WMADRC_PEAKREF 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512821"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a><span data-ttu-id="5ac3d-103">MF \_ MT \_ 音訊 \_ WMADRC \_ PEAKREF 屬性</span><span class="sxs-lookup"><span data-stu-id="5ac3d-103">MF\_MT\_AUDIO\_WMADRC\_PEAKREF attribute</span></span>

<span data-ttu-id="5ac3d-104">參考 Windows Media 音訊檔案的尖峰磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="5ac3d-104">Reference peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="5ac3d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5ac3d-105">Data type</span></span>

<span data-ttu-id="5ac3d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5ac3d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac3d-107">備註</span><span class="sxs-lookup"><span data-stu-id="5ac3d-107">Remarks</span></span>

<span data-ttu-id="5ac3d-108">此屬性適用于 Windows Media 音訊編解碼器的音訊媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5ac3d-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="5ac3d-109">它會指定內容的原始尖峰磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="5ac3d-109">It specifies the original peak volume level of the content.</span></span> <span data-ttu-id="5ac3d-110">此解碼器可以使用此值來執行動態範圍控制。</span><span class="sxs-lookup"><span data-stu-id="5ac3d-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="5ac3d-111">如果 ASF 標頭包含 [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md)屬性， [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)方法會將此屬性新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5ac3d-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) attribute.</span></span> <span data-ttu-id="5ac3d-112">此屬性記載于 Windows Media Format SDK 檔中。</span><span class="sxs-lookup"><span data-stu-id="5ac3d-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="5ac3d-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5ac3d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac3d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ac3d-114">Requirements</span></span>



| <span data-ttu-id="5ac3d-115">需求</span><span class="sxs-lookup"><span data-stu-id="5ac3d-115">Requirement</span></span> | <span data-ttu-id="5ac3d-116">值</span><span class="sxs-lookup"><span data-stu-id="5ac3d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac3d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ac3d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac3d-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ac3d-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5ac3d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ac3d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac3d-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ac3d-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5ac3d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5ac3d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac3d-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac3d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac3d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ac3d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac3d-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5ac3d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ac3d-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5ac3d-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5ac3d-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5ac3d-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5ac3d-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5ac3d-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5ac3d-128">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="5ac3d-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
