---
description: 傳回已編碼的影片框架數目。
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: 'AVEncStatVideoCodedFrames 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109372"
---
# <a name="avencstatvideocodedframes-property"></a><span data-ttu-id="ed892-103">AVEncStatVideoCodedFrames 屬性</span><span class="sxs-lookup"><span data-stu-id="ed892-103">AVEncStatVideoCodedFrames property</span></span>

<span data-ttu-id="ed892-104">傳回已編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="ed892-104">Returns the number of video frames that were encoded.</span></span>

<span data-ttu-id="ed892-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ed892-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ed892-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="ed892-106">Data type</span></span>

<span data-ttu-id="ed892-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="ed892-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ed892-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="ed892-108">Property GUID</span></span>

<span data-ttu-id="ed892-109">**CODECAPI \_ AVEncStatVideoCodedFrames**</span><span class="sxs-lookup"><span data-stu-id="ed892-109">**CODECAPI\_AVEncStatVideoCodedFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="ed892-110">備註</span><span class="sxs-lookup"><span data-stu-id="ed892-110">Remarks</span></span>

<span data-ttu-id="ed892-111">編碼完成之後，就可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ed892-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="ed892-112">這個屬性的值等於 [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) 屬性減去捨棄的框架數目。</span><span class="sxs-lookup"><span data-stu-id="ed892-112">The value of this property is equal to the [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) property minus the number of dropped frames.</span></span> <span data-ttu-id="ed892-113">編碼器可能會捨棄框架，以保持在指定的位速率條件約束內。</span><span class="sxs-lookup"><span data-stu-id="ed892-113">The encoder might drop frames to stay within the specified bit rate constraints.</span></span> <span data-ttu-id="ed892-114">它也可能會捨棄資料流程結尾的框架 (請參閱 [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="ed892-114">It might also drop frames at the end of the stream (see [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) property).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed892-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed892-115">Requirements</span></span>



| <span data-ttu-id="ed892-116">需求</span><span class="sxs-lookup"><span data-stu-id="ed892-116">Requirement</span></span> | <span data-ttu-id="ed892-117">值</span><span class="sxs-lookup"><span data-stu-id="ed892-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed892-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed892-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ed892-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed892-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ed892-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed892-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ed892-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed892-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ed892-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ed892-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed892-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed892-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed892-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed892-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed892-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="ed892-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ed892-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="ed892-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




