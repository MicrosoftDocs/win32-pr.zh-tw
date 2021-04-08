---
description: 指定目前的框架使用一或多個 LTR 框架進行編碼。
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: 'CODECAPI_AVEncVideoUseLTRFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689355"
---
# <a name="codecapi_avencvideouseltrframe-property"></a><span data-ttu-id="13b18-103">CODECAPI \_ AVEncVideoUseLTRFrame 屬性</span><span class="sxs-lookup"><span data-stu-id="13b18-103">CODECAPI\_AVEncVideoUseLTRFrame property</span></span>

<span data-ttu-id="13b18-104">指定目前的框架使用一或多個 LTR 框架進行編碼。</span><span class="sxs-lookup"><span data-stu-id="13b18-104">Specifies that the current frame is encoded using one or multiple LTR frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="13b18-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="13b18-105">Data type</span></span>

<span data-ttu-id="13b18-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="13b18-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="13b18-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="13b18-107">Property GUID</span></span>

<span data-ttu-id="13b18-108">**CODECAPI \_ AVEncVideoUseLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="13b18-108">**CODECAPI\_AVEncVideoUseLTRFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="13b18-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="13b18-109">Property value</span></span>

<span data-ttu-id="13b18-110">此控制項的值包含兩個欄位，其中每個欄位都有16個位。</span><span class="sxs-lookup"><span data-stu-id="13b18-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13b18-111">值</span><span class="sxs-lookup"><span data-stu-id="13b18-111">Value</span></span></th>
<th><span data-ttu-id="13b18-112">意義</span><span class="sxs-lookup"><span data-stu-id="13b18-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="13b18-113"><dt><strong>第一個欄位</strong></dt><dt>位 [0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="13b18-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="13b18-114">指出哪些 LTR 框架 (s) 允許編碼目前的框架。</span><span class="sxs-lookup"><span data-stu-id="13b18-114">Indicates which LTR frame(s) are allowed for encoding the current frame.</span></span> <br/> <span data-ttu-id="13b18-115"><strong>H.264/AVC 編碼器：</strong></span><span class="sxs-lookup"><span data-stu-id="13b18-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="13b18-116">這是表示可以使用哪些 LTR 框架做為此框架參考的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="13b18-116">This is a bitmap that indicates which LTR frames can be used as a reference for this frame.</span></span> <span data-ttu-id="13b18-117">最不重要的位會對應到 LTR 索引0，第二個最小的位則對應到 LTR 索引1等等。</span><span class="sxs-lookup"><span data-stu-id="13b18-117">The least significant bit corresponds to LTR index 0, the second least significant bit corresponds to LTR index 1, etc.</span></span><br/> <span data-ttu-id="13b18-118">此值不得為0。</span><span class="sxs-lookup"><span data-stu-id="13b18-118">This value shall not be 0.</span></span><br/> <span data-ttu-id="13b18-119">此值指定的最高索引不能大於 <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> 屬性中指定的 LTR 框架數目上限。</span><span class="sxs-lookup"><span data-stu-id="13b18-119">The highest index specified by this value shall not be greater than the maximum number of LTR frames specified in the <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> property less one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="13b18-120"><dt><strong>第二個欄位</strong></dt><dt>位 [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="13b18-120"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="13b18-121">指出編碼後續框架是否需要額外限制的旗標。</span><span class="sxs-lookup"><span data-stu-id="13b18-121">Flag that indicates whether additional limitations are required for encoding subsequent frames.</span></span> <br/> <span data-ttu-id="13b18-122"><strong>H.264/AVC 編碼器：</strong></span><span class="sxs-lookup"><span data-stu-id="13b18-122"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="13b18-123">1是在此欄位唯一有效的值。</span><span class="sxs-lookup"><span data-stu-id="13b18-123">1 is on the only valid value for this field.</span></span> <span data-ttu-id="13b18-124">所有其他值都無效，並保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="13b18-124">All other values are invalid and reserved for future use.</span></span><br/> <span data-ttu-id="13b18-125">當旗標為1時，編碼器應該依照下列條件約束，編碼編碼順序中的後續框架：</span><span class="sxs-lookup"><span data-stu-id="13b18-125">When the flag is 1, the encoder shall encode subsequent frames in encoding order subject to the following constraints:</span></span><br/>
<ul>
<li><span data-ttu-id="13b18-126">它不應使用比目前框架更舊的編碼順序或編碼順序中未來編碼的短期參考框架。</span><span class="sxs-lookup"><span data-stu-id="13b18-126">It shall not use short term reference frames in encoding order older than the current frame or future encoding in encoding order.</span></span></li>
<li><span data-ttu-id="13b18-127">它不應該使用最近 CODECAPI_AVEncVideoUseLTRFrame 控制項未描述的 LTR 框架。</span><span class="sxs-lookup"><span data-stu-id="13b18-127">It shall not use LTR frames not described by the most recent CODECAPI_AVEncVideoUseLTRFrame control.</span></span></li>
<li><span data-ttu-id="13b18-128">它可能會使用目前框架之後更新的 LTR 框架。</span><span class="sxs-lookup"><span data-stu-id="13b18-128">It may use LTR frames updated after the current frame.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="13b18-129">備註</span><span class="sxs-lookup"><span data-stu-id="13b18-129">Remarks</span></span>

