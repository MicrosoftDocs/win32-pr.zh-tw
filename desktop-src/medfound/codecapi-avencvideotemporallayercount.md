---
description: 設定影片編碼器的影片時態圖層計數。
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: 'CODECAPI_AVEncVideoTemporalLayerCount 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468644"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a><span data-ttu-id="6ff25-103">CODECAPI \_ AVEncVideoTemporalLayerCount 屬性</span><span class="sxs-lookup"><span data-stu-id="6ff25-103">CODECAPI\_AVEncVideoTemporalLayerCount property</span></span>

<span data-ttu-id="6ff25-104">設定影片編碼器的影片時態圖層計數。</span><span class="sxs-lookup"><span data-stu-id="6ff25-104">Sets the video temporal layer count for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ff25-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6ff25-105">Data type</span></span>

<span data-ttu-id="6ff25-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="6ff25-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="6ff25-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="6ff25-107">Property GUID</span></span>

<span data-ttu-id="6ff25-108">**CODECAPI \_ AVEncVideoTemporalLayerCount**</span><span class="sxs-lookup"><span data-stu-id="6ff25-108">**CODECAPI\_AVEncVideoTemporalLayerCount**</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff25-109">備註</span><span class="sxs-lookup"><span data-stu-id="6ff25-109">Remarks</span></span>

<span data-ttu-id="6ff25-110">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="6ff25-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="6ff25-111">CODECAPI \_ AVEncVideoTemporalLayerCount、 [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)和 [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) 是靜態編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="6ff25-111">CODECAPI\_AVEncVideoTemporalLayerCount, [CODECAPI\_AVEncVideoUsage](codecapi-avencvideousage.md), and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="6ff25-112">一旦設定之後，只有在相機的輸出 pin 上呼叫設定媒體類型之後，才會生效。</span><span class="sxs-lookup"><span data-stu-id="6ff25-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff25-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ff25-113">Requirements</span></span>



| <span data-ttu-id="6ff25-114">需求</span><span class="sxs-lookup"><span data-stu-id="6ff25-114">Requirement</span></span> | <span data-ttu-id="6ff25-115">值</span><span class="sxs-lookup"><span data-stu-id="6ff25-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff25-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ff25-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff25-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ff25-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="6ff25-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ff25-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff25-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ff25-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6ff25-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6ff25-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ff25-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ff25-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff25-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ff25-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff25-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="6ff25-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

