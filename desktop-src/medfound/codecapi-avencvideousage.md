---
description: 設定影片編碼器的影片使用方式。
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: 'CODECAPI_AVEncVideoUsage 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970558"
---
# <a name="codecapi_avencvideousage-property"></a><span data-ttu-id="8eac9-103">CODECAPI \_ AVEncVideoUsage 屬性</span><span class="sxs-lookup"><span data-stu-id="8eac9-103">CODECAPI\_AVEncVideoUsage property</span></span>

<span data-ttu-id="8eac9-104">設定影片編碼器的影片使用方式。</span><span class="sxs-lookup"><span data-stu-id="8eac9-104">Sets the video usage for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="8eac9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8eac9-105">Data type</span></span>

<span data-ttu-id="8eac9-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="8eac9-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="8eac9-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="8eac9-107">Property GUID</span></span>

<span data-ttu-id="8eac9-108">**CODECAPI \_ AVEncVideoUsage**</span><span class="sxs-lookup"><span data-stu-id="8eac9-108">**CODECAPI\_AVEncVideoUsage**</span></span>

## <a name="remarks"></a><span data-ttu-id="8eac9-109">備註</span><span class="sxs-lookup"><span data-stu-id="8eac9-109">Remarks</span></span>

<span data-ttu-id="8eac9-110">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="8eac9-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="8eac9-111">[CODECAPI \_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md)、CODECAPI \_ AVEncVideoUsage 和 [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) 是靜態編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="8eac9-111">[CODECAPI\_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI\_AVEncVideoUsage, and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="8eac9-112">一旦設定之後，只有在相機的輸出 pin 上呼叫設定媒體類型之後，才會生效。</span><span class="sxs-lookup"><span data-stu-id="8eac9-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eac9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8eac9-113">Requirements</span></span>



| <span data-ttu-id="8eac9-114">需求</span><span class="sxs-lookup"><span data-stu-id="8eac9-114">Requirement</span></span> | <span data-ttu-id="8eac9-115">值</span><span class="sxs-lookup"><span data-stu-id="8eac9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8eac9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8eac9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8eac9-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8eac9-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="8eac9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8eac9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8eac9-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8eac9-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8eac9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8eac9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eac9-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8eac9-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eac9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8eac9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eac9-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="8eac9-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

