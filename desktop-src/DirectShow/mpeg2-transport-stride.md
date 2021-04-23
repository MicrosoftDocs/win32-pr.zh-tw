---
description: MPEG2 \_ 傳輸 \_ STRIDE 結構說明 mpeg-2 傳輸串流 (TS) 封包的格式。
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: 'MPEG2_TRANSPORT_STRIDE 結構 (Bdatypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908486"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="aa131-103">MPEG2 \_ 傳輸 \_ STRIDE 結構</span><span class="sxs-lookup"><span data-stu-id="aa131-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="aa131-104">`MPEG2_TRANSPORT_STRIDE`結構描述 mpeg-2 傳輸串流 (TS) 封包的格式。</span><span class="sxs-lookup"><span data-stu-id="aa131-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="aa131-105">此結構允許傳輸資料流程，其中188位元組傳輸封包不是連續的。</span><span class="sxs-lookup"><span data-stu-id="aa131-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="aa131-106">基於本檔的目的，這類封包稱為 stride 封 *包*。</span><span class="sxs-lookup"><span data-stu-id="aa131-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="aa131-107">Stride 封包是由下列媒體類型來識別：</span><span class="sxs-lookup"><span data-stu-id="aa131-107">Stride packets are identified by the following media type:</span></span>



| <span data-ttu-id="aa131-108">標籤</span><span class="sxs-lookup"><span data-stu-id="aa131-108">Label</span></span> | <span data-ttu-id="aa131-109">值</span><span class="sxs-lookup"><span data-stu-id="aa131-109">Value</span></span> |
|-------------|----------------------------------------|
| <span data-ttu-id="aa131-110">主要類型</span><span class="sxs-lookup"><span data-stu-id="aa131-110">Major Type</span></span>  | <span data-ttu-id="aa131-111">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="aa131-111">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="aa131-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="aa131-112">Subtype</span></span>     | <span data-ttu-id="aa131-113">MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="aa131-113">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="aa131-114">格式類型</span><span class="sxs-lookup"><span data-stu-id="aa131-114">Format Type</span></span> | <span data-ttu-id="aa131-115">格式化 \_ 無</span><span class="sxs-lookup"><span data-stu-id="aa131-115">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="aa131-116">格式區塊 (**pbFormat**) 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="aa131-116">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="aa131-117">如果包含格式區塊，則必須以 **MPEG2 \_ 傳輸 \_ STRIDE** 結構作為開頭。</span><span class="sxs-lookup"><span data-stu-id="aa131-117">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="aa131-118">此結構會定義 stride 封包內傳輸封包的版面配置。</span><span class="sxs-lookup"><span data-stu-id="aa131-118">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="aa131-119">如果格式區塊為 **Null**，則會假設封包使用一組預設值;如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="aa131-119">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa131-120">語法</span><span class="sxs-lookup"><span data-stu-id="aa131-120">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="aa131-121">成員</span><span class="sxs-lookup"><span data-stu-id="aa131-121">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa131-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="aa131-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="aa131-123">指定從封包開頭到內嵌傳輸封包第一個位元組的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aa131-123">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="aa131-124">值的範圍必須介於零到 `(dwStride - dwPacketLength)` （含）之間。</span><span class="sxs-lookup"><span data-stu-id="aa131-124">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="aa131-125">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="aa131-125">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="aa131-126">指定內嵌傳輸封包的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aa131-126">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="aa131-127">若為標準的 MPEG-2 傳輸封包，此值必須為188個位元組。</span><span class="sxs-lookup"><span data-stu-id="aa131-127">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aa131-128">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="aa131-128">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="aa131-129">指定整個 stride 封包的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aa131-129">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="aa131-130">值必須至少為 `(dwOffset + dwPacketLength)` 。</span><span class="sxs-lookup"><span data-stu-id="aa131-130">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa131-131">備註</span><span class="sxs-lookup"><span data-stu-id="aa131-131">Remarks</span></span>

<span data-ttu-id="aa131-132">下圖說明結構成員之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="aa131-132">The following diagram illustrates the relations between the structure members.</span></span>

![mpeg-2 stride 封包](images/mpeg2-stride-packet.png)

<span data-ttu-id="aa131-134">包含多工跨距封包的輸入緩衝區有一些限制：</span><span class="sxs-lookup"><span data-stu-id="aa131-134">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="aa131-135">Stride 封包必須連續封裝在緩衝區內。</span><span class="sxs-lookup"><span data-stu-id="aa131-135">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="aa131-136">第一個 stride 封包之前沒有任何位元組，或遵循最後一個 stride 封包。</span><span class="sxs-lookup"><span data-stu-id="aa131-136">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="aa131-137">緩衝區中的 stride 封包數目必須符合;也就是說，緩衝區長度% dwStride 等於零。</span><span class="sxs-lookup"><span data-stu-id="aa131-137">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="aa131-138">每個緩衝區的 stride 封包數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="aa131-138">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="aa131-139">如果媒體類型不包含格式區塊 (**pbFormat** 為 **Null**) ，則會使用下列預設值：</span><span class="sxs-lookup"><span data-stu-id="aa131-139">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="aa131-140">**dwOffset**：0</span><span class="sxs-lookup"><span data-stu-id="aa131-140">**dwOffset**: 0</span></span>
-   <span data-ttu-id="aa131-141">**dwPacketLength**：188</span><span class="sxs-lookup"><span data-stu-id="aa131-141">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="aa131-142">**dwStride**：188</span><span class="sxs-lookup"><span data-stu-id="aa131-142">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="aa131-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa131-143">Requirements</span></span>



| <span data-ttu-id="aa131-144">需求</span><span class="sxs-lookup"><span data-stu-id="aa131-144">Requirement</span></span> | <span data-ttu-id="aa131-145">值</span><span class="sxs-lookup"><span data-stu-id="aa131-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa131-146">標頭</span><span class="sxs-lookup"><span data-stu-id="aa131-146">Header</span></span><br/> | <dl> <span data-ttu-id="aa131-147"><dt>Bdatypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa131-147"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa131-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa131-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa131-149">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="aa131-149">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="aa131-150">MPEG-2 媒體類型</span><span class="sxs-lookup"><span data-stu-id="aa131-150">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




