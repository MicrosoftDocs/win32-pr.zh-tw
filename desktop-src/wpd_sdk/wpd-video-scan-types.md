---
description: WPD \_ 影片 \_ 掃描 \_ 類型列舉類型說明如何編碼影片檔案中的欄位。
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: 'WPD_VIDEO_SCAN_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995186"
---
# <a name="wpd_video_scan_types-enumeration"></a><span data-ttu-id="69306-103">WPD \_ 影片 \_ 掃描 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="69306-103">WPD\_VIDEO\_SCAN\_TYPES enumeration</span></span>

<span data-ttu-id="69306-104">**WPD \_ 影片 \_ 掃描 \_ 類型** 列舉類型說明如何編碼影片檔案中的欄位。</span><span class="sxs-lookup"><span data-stu-id="69306-104">The **WPD\_VIDEO\_SCAN\_TYPES** enumeration type describes how the fields in a video file are encoded.</span></span>

## <a name="syntax"></a><span data-ttu-id="69306-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69306-105">Syntax</span></span>


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="69306-106">常數</span><span class="sxs-lookup"><span data-stu-id="69306-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="69306-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_未使用的 WPD 影片 \_ 掃描 \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="69306-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD\_VIDEO\_SCAN\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="69306-108">尚未為此影片檔案定義掃描類型，或不適用。</span><span class="sxs-lookup"><span data-stu-id="69306-108">The scan type has not been defined for this video file, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="69306-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 漸進式**</span><span class="sxs-lookup"><span data-stu-id="69306-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="69306-110">漸進式掃描影片檔案。</span><span class="sxs-lookup"><span data-stu-id="69306-110">A progressive scan video file.</span></span>

</dd> <dt>

