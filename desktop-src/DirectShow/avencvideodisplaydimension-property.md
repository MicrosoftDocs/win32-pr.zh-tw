---
description: 指定解碼時影片資料流程的大小。
ms.assetid: db7b101a-5ff8-4a62-b9e2-d05fcdc44b3d
title: 'AVEncVideoDisplayDimension 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e5f611525e68f6f47c442c6e733c6c3e7de14d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967003"
---
# <a name="avencvideodisplaydimension-property"></a><span data-ttu-id="fec44-103">AVEncVideoDisplayDimension 屬性</span><span class="sxs-lookup"><span data-stu-id="fec44-103">AVEncVideoDisplayDimension property</span></span>

<span data-ttu-id="fec44-104">指定解碼時影片資料流程的大小。</span><span class="sxs-lookup"><span data-stu-id="fec44-104">Specifies the size of the video stream when it is decoded.</span></span>

<span data-ttu-id="fec44-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="fec44-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fec44-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="fec44-106">Data type</span></span>

<span data-ttu-id="fec44-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="fec44-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fec44-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="fec44-108">Property GUID</span></span>

<span data-ttu-id="fec44-109">**CODECAPI \_ AVEncVideoDisplayDimension**</span><span class="sxs-lookup"><span data-stu-id="fec44-109">**CODECAPI\_AVEncVideoDisplayDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="fec44-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="fec44-110">Property value</span></span>

<span data-ttu-id="fec44-111">值的上層16位包含寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="fec44-111">The upper 16 bits of the value contain the width, in pixels.</span></span> <span data-ttu-id="fec44-112">較低的16個位包含高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="fec44-112">The lower 16 bits contain the height, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec44-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fec44-113">Requirements</span></span>



| <span data-ttu-id="fec44-114">需求</span><span class="sxs-lookup"><span data-stu-id="fec44-114">Requirement</span></span> | <span data-ttu-id="fec44-115">值</span><span class="sxs-lookup"><span data-stu-id="fec44-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fec44-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fec44-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fec44-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fec44-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fec44-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fec44-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fec44-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fec44-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fec44-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fec44-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fec44-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fec44-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec44-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fec44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec44-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="fec44-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fec44-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="fec44-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




