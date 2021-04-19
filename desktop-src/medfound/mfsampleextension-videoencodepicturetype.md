---
description: 指定影片編碼器輸出的圖片類型。
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: 'MFSampleExtension_VideoEncodePictureType 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974166"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a><span data-ttu-id="27c9d-103">MFSampleExtension \_ VideoEncodePictureType 屬性</span><span class="sxs-lookup"><span data-stu-id="27c9d-103">MFSampleExtension\_VideoEncodePictureType attribute</span></span>

<span data-ttu-id="27c9d-104">指定影片編碼器輸出的圖片類型。</span><span class="sxs-lookup"><span data-stu-id="27c9d-104">Specifies the type of picture that is output by a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="27c9d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="27c9d-105">Data type</span></span>

<span data-ttu-id="27c9d-106">**eAVEncH264PictureType \_B** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="27c9d-106">**eAVEncH264PictureType\_B** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="27c9d-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="27c9d-107">Get/set</span></span>

<span data-ttu-id="27c9d-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="27c9d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="27c9d-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="27c9d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="27c9d-110">適用於</span><span class="sxs-lookup"><span data-stu-id="27c9d-110">Applies to</span></span>

[<span data-ttu-id="27c9d-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="27c9d-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="27c9d-112">備註</span><span class="sxs-lookup"><span data-stu-id="27c9d-112">Remarks</span></span>

<span data-ttu-id="27c9d-113">H.264 [**Video 編碼器**](h-264-video-encoder.md) 會在其產生的輸出範例上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="27c9d-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span> <span data-ttu-id="27c9d-114">屬性的值是 [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="27c9d-114">The value of the attribute is a member of the [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c9d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="27c9d-115">Requirements</span></span>



| <span data-ttu-id="27c9d-116">需求</span><span class="sxs-lookup"><span data-stu-id="27c9d-116">Requirement</span></span> | <span data-ttu-id="27c9d-117">值</span><span class="sxs-lookup"><span data-stu-id="27c9d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27c9d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27c9d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27c9d-119">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27c9d-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="27c9d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27c9d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27c9d-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="27c9d-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="27c9d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="27c9d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27c9d-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="27c9d-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c9d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27c9d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c9d-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="27c9d-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="27c9d-126">**H.264 影片編碼器**</span><span class="sxs-lookup"><span data-stu-id="27c9d-126">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="27c9d-127">範例屬性</span><span class="sxs-lookup"><span data-stu-id="27c9d-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="27c9d-128">媒體範例</span><span class="sxs-lookup"><span data-stu-id="27c9d-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