<span data-ttu-id="69306-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 欄位 \_ 交錯 \_ 上方 \_**</span><span class="sxs-lookup"><span data-stu-id="69306-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="69306-112">一種交錯的影片檔案，其中的欄位是替代的，而第) 1 行 (的欄位則是先繪製。</span><span class="sxs-lookup"><span data-stu-id="69306-112">An interleaved video file where the fields alternate and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="69306-113">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="69306-113">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="69306-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_ \_ \_ \_ \_ \_ 先交錯較低 \_ 的 WPD 影片掃描類型欄位**</span><span class="sxs-lookup"><span data-stu-id="69306-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="69306-115">一種交錯的影片檔案，其中的欄位是替代的，而第) 2 行 (的欄位則是先繪製。</span><span class="sxs-lookup"><span data-stu-id="69306-115">An interleaved video file where the fields alternate and the lower field (with line 2) is drawn first.</span></span> <span data-ttu-id="69306-116">如需詳細資訊，請參閱本節後面的「備註」。</span><span class="sxs-lookup"><span data-stu-id="69306-116">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="69306-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ 欄位 \_ SINGLE \_ \_ FIRST**</span><span class="sxs-lookup"><span data-stu-id="69306-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="69306-118">一種交錯的影片檔案，其中的欄位會以連續範例的形式傳送，而第1行) 的上方欄位 (則會先繪製。</span><span class="sxs-lookup"><span data-stu-id="69306-118">An interleaved video file where the fields are sent as contiguous samples and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="69306-119">如需詳細資訊，請參閱本節後面的「備註」。</span><span class="sxs-lookup"><span data-stu-id="69306-119">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="69306-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 欄位 \_ 的 \_ \_ 第一個較低**</span><span class="sxs-lookup"><span data-stu-id="69306-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="69306-121">一種交錯的影片檔案，其中的欄位會以連續範例的形式傳送，而第) 2 行 (的較低欄位則會先傳送。</span><span class="sxs-lookup"><span data-stu-id="69306-121">An interleaved video file where the fields are sent as contiguous samples and the lower field (with line 2) is sent first.</span></span>

</dd> <dt>

<span data-ttu-id="69306-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 混合 \_ 交錯**</span><span class="sxs-lookup"><span data-stu-id="69306-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE**</span></span>
</dt> <dd>

<span data-ttu-id="69306-123">混合交錯模式的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="69306-123">A video file with a mix of interlacing modes.</span></span>

</dd> <dt>

<span data-ttu-id="69306-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 混合 \_ 交錯 \_ 和 \_ 漸進**</span><span class="sxs-lookup"><span data-stu-id="69306-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE\_AND\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="69306-125">混合交錯和漸進模式的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="69306-125">A video file with a mix of interlaced and progressive modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69306-126">備註</span><span class="sxs-lookup"><span data-stu-id="69306-126">Remarks</span></span>

<span data-ttu-id="69306-127">此列舉是由 [WPD \_ VIDEO \_ SCAN \_ TYPE](properties-and-attributes.md) 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="69306-127">This enumeration is used by the [WPD\_VIDEO\_SCAN\_TYPE](properties-and-attributes.md) property.</span></span>

<span data-ttu-id="69306-128">這兩種類型的交錯檔案格式是由這個列舉所指定。</span><span class="sxs-lookup"><span data-stu-id="69306-128">There are two types of interleaved file formats that are specified by this enumeration.</span></span> <span data-ttu-id="69306-129">**WPD \_影片 \_ 掃描 \_ 類型 \_ 欄位 \_ 交錯** 指的是一種檔案格式，它會在掃描的欄位替換時傳遞框架，而資料會逐行進行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="69306-129">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED** refers to a file format where frames are delivered as they were scanned fields alternate and data goes line by line, as shown here:</span></span>

<span data-ttu-id="69306-130">**畫面 1**</span><span class="sxs-lookup"><span data-stu-id="69306-130">**Frame 1**</span></span>

<span data-ttu-id="69306-131">欄位1：行1</span><span class="sxs-lookup"><span data-stu-id="69306-131">Field 1: Line 1</span></span>

<span data-ttu-id="69306-132">欄位2：行1</span><span class="sxs-lookup"><span data-stu-id="69306-132">Field 2: Line 1</span></span>

<span data-ttu-id="69306-133">欄位1：第2行</span><span class="sxs-lookup"><span data-stu-id="69306-133">Field 1: Line 2</span></span>

<span data-ttu-id="69306-134">欄位2：第2行</span><span class="sxs-lookup"><span data-stu-id="69306-134">Field 2: Line 2</span></span>

<span data-ttu-id="69306-135">欄位1：第3行</span><span class="sxs-lookup"><span data-stu-id="69306-135">Field 1: Line 3</span></span>

<span data-ttu-id="69306-136">欄位2：第3行</span><span class="sxs-lookup"><span data-stu-id="69306-136">Field 2: Line 3</span></span>

<span data-ttu-id="69306-137">...</span><span class="sxs-lookup"><span data-stu-id="69306-137">...</span></span>

<span data-ttu-id="69306-138">**WPD \_影片 \_ 掃描 \_ 類型 \_ 欄位 \_ SINGLE** 指的是一種檔案格式，其中每個欄位都會儲存在掃描行的單一區塊中，而且會依序儲存欄位，如下所示：</span><span class="sxs-lookup"><span data-stu-id="69306-138">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE** refers to a file format where each field is stored in a single block of scan lines, and fields are stored sequentially, as shown here:</span></span>

<span data-ttu-id="69306-139">**畫面 1**</span><span class="sxs-lookup"><span data-stu-id="69306-139">**Frame 1**</span></span>

<span data-ttu-id="69306-140">欄位1：行1</span><span class="sxs-lookup"><span data-stu-id="69306-140">Field 1: Line 1</span></span>

<span data-ttu-id="69306-141">欄位1：第2行</span><span class="sxs-lookup"><span data-stu-id="69306-141">Field 1: Line 2</span></span>

<span data-ttu-id="69306-142">欄位1：第3行</span><span class="sxs-lookup"><span data-stu-id="69306-142">Field 1: Line 3</span></span>

<span data-ttu-id="69306-143">...</span><span class="sxs-lookup"><span data-stu-id="69306-143">...</span></span>

<span data-ttu-id="69306-144">其次</span><span class="sxs-lookup"><span data-stu-id="69306-144">Followed by</span></span>

<span data-ttu-id="69306-145">欄位2：行1</span><span class="sxs-lookup"><span data-stu-id="69306-145">Field 2: Line 1</span></span>

<span data-ttu-id="69306-146">欄位2：第2行</span><span class="sxs-lookup"><span data-stu-id="69306-146">Field 2: Line 2</span></span>

<span data-ttu-id="69306-147">欄位2：第3行</span><span class="sxs-lookup"><span data-stu-id="69306-147">Field 2: Line 3</span></span>

<span data-ttu-id="69306-148">...</span><span class="sxs-lookup"><span data-stu-id="69306-148">...</span></span>

## <a name="requirements"></a><span data-ttu-id="69306-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="69306-149">Requirements</span></span>



| <span data-ttu-id="69306-150">需求</span><span class="sxs-lookup"><span data-stu-id="69306-150">Requirement</span></span> | <span data-ttu-id="69306-151">值</span><span class="sxs-lookup"><span data-stu-id="69306-151">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="69306-152">標頭</span><span class="sxs-lookup"><span data-stu-id="69306-152">Header</span></span><br/> | <dl> <span data-ttu-id="69306-153"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="69306-153"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69306-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69306-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69306-155">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="69306-155">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