<span data-ttu-id="13b18-130">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="13b18-130">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="13b18-131">如果使用 CODECAPI AVEncVideoUseLTRFrame 屬性發出了暫止的呼叫， \_ 但編碼器尚未產生使用 ltr 的框架，就不應呼叫這個屬性。</span><span class="sxs-lookup"><span data-stu-id="13b18-131">This property should not be called if a pending call to use an LTR frame has been issued using the CODECAPI\_AVEncVideoUseLTRFrame property and the encoder has not yet generated a frame that has used the LTR.</span></span> <span data-ttu-id="13b18-132">換句話說，編碼器不應將 CODECAPI AVEncVideoUseLTRFrame 要求排入佇列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="13b18-132">In other words, the encoder should not queue up CODECAPI\_AVEncVideoUseLTRFrame requests.</span></span>

<span data-ttu-id="13b18-133">如果在 \_ 其他 CODECAPI AVEncVideoUseLTRFrame 要求仍在擱置中時提交 CODECAPI AVEncVideoUseLTRFrame 要求 \_ ，則應捨棄較舊的要求。</span><span class="sxs-lookup"><span data-stu-id="13b18-133">If a CODECAPI\_AVEncVideoUseLTRFrame request is submitted while another CODECAPI\_AVEncVideoUseLTRFrame request is still pending, then the older request should be dropped.</span></span>

<span data-ttu-id="13b18-134">\_在非基底分層框架上呼叫 CODECAPI AVEncVideoUseLTRFrame 是有效的，而且應該套用至非基底分層框架，而不會延遲基底圖層框架。</span><span class="sxs-lookup"><span data-stu-id="13b18-134">Calling CODECAPI\_AVEncVideoUseLTRFrame on a non-base layer frame is valid and shall apply to the non-base layer frame, without delay to a base layer frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b18-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="13b18-135">Requirements</span></span>



| <span data-ttu-id="13b18-136">需求</span><span class="sxs-lookup"><span data-stu-id="13b18-136">Requirement</span></span> | <span data-ttu-id="13b18-137">值</span><span class="sxs-lookup"><span data-stu-id="13b18-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13b18-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13b18-138">Minimum supported client</span></span><br/> | <span data-ttu-id="13b18-139">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13b18-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="13b18-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13b18-140">Minimum supported server</span></span><br/> | <span data-ttu-id="13b18-141">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13b18-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="13b18-142">標頭</span><span class="sxs-lookup"><span data-stu-id="13b18-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="13b18-143"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="13b18-143"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b18-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13b18-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b18-145">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="13b18-145">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




