---
description: 指定適用于影片編碼 (QP) 的量化參數。
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: 'CODECAPI_AVEncVideoEncodeQP 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972993"
---
# <a name="codecapi_avencvideoencodeqp-property"></a><span data-ttu-id="9bcd6-103">CODECAPI \_ AVEncVideoEncodeQP 屬性</span><span class="sxs-lookup"><span data-stu-id="9bcd6-103">CODECAPI\_AVEncVideoEncodeQP property</span></span>

<span data-ttu-id="9bcd6-104">指定適用于影片編碼 (QP) 的量化參數。</span><span class="sxs-lookup"><span data-stu-id="9bcd6-104">Specifies the quantization parameter (QP) for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="9bcd6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9bcd6-105">Data type</span></span>

<span data-ttu-id="9bcd6-106">**ULONGLONG** (VT \_ UI8) </span><span class="sxs-lookup"><span data-stu-id="9bcd6-106">**ULONGLONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9bcd6-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="9bcd6-107">Property GUID</span></span>

<span data-ttu-id="9bcd6-108">**CODECAPI \_ AVEncVideoEncodeQP**</span><span class="sxs-lookup"><span data-stu-id="9bcd6-108">**CODECAPI\_AVEncVideoEncodeQP**</span></span>

## <a name="property-value"></a><span data-ttu-id="9bcd6-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9bcd6-109">Property value</span></span>

<span data-ttu-id="9bcd6-110">一組 4 16 位欄位，用來以固定的 QP 編碼指定框架 QPs。</span><span class="sxs-lookup"><span data-stu-id="9bcd6-110">A set of four 16-bit fields used to specify the frame QPs in fixed-QP encoding.</span></span>

<span data-ttu-id="9bcd6-111">這些欄位包括：</span><span class="sxs-lookup"><span data-stu-id="9bcd6-111">The fields are:</span></span>

-   <span data-ttu-id="9bcd6-112">Bits 0-15：預設的 QP</span><span class="sxs-lookup"><span data-stu-id="9bcd6-112">Bits 0-15: Default QP</span></span>
-   <span data-ttu-id="9bcd6-113">Bits 16-31：用於 I 框架的 QP</span><span class="sxs-lookup"><span data-stu-id="9bcd6-113">Bits 16-31: QP used for I frames</span></span>
-   <span data-ttu-id="9bcd6-114">Bits 32-47：用於 P 框架的 QP</span><span class="sxs-lookup"><span data-stu-id="9bcd6-114">Bits 32-47: QP used for P frames</span></span>
-   <span data-ttu-id="9bcd6-115">Bits 48-63：用於 B 框架的 QP</span><span class="sxs-lookup"><span data-stu-id="9bcd6-115">Bits 48-63: QP used for B frames</span></span>

## <a name="remarks"></a><span data-ttu-id="9bcd6-116">備註</span><span class="sxs-lookup"><span data-stu-id="9bcd6-116">Remarks</span></span>

<span data-ttu-id="9bcd6-117">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="9bcd6-117">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="9bcd6-118">若要確保不同編碼器之間的一致使用方式，您應該假設編碼器只會查看預設的 QP，並且可以忽略 I/P/B 圖片的 QP 值。</span><span class="sxs-lookup"><span data-stu-id="9bcd6-118">To insure consistent usage across different encoders, you should assume encoders will only look at the default QP and can ignore QP values for I/P/B pictures.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcd6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bcd6-119">Requirements</span></span>



| <span data-ttu-id="9bcd6-120">需求</span><span class="sxs-lookup"><span data-stu-id="9bcd6-120">Requirement</span></span> | <span data-ttu-id="9bcd6-121">值</span><span class="sxs-lookup"><span data-stu-id="9bcd6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcd6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9bcd6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcd6-123">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bcd6-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="9bcd6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9bcd6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcd6-125">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bcd6-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9bcd6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9bcd6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bcd6-127"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bcd6-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcd6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bcd6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcd6-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="9bcd6-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9bcd6-130">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9bcd6-130">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

