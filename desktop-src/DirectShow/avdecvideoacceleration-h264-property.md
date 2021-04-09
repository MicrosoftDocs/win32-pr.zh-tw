---
description: 啟用或停用 h.264 影片解碼的硬體加速。
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: 'AVDecVideoAcceleration_H264 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846680"
---
# <a name="avdecvideoacceleration_h264-property"></a><span data-ttu-id="d6111-103">AVDecVideoAcceleration \_ H264 屬性</span><span class="sxs-lookup"><span data-stu-id="d6111-103">AVDecVideoAcceleration\_H264 property</span></span>

<span data-ttu-id="d6111-104">啟用或停用 h.264 影片解碼的硬體加速。</span><span class="sxs-lookup"><span data-stu-id="d6111-104">Enables or disables hardware acceleration for H.264 video decoding.</span></span>

<span data-ttu-id="d6111-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d6111-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6111-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="d6111-106">Data type</span></span>

<span data-ttu-id="d6111-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="d6111-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d6111-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="d6111-108">Property GUID</span></span>

<span data-ttu-id="d6111-109">**CODECAPI \_ AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="d6111-109">**CODECAPI\_AVDecVideoAcceleration\_H264**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6111-110">備註</span><span class="sxs-lookup"><span data-stu-id="d6111-110">Remarks</span></span>

<span data-ttu-id="d6111-111">如果值為零，則不會使用 DirectX Video 加速 (DXVA) 進行 h.264 影片解碼。</span><span class="sxs-lookup"><span data-stu-id="d6111-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for H.264 video decoding.</span></span> <span data-ttu-id="d6111-112">針對 DirectShow 篩選器，請在配置解碼器的輸出連接之前設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d6111-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6111-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6111-113">Requirements</span></span>



| <span data-ttu-id="d6111-114">需求</span><span class="sxs-lookup"><span data-stu-id="d6111-114">Requirement</span></span> | <span data-ttu-id="d6111-115">值</span><span class="sxs-lookup"><span data-stu-id="d6111-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6111-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6111-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d6111-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6111-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d6111-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6111-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d6111-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6111-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d6111-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d6111-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6111-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6111-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6111-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6111-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6111-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="d6111-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d6111-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="d6111-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




