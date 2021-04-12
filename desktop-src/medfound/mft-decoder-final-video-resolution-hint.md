---
description: 指定在視頻處理之後，解碼影像的最終輸出解析度。
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: 'MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191780"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a><span data-ttu-id="f32dc-103">MFT \_ 解碼器 \_ 最終 \_ 影片 \_ 解析 \_ 提示屬性</span><span class="sxs-lookup"><span data-stu-id="f32dc-103">MFT\_DECODER\_FINAL\_VIDEO\_RESOLUTION\_HINT attribute</span></span>

<span data-ttu-id="f32dc-104">指定在視頻處理之後，解碼影像的最終輸出解析度。</span><span class="sxs-lookup"><span data-stu-id="f32dc-104">Specifies the final output resolution of the decoded image, after video processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="f32dc-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f32dc-105">Data type</span></span>

<span data-ttu-id="f32dc-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f32dc-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="f32dc-107">備註</span><span class="sxs-lookup"><span data-stu-id="f32dc-107">Remarks</span></span>

<span data-ttu-id="f32dc-108">部分影片解碼器支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="f32dc-108">This attribute is supported by some video decoders.</span></span> <span data-ttu-id="f32dc-109">應用程式可以設定此屬性，以指出影片處理之後影像的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="f32dc-109">An application can set this attribute to indicate the width and height of the image after video processing.</span></span> <span data-ttu-id="f32dc-110">您可以使用這項資訊來優化解碼程式，特別是如果最終的映射大小遠小於原生映射大小。</span><span class="sxs-lookup"><span data-stu-id="f32dc-110">The decoder can use this information to optimize the decoding process, especially if the final image size is much smaller than the native image size.</span></span> <span data-ttu-id="f32dc-111">例如，此解碼器可能會略過迴圈式篩選。</span><span class="sxs-lookup"><span data-stu-id="f32dc-111">For example, the decoder might skip an out-of-loop filter.</span></span>

<span data-ttu-id="f32dc-112">上方的32位包含寬度，而較低的32位則包含高度。</span><span class="sxs-lookup"><span data-stu-id="f32dc-112">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="f32dc-113">若要設定此屬性：</span><span class="sxs-lookup"><span data-stu-id="f32dc-113">To set this attribute:</span></span>

1.  <span data-ttu-id="f32dc-114">在解碼器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="f32dc-114">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="f32dc-115">呼叫 [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) 以加入屬性。</span><span class="sxs-lookup"><span data-stu-id="f32dc-115">Call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="f32dc-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f32dc-116">Requirements</span></span>



| <span data-ttu-id="f32dc-117">需求</span><span class="sxs-lookup"><span data-stu-id="f32dc-117">Requirement</span></span> | <span data-ttu-id="f32dc-118">值</span><span class="sxs-lookup"><span data-stu-id="f32dc-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32dc-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f32dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f32dc-120">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f32dc-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f32dc-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f32dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f32dc-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="f32dc-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f32dc-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f32dc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f32dc-124"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="f32dc-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32dc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f32dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32dc-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f32dc-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f32dc-127">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="f32dc-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




