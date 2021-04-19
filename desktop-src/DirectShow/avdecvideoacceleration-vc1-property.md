---
description: 啟用或停用 VC-1 video 解碼的硬體加速。
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: 'AVDecVideoAcceleration_VC1 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970088"
---
# <a name="avdecvideoacceleration_vc1-property"></a><span data-ttu-id="2f249-103">AVDecVideoAcceleration \_ VC1 屬性</span><span class="sxs-lookup"><span data-stu-id="2f249-103">AVDecVideoAcceleration\_VC1 property</span></span>

<span data-ttu-id="2f249-104">啟用或停用 VC-1 video 解碼的硬體加速。</span><span class="sxs-lookup"><span data-stu-id="2f249-104">Enables or disables hardware acceleration for VC-1 video decoding.</span></span>

<span data-ttu-id="2f249-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f249-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2f249-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="2f249-106">Data type</span></span>

<span data-ttu-id="2f249-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="2f249-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2f249-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="2f249-108">Property GUID</span></span>

<span data-ttu-id="2f249-109">**CODECAPI \_ AVDecVideoAcceleration \_ VC1**</span><span class="sxs-lookup"><span data-stu-id="2f249-109">**CODECAPI\_AVDecVideoAcceleration\_VC1**</span></span>

## <a name="remarks"></a><span data-ttu-id="2f249-110">備註</span><span class="sxs-lookup"><span data-stu-id="2f249-110">Remarks</span></span>

<span data-ttu-id="2f249-111">如果值為零，則此解碼器不會使用 DirectX Video 加速 (DXVA) 進行 VC-1 的影片解碼。</span><span class="sxs-lookup"><span data-stu-id="2f249-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for VC-1 video decoding.</span></span> <span data-ttu-id="2f249-112">針對 DirectShow 篩選器，請在配置解碼器的輸出連接之前設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2f249-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f249-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f249-113">Requirements</span></span>



| <span data-ttu-id="2f249-114">需求</span><span class="sxs-lookup"><span data-stu-id="2f249-114">Requirement</span></span> | <span data-ttu-id="2f249-115">值</span><span class="sxs-lookup"><span data-stu-id="2f249-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f249-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f249-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f249-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f249-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2f249-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f249-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f249-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f249-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2f249-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2f249-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f249-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f249-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f249-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f249-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f249-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="2f249-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2f249-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="2f249-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




