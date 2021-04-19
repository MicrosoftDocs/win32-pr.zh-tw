---
description: 設定要送入編碼器的影片畫面最大即時輸入速率。
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: 'CODECAPI_AVEncMaxFrameRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970560"
---
# <a name="codecapi_avencmaxframerate-property"></a><span data-ttu-id="11ba4-103">CODECAPI \_ AVEncMaxFrameRate 屬性</span><span class="sxs-lookup"><span data-stu-id="11ba4-103">CODECAPI\_AVEncMaxFrameRate property</span></span>

<span data-ttu-id="11ba4-104">設定要送入編碼器的影片畫面最大即時輸入速率。</span><span class="sxs-lookup"><span data-stu-id="11ba4-104">Sets the maximum real-time input rate of video frames being fed to the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="11ba4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="11ba4-105">Data type</span></span>

<span data-ttu-id="11ba4-106">**ULONGULONG** (VT \_ UI8) </span><span class="sxs-lookup"><span data-stu-id="11ba4-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="11ba4-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="11ba4-107">Property GUID</span></span>

<span data-ttu-id="11ba4-108">**CODECAPI \_ AVEncMaxFrameRate**</span><span class="sxs-lookup"><span data-stu-id="11ba4-108">**CODECAPI\_AVEncMaxFrameRate**</span></span>

## <a name="remarks"></a><span data-ttu-id="11ba4-109">備註</span><span class="sxs-lookup"><span data-stu-id="11ba4-109">Remarks</span></span>

<span data-ttu-id="11ba4-110">這個屬性可讓呼叫者指定將影片畫面送入編碼器的最大即時輸入速率。</span><span class="sxs-lookup"><span data-stu-id="11ba4-110">This property allows the caller to specify the maximum real-time input rate of video frames being fed to the encoder.</span></span> <span data-ttu-id="11ba4-111">這可讓編碼器指出處理傳入畫面所需的速率。</span><span class="sxs-lookup"><span data-stu-id="11ba4-111">This gives the encoder an indication of the rate that it will need to process the incoming frames.</span></span> <span data-ttu-id="11ba4-112">這對於根據來源影片的解析度和畫面播放速率，將本身設為特定電源狀態設定的編碼器很有用。</span><span class="sxs-lookup"><span data-stu-id="11ba4-112">This is useful for encoders that set themselves into a particular power state configuration based on the resolution and frame-rate of the source video.</span></span>

<span data-ttu-id="11ba4-113">畫面播放速率以比例表示。</span><span class="sxs-lookup"><span data-stu-id="11ba4-113">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="11ba4-114">屬性值的上方32位包含分子，而較低的32位則包含分母。</span><span class="sxs-lookup"><span data-stu-id="11ba4-114">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="11ba4-115">例如，如果畫面播放速率是每秒30個畫面格 (fps) ，則比率為30/1。</span><span class="sxs-lookup"><span data-stu-id="11ba4-115">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="11ba4-116">如果畫面播放速率是 29.97 fps，則比率為 30000/1001。</span><span class="sxs-lookup"><span data-stu-id="11ba4-116">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ba4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="11ba4-117">Requirements</span></span>



| <span data-ttu-id="11ba4-118">需求</span><span class="sxs-lookup"><span data-stu-id="11ba4-118">Requirement</span></span> | <span data-ttu-id="11ba4-119">值</span><span class="sxs-lookup"><span data-stu-id="11ba4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11ba4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11ba4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11ba4-121">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11ba4-121">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11ba4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11ba4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11ba4-123">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11ba4-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11ba4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="11ba4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="11ba4-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="11ba4-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ba4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11ba4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ba4-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="11ba4-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="11ba4-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="11ba4-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

