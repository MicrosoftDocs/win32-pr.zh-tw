---
description: 以 Windows Media 音訊檔的平均磁片區層級為目標。
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: 'MF_MT_AUDIO_WMADRC_AVGTARGET 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320628"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a><span data-ttu-id="747f0-103">MF \_ MT \_ 音訊 \_ WMADRC \_ AVGTARGET 屬性</span><span class="sxs-lookup"><span data-stu-id="747f0-103">MF\_MT\_AUDIO\_WMADRC\_AVGTARGET attribute</span></span>

<span data-ttu-id="747f0-104">以 Windows Media 音訊檔的平均磁片區層級為目標。</span><span class="sxs-lookup"><span data-stu-id="747f0-104">Target average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="747f0-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="747f0-105">Data type</span></span>

<span data-ttu-id="747f0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="747f0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="747f0-107">備註</span><span class="sxs-lookup"><span data-stu-id="747f0-107">Remarks</span></span>

<span data-ttu-id="747f0-108">此屬性適用于 Windows Media 音訊編解碼器的音訊媒體類型。</span><span class="sxs-lookup"><span data-stu-id="747f0-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="747f0-109">它會指定內容的目標平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="747f0-109">It specifies the target average volume level of the content.</span></span> <span data-ttu-id="747f0-110">此解碼器可以使用此值來執行動態範圍控制。</span><span class="sxs-lookup"><span data-stu-id="747f0-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="747f0-111">如果 ASF 標頭包含 [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md)屬性， [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)方法會將此屬性新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="747f0-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) attribute.</span></span> <span data-ttu-id="747f0-112">此屬性記載于 Windows Media Format SDK 檔中。</span><span class="sxs-lookup"><span data-stu-id="747f0-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="747f0-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="747f0-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="747f0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="747f0-114">Requirements</span></span>



| <span data-ttu-id="747f0-115">需求</span><span class="sxs-lookup"><span data-stu-id="747f0-115">Requirement</span></span> | <span data-ttu-id="747f0-116">值</span><span class="sxs-lookup"><span data-stu-id="747f0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="747f0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="747f0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="747f0-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="747f0-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="747f0-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="747f0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="747f0-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="747f0-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="747f0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="747f0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="747f0-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="747f0-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747f0-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="747f0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747f0-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="747f0-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="747f0-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="747f0-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="747f0-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="747f0-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="747f0-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="747f0-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="747f0-128">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="747f0-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
