---
description: 指定應用程式所控制 (LTR) 框架的最大長期參考數目。
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: 'CODECAPI_AVEncVideoLTRBufferControl 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510819"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a><span data-ttu-id="647da-103">CODECAPI \_ AVEncVideoLTRBufferControl 屬性</span><span class="sxs-lookup"><span data-stu-id="647da-103">CODECAPI\_AVEncVideoLTRBufferControl property</span></span>

<span data-ttu-id="647da-104">指定應用程式所控制 (LTR) 框架的最大長期參考數目。</span><span class="sxs-lookup"><span data-stu-id="647da-104">Specifies the maximum number of Long Term Reference (LTR) frames controlled by application.</span></span>

## <a name="data-type"></a><span data-ttu-id="647da-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="647da-105">Data type</span></span>

<span data-ttu-id="647da-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="647da-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="647da-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="647da-107">Property GUID</span></span>

<span data-ttu-id="647da-108">**CODECAPI \_ AVEncVideoLTRBufferControl**</span><span class="sxs-lookup"><span data-stu-id="647da-108">**CODECAPI\_AVEncVideoLTRBufferControl**</span></span>

## <a name="property-value"></a><span data-ttu-id="647da-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="647da-109">Property value</span></span>

<span data-ttu-id="647da-110">此控制項的值包含兩個欄位，其中每個欄位都有16個位。</span><span class="sxs-lookup"><span data-stu-id="647da-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647da-111">值</span><span class="sxs-lookup"><span data-stu-id="647da-111">Value</span></span></th>
<th><span data-ttu-id="647da-112">意義</span><span class="sxs-lookup"><span data-stu-id="647da-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="647da-113"><dt><strong>第一個欄位</strong></dt><dt>位 [0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="647da-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="647da-114">應用程式所控制的 LTR 框架數目。</span><span class="sxs-lookup"><span data-stu-id="647da-114">The number of LTR frames controlled by the application.</span></span><br/> <span data-ttu-id="647da-115"><strong>H.264/AVC 編碼器：</strong></span><span class="sxs-lookup"><span data-stu-id="647da-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="647da-116">假設值為 N 而 N 為非零值，則在每個 IDR 的畫面上，編碼器必須自動將 IDR 框架之後的框架標示 (，並將 IDR 框架) 為 LTR 框架，只要下列全部3項適用：</span><span class="sxs-lookup"><span data-stu-id="647da-116">Assuming the value is N and N is non-zero value, at each IDR frame the encoder must automatically mark the frames following the IDR frame (and including the IDR frame) as LTR frames as long as all 3 of the following apply:</span></span>
<ul>
<li><span data-ttu-id="647da-117">框架尚未設定為標示為長期參考框架。</span><span class="sxs-lookup"><span data-stu-id="647da-117">The frame is not already set to be marked as a long term reference frame.</span></span></li>
<li><span data-ttu-id="647da-118">框架是基底圖層框架。</span><span class="sxs-lookup"><span data-stu-id="647da-118">The frame is a base layer frame.</span></span> <span data-ttu-id="647da-119">例如，語法元素 <strong>temporal_id</strong> 等於0。</span><span class="sxs-lookup"><span data-stu-id="647da-119">For example, syntax element <strong>temporal_id</strong> equal to 0.</span></span></li>
<li><span data-ttu-id="647da-120">目前標示為 LTR 的框架數目小於 N。</span><span class="sxs-lookup"><span data-stu-id="647da-120">The number of frames currently marked as LTR is less than N.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="647da-121"><dt><strong>第二個欄位</strong></dt><dt>位 [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="647da-121"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="647da-122">LTR 控制項的信任模式。</span><span class="sxs-lookup"><span data-stu-id="647da-122">The trust mode of LTR control.</span></span><br/> <span data-ttu-id="647da-123"><strong>H.264/AVC 編碼器：</strong></span><span class="sxs-lookup"><span data-stu-id="647da-123"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="647da-124">1 (信任直到) 表示編碼器可能會使用 LTR 框架，除非應用程式透過 <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> 控制項明確使其失效。</span><span class="sxs-lookup"><span data-stu-id="647da-124">1 (Trust Until) means the encoder may use an LTR frame unless the app explicitly invalidates it through the <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> control.</span></span> <br/> <span data-ttu-id="647da-125">其他值是不正確，並保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="647da-125">Other values are invalid and reserved for future use.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="647da-126">備註</span><span class="sxs-lookup"><span data-stu-id="647da-126">Remarks</span></span>

<span data-ttu-id="647da-127">這是靜態 API。</span><span class="sxs-lookup"><span data-stu-id="647da-127">This is a static API.</span></span>

<span data-ttu-id="647da-128">預設值應為0</span><span class="sxs-lookup"><span data-stu-id="647da-128">Default value shall be 0</span></span>

## <a name="requirements"></a><span data-ttu-id="647da-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="647da-129">Requirements</span></span>



| <span data-ttu-id="647da-130">需求</span><span class="sxs-lookup"><span data-stu-id="647da-130">Requirement</span></span> | <span data-ttu-id="647da-131">值</span><span class="sxs-lookup"><span data-stu-id="647da-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="647da-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="647da-132">Minimum supported client</span></span><br/> | <span data-ttu-id="647da-133">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="647da-133">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="647da-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="647da-134">Minimum supported server</span></span><br/> | <span data-ttu-id="647da-135">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="647da-135">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="647da-136">標頭</span><span class="sxs-lookup"><span data-stu-id="647da-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="647da-137"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="647da-137"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="647da-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="647da-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647da-139">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="647da-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




