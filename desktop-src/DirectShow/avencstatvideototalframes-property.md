---
description: 傳回編碼器收到的影片框架數目。
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: 'AVEncStatVideoTotalFrames 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970282"
---
# <a name="avencstatvideototalframes-property"></a><span data-ttu-id="72b23-103">AVEncStatVideoTotalFrames 屬性</span><span class="sxs-lookup"><span data-stu-id="72b23-103">AVEncStatVideoTotalFrames property</span></span>

<span data-ttu-id="72b23-104">傳回編碼器收到的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="72b23-104">Returns the number of video frames that the encoder received.</span></span>

<span data-ttu-id="72b23-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="72b23-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="72b23-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="72b23-106">Data type</span></span>

<span data-ttu-id="72b23-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="72b23-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="72b23-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="72b23-108">Property GUID</span></span>

<span data-ttu-id="72b23-109">**CODECAPI \_ AVEncStatVideoTotalFrames**</span><span class="sxs-lookup"><span data-stu-id="72b23-109">**CODECAPI\_AVEncStatVideoTotalFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="72b23-110">備註</span><span class="sxs-lookup"><span data-stu-id="72b23-110">Remarks</span></span>

<span data-ttu-id="72b23-111">編碼完成之後，就可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="72b23-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="72b23-112">這個屬性的值是傳送至編碼器的畫面格總數，包括已卸載的框架。</span><span class="sxs-lookup"><span data-stu-id="72b23-112">The value of this property is the total number of frames sent to the encoder, including frames that were dropped.</span></span> <span data-ttu-id="72b23-113">若要取得編碼的框架數目，請閱讀 [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="72b23-113">To get the number of encoded frames, read the [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b23-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="72b23-114">Requirements</span></span>



| <span data-ttu-id="72b23-115">需求</span><span class="sxs-lookup"><span data-stu-id="72b23-115">Requirement</span></span> | <span data-ttu-id="72b23-116">值</span><span class="sxs-lookup"><span data-stu-id="72b23-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72b23-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72b23-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72b23-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72b23-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="72b23-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72b23-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72b23-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72b23-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="72b23-121">標頭</span><span class="sxs-lookup"><span data-stu-id="72b23-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b23-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="72b23-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b23-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72b23-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b23-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="72b23-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="72b23-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="72b23-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




