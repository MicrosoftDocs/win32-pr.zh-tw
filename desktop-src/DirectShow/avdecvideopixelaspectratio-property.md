---
description: 指定已解碼影片資料流程的圖元外觀比例。
ms.assetid: 07689d15-3e46-45f7-bdd5-ae51308ddbce
title: 'AVDecVideoPixelAspectRatio 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ce01fbe8d8e7992b35265a67f1833ae41bdde2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935795"
---
# <a name="avdecvideopixelaspectratio-property"></a><span data-ttu-id="2d8bf-103">AVDecVideoPixelAspectRatio 屬性</span><span class="sxs-lookup"><span data-stu-id="2d8bf-103">AVDecVideoPixelAspectRatio property</span></span>

<span data-ttu-id="2d8bf-104">指定已解碼影片資料流程的圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="2d8bf-104">Specifies the pixel aspect ratio of the decoded video stream.</span></span>

<span data-ttu-id="2d8bf-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="2d8bf-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="2d8bf-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="2d8bf-106">Data type</span></span>

<span data-ttu-id="2d8bf-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="2d8bf-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2d8bf-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="2d8bf-108">Property GUID</span></span>

<span data-ttu-id="2d8bf-109">**CODECAPI \_ AVDecVideoPixelAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-109">**CODECAPI\_AVDecVideoPixelAspectRatio**</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8bf-110">備註</span><span class="sxs-lookup"><span data-stu-id="2d8bf-110">Remarks</span></span>

<span data-ttu-id="2d8bf-111">值的上層16位包含寬度，而較低的16位則包含高度。</span><span class="sxs-lookup"><span data-stu-id="2d8bf-111">The upper 16 bits of the value contain the width, and the lower 16 bits contain the height.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d8bf-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d8bf-112">Requirements</span></span>



| <span data-ttu-id="2d8bf-113">需求</span><span class="sxs-lookup"><span data-stu-id="2d8bf-113">Requirement</span></span> | <span data-ttu-id="2d8bf-114">值</span><span class="sxs-lookup"><span data-stu-id="2d8bf-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8bf-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d8bf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2d8bf-116">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d8bf-116">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2d8bf-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d8bf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2d8bf-118">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d8bf-118">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2d8bf-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2d8bf-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d8bf-120"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d8bf-120"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d8bf-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d8bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d8bf-122">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="2d8bf-122">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2d8bf-123">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-123">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




