---
description: 指定速率控制模式。
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: 'AVEncCommonRateControlMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187554"
---
# <a name="avenccommonratecontrolmode-property"></a><span data-ttu-id="e3013-103">AVEncCommonRateControlMode 屬性</span><span class="sxs-lookup"><span data-stu-id="e3013-103">AVEncCommonRateControlMode property</span></span>

<span data-ttu-id="e3013-104">指定速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="e3013-104">Specifies the rate control mode.</span></span>

<span data-ttu-id="e3013-105">應用程式可以設定此屬性來指定速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="e3013-105">Applications can set this property to specify the rate control mode.</span></span> <span data-ttu-id="e3013-106">編碼器也可以將此屬性作為功能傳回。</span><span class="sxs-lookup"><span data-stu-id="e3013-106">Encoders can also return this property as a capability.</span></span>

<span data-ttu-id="e3013-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3013-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3013-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="e3013-108">Data type</span></span>

<span data-ttu-id="e3013-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="e3013-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e3013-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="e3013-110">Property GUID</span></span>

<span data-ttu-id="e3013-111">**CODECAPI \_ AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="e3013-111">**CODECAPI\_AVEncCommonRateControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="e3013-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e3013-112">Property value</span></span>

<span data-ttu-id="e3013-113">這個屬性的值是 [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="e3013-113">The value of this property is a member of the [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3013-114">備註</span><span class="sxs-lookup"><span data-stu-id="e3013-114">Remarks</span></span>

<span data-ttu-id="e3013-115">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。</span><span class="sxs-lookup"><span data-stu-id="e3013-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="e3013-116">[CODECAPI \_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount)、 [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)和 CODECAPI \_ AVEncCommonRateControlMode 是靜態編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="e3013-116">[CODECAPI\_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI\_AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage), and CODECAPI\_AVEncCommonRateControlMode are static encoder properties.</span></span> <span data-ttu-id="e3013-117">一旦設定之後，只有在相機的輸出圖釘上呼叫設定媒體類型之後，才會生效。</span><span class="sxs-lookup"><span data-stu-id="e3013-117">Once set, these will only take effect after a set media type is called on the camera’s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3013-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3013-118">Requirements</span></span>



| <span data-ttu-id="e3013-119">需求</span><span class="sxs-lookup"><span data-stu-id="e3013-119">Requirement</span></span> | <span data-ttu-id="e3013-120">值</span><span class="sxs-lookup"><span data-stu-id="e3013-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3013-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3013-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3013-122">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3013-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e3013-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3013-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3013-124">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3013-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e3013-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e3013-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3013-126"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3013-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3013-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3013-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3013-128">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="e3013-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e3013-129">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="e3013-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

