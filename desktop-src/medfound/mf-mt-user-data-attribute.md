---
description: 包含媒體類型的其他格式資料。
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: 'MF_MT_USER_DATA 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984660"
---
# <a name="mf_mt_user_data-attribute"></a><span data-ttu-id="f32be-103">MF \_ MT \_ 使用者 \_ 資料屬性</span><span class="sxs-lookup"><span data-stu-id="f32be-103">MF\_MT\_USER\_DATA attribute</span></span>

<span data-ttu-id="f32be-104">包含媒體類型的其他格式資料。</span><span class="sxs-lookup"><span data-stu-id="f32be-104">Contains additional format data for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="f32be-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f32be-105">Data type</span></span>

<span data-ttu-id="f32be-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="f32be-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="f32be-107">備註</span><span class="sxs-lookup"><span data-stu-id="f32be-107">Remarks</span></span>

<span data-ttu-id="f32be-108">這個屬性中資料的意義取決於媒體類型所描述的格式。</span><span class="sxs-lookup"><span data-stu-id="f32be-108">The meaning of the data in this attribute depends on the format that is described by the media type.</span></span>



| <span data-ttu-id="f32be-109">格式類型</span><span class="sxs-lookup"><span data-stu-id="f32be-109">Format Type</span></span>                                                                                                           | <span data-ttu-id="f32be-110">其他格式資料</span><span class="sxs-lookup"><span data-stu-id="f32be-110">Additional Format Data</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32be-111">Windows Media 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="f32be-111">Windows Media codec.</span></span>                                                                                                  | <span data-ttu-id="f32be-112">編解碼器私用資料。</span><span class="sxs-lookup"><span data-stu-id="f32be-112">Codec private data.</span></span>                                                                                                                       |
| <span data-ttu-id="f32be-113">已轉換的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構。</span><span class="sxs-lookup"><span data-stu-id="f32be-113">Converted [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span>   | <span data-ttu-id="f32be-114">在 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構後面出現的額外資料，不包括色彩表或色彩遮罩。</span><span class="sxs-lookup"><span data-stu-id="f32be-114">Extra data that appears after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, not including the color table or color masks.</span></span> |
| <span data-ttu-id="f32be-115">已轉換的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 或 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="f32be-115">Converted [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> | <span data-ttu-id="f32be-116">在音訊格式結構後面出現的額外資料。</span><span class="sxs-lookup"><span data-stu-id="f32be-116">Extra data that appears after the audio format structure.</span></span>                                                                                 |



 

<span data-ttu-id="f32be-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="f32be-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f32be-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f32be-118">Requirements</span></span>



| <span data-ttu-id="f32be-119">需求</span><span class="sxs-lookup"><span data-stu-id="f32be-119">Requirement</span></span> | <span data-ttu-id="f32be-120">值</span><span class="sxs-lookup"><span data-stu-id="f32be-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f32be-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f32be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f32be-122">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f32be-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f32be-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f32be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f32be-124">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f32be-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f32be-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f32be-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f32be-126"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f32be-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32be-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f32be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32be-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f32be-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f32be-129">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="f32be-129">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="f32be-130">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="f32be-130">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="f32be-131">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="f32be-131">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f32be-132">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="f32be-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
