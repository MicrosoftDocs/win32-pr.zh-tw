---
description: 描述 MPEG-2 傳輸串流內的基本資料流程內容。 此列舉會在 IMPEG2PIDMap 介面中使用，此介面會在 MPEG-2 信號的輸出針腳上執行。
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: 'MEDIA_SAMPLE_CONTENT 列舉 (Bdatypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998741"
---
# <a name="media_sample_content-enumeration"></a><span data-ttu-id="bdb55-104">媒體 \_ 範例 \_ 內容列舉</span><span class="sxs-lookup"><span data-stu-id="bdb55-104">MEDIA\_SAMPLE\_CONTENT enumeration</span></span>

<span data-ttu-id="bdb55-105">描述 MPEG-2 傳輸串流內的基本資料流程內容。</span><span class="sxs-lookup"><span data-stu-id="bdb55-105">Describes the contents of an elementary stream within an MPEG-2 transport stream.</span></span> <span data-ttu-id="bdb55-106">此列舉會在 [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) 介面中使用，此介面會在 [mpeg-2 信號](mpeg-2-demultiplexer.md)的輸出針腳上執行。</span><span class="sxs-lookup"><span data-stu-id="bdb55-106">This enumeration is used in the [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb55-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb55-107">Syntax</span></span>


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a><span data-ttu-id="bdb55-108">常數</span><span class="sxs-lookup"><span data-stu-id="bdb55-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bdb55-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**媒體 \_ 傳輸封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="bdb55-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**</span></span>
</dt> <dd>

<span data-ttu-id="bdb55-110">指定要在不處理的情況下傳遞的完整傳輸資料流程封包。</span><span class="sxs-lookup"><span data-stu-id="bdb55-110">Specifies a complete transport stream packet to be passed through without processing.</span></span>

</dd> <dt>

<span data-ttu-id="bdb55-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**媒體 \_ 基本 \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="bdb55-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**</span></span>
</dt> <dd>

<span data-ttu-id="bdb55-112">指定音訊或影片 PE 裝載。</span><span class="sxs-lookup"><span data-stu-id="bdb55-112">Specifies an audio or video PES payload.</span></span>

</dd> <dt>

<span data-ttu-id="bdb55-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**媒體 \_ MPEG2 \_ PSI**</span><span class="sxs-lookup"><span data-stu-id="bdb55-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**</span></span>
</dt> <dd>

<span data-ttu-id="bdb55-114">指定 PAT、PMT、CAT 或私用資料流程。</span><span class="sxs-lookup"><span data-stu-id="bdb55-114">Specifies a PAT, PMT, CAT, or Private data stream.</span></span> <span data-ttu-id="bdb55-115">這些是完全不需要重組的 PSI 區段。</span><span class="sxs-lookup"><span data-stu-id="bdb55-115">These are complete PSI sections which do not need to be reassembled.</span></span>

</dd> <dt>

<span data-ttu-id="bdb55-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**媒體 \_ 傳輸 \_ 承載**</span><span class="sxs-lookup"><span data-stu-id="bdb55-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="bdb55-117">指定收集的 TS 封包承載，例如 PE 封包。</span><span class="sxs-lookup"><span data-stu-id="bdb55-117">Specifies gathered TS packet payloads, such as PES packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdb55-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdb55-118">Requirements</span></span>



| <span data-ttu-id="bdb55-119">需求</span><span class="sxs-lookup"><span data-stu-id="bdb55-119">Requirement</span></span> | <span data-ttu-id="bdb55-120">值</span><span class="sxs-lookup"><span data-stu-id="bdb55-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb55-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bdb55-121">Header</span></span><br/> | <dl> <span data-ttu-id="bdb55-122"><dt>Bdatypes (包含 Bdaiface) </dt></span><span class="sxs-lookup"><span data-stu-id="bdb55-122"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb55-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdb55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb55-124">DirectShow 列舉類型</span><span class="sxs-lookup"><span data-stu-id="bdb55-124">DirectShow Enumerated Types</span></span>](directshow-enumerated-types.md)
</dt> </dl>

 

 




