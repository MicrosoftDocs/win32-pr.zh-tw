---
description: 指定用來編碼影片範例的 (QP) 的量化參數。
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: 'MFSampleExtension_VideoEncodeQP 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975025"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a><span data-ttu-id="7f5eb-103">MFSampleExtension \_ VideoEncodeQP 屬性</span><span class="sxs-lookup"><span data-stu-id="7f5eb-103">MFSampleExtension\_VideoEncodeQP attribute</span></span>

<span data-ttu-id="7f5eb-104">指定用來編碼影片範例的 (QP) 的量化參數。</span><span class="sxs-lookup"><span data-stu-id="7f5eb-104">Specifies the quantization parameter (QP) that was used to encode a video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f5eb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7f5eb-105">Data type</span></span>

<span data-ttu-id="7f5eb-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="7f5eb-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="7f5eb-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="7f5eb-107">Get/set</span></span>

<span data-ttu-id="7f5eb-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。</span><span class="sxs-lookup"><span data-stu-id="7f5eb-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="7f5eb-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。</span><span class="sxs-lookup"><span data-stu-id="7f5eb-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7f5eb-110">適用於</span><span class="sxs-lookup"><span data-stu-id="7f5eb-110">Applies to</span></span>

[<span data-ttu-id="7f5eb-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="7f5eb-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="7f5eb-112">備註</span><span class="sxs-lookup"><span data-stu-id="7f5eb-112">Remarks</span></span>

<span data-ttu-id="7f5eb-113">H.264 [**Video 編碼器**](h-264-video-encoder.md) 會在其產生的輸出範例上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="7f5eb-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f5eb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f5eb-114">Requirements</span></span>



| <span data-ttu-id="7f5eb-115">需求</span><span class="sxs-lookup"><span data-stu-id="7f5eb-115">Requirement</span></span> | <span data-ttu-id="7f5eb-116">值</span><span class="sxs-lookup"><span data-stu-id="7f5eb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f5eb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f5eb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7f5eb-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f5eb-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7f5eb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f5eb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7f5eb-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="7f5eb-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="7f5eb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7f5eb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f5eb-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f5eb-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f5eb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f5eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f5eb-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7f5eb-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f5eb-125">**H.264 影片編碼器**</span><span class="sxs-lookup"><span data-stu-id="7f5eb-125">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="7f5eb-126">範例屬性</span><span class="sxs-lookup"><span data-stu-id="7f5eb-126">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f5eb-127">媒體範例</span><span class="sxs-lookup"><span data-stu-id="7f5eb-127">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




