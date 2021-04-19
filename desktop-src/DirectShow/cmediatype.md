---
description: CMediaType 類別會管理媒體類型。 此類別繼承 AM \_ 媒體 \_ 類型結構。 它可以轉換成類型為媒體類型的變數 \_ \_ 。
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: 'CMediaType 類別 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998792"
---
# <a name="cmediatype-class"></a><span data-ttu-id="6cb16-105">CMediaType 類別</span><span class="sxs-lookup"><span data-stu-id="6cb16-105">CMediaType class</span></span>

![cmediatype 類別階層](images/mtype01.png)

<span data-ttu-id="6cb16-107">`CMediaType`類別會管理媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-107">The `CMediaType` class manages media types.</span></span> <span data-ttu-id="6cb16-108">此類別繼承 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="6cb16-108">This class inherits the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="6cb16-109">它可以轉換成類型為 **\_ 媒體 \_ 類型** 的變數。</span><span class="sxs-lookup"><span data-stu-id="6cb16-109">It can be cast to a variable of type **AM\_MEDIA\_TYPE**.</span></span>



| <span data-ttu-id="6cb16-110">公用方法</span><span class="sxs-lookup"><span data-stu-id="6cb16-110">Public Methods</span></span>                                                      | <span data-ttu-id="6cb16-111">Description</span><span class="sxs-lookup"><span data-stu-id="6cb16-111">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="6cb16-112">**CMediaType**</span><span class="sxs-lookup"><span data-stu-id="6cb16-112">**CMediaType**</span></span>](cmediatype-cmediatype.md)                         | <span data-ttu-id="6cb16-113">函式方法。</span><span class="sxs-lookup"><span data-stu-id="6cb16-113">Constructor method.</span></span>                                                            |
| [<span data-ttu-id="6cb16-114">**~ CMediaType**</span><span class="sxs-lookup"><span data-stu-id="6cb16-114">**~CMediaType**</span></span>](cmediatype--cmediatype.md)                       | <span data-ttu-id="6cb16-115">函式方法。</span><span class="sxs-lookup"><span data-stu-id="6cb16-115">Destructor method.</span></span>                                                             |
| [<span data-ttu-id="6cb16-116">**設定**</span><span class="sxs-lookup"><span data-stu-id="6cb16-116">**Set**</span></span>](cmediatype-set.md)                                       | <span data-ttu-id="6cb16-117">設定另一種媒體類型的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-117">Sets the media type from another media type.</span></span>                                   |
| [<span data-ttu-id="6cb16-118">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="6cb16-118">**IsValid**</span></span>](cmediatype-isvalid.md)                               | <span data-ttu-id="6cb16-119">判斷是否已將主要類型指派給這個物件。</span><span class="sxs-lookup"><span data-stu-id="6cb16-119">Determines whether a major type has been assigned to this object.</span></span>              |
| [<span data-ttu-id="6cb16-120">**類型**</span><span class="sxs-lookup"><span data-stu-id="6cb16-120">**Type**</span></span>](cmediatype-type.md)                                     | <span data-ttu-id="6cb16-121">抓取主要型別。</span><span class="sxs-lookup"><span data-stu-id="6cb16-121">Retrieves the major type.</span></span>                                                      |
| [<span data-ttu-id="6cb16-122">**>advanced.field.settype**</span><span class="sxs-lookup"><span data-stu-id="6cb16-122">**SetType**</span></span>](cmediatype-settype.md)                               | <span data-ttu-id="6cb16-123">指定主要類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-123">Specifies the major type.</span></span>                                                      |
| [<span data-ttu-id="6cb16-124">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="6cb16-124">**Subtype**</span></span>](cmediatype-subtype.md)                               | <span data-ttu-id="6cb16-125">抓取子類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-125">Retrieves the subtype.</span></span>                                                         |
| [<span data-ttu-id="6cb16-126">**SetSubtype**</span><span class="sxs-lookup"><span data-stu-id="6cb16-126">**SetSubtype**</span></span>](cmediatype-setsubtype.md)                         | <span data-ttu-id="6cb16-127">指定子類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-127">Specifies the subtype.</span></span>                                                         |
| [<span data-ttu-id="6cb16-128">**IsFixedSize**</span><span class="sxs-lookup"><span data-stu-id="6cb16-128">**IsFixedSize**</span></span>](cmediatype-isfixedsize.md)                       | <span data-ttu-id="6cb16-129">判斷樣本的大小是否固定或變數大小。</span><span class="sxs-lookup"><span data-stu-id="6cb16-129">Determines if the samples have a fixed size or a variable size.</span></span>                |
| [<span data-ttu-id="6cb16-130">**IsTemporalCompressed**</span><span class="sxs-lookup"><span data-stu-id="6cb16-130">**IsTemporalCompressed**</span></span>](cmediatype-istemporalcompressed.md)     | <span data-ttu-id="6cb16-131">判斷資料流程是否使用時態性壓縮。</span><span class="sxs-lookup"><span data-stu-id="6cb16-131">Determines if the stream uses temporal compression.</span></span>                            |
| [<span data-ttu-id="6cb16-132">**GetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="6cb16-132">**GetSampleSize**</span></span>](cmediatype-getsamplesize.md)                   | <span data-ttu-id="6cb16-133">抓取範例大小。</span><span class="sxs-lookup"><span data-stu-id="6cb16-133">Retrieves the sample size.</span></span>                                                     |
| [<span data-ttu-id="6cb16-134">**SetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="6cb16-134">**SetSampleSize**</span></span>](cmediatype-setsamplesize.md)                   | <span data-ttu-id="6cb16-135">指定固定樣本大小，或指定樣本具有變數大小。</span><span class="sxs-lookup"><span data-stu-id="6cb16-135">Specifies a fixed sample size, or specifies that samples have a variable size.</span></span> |
| [<span data-ttu-id="6cb16-136">**SetVariableSize**</span><span class="sxs-lookup"><span data-stu-id="6cb16-136">**SetVariableSize**</span></span>](cmediatype-setvariablesize.md)               | <span data-ttu-id="6cb16-137">指定範例沒有固定的大小。</span><span class="sxs-lookup"><span data-stu-id="6cb16-137">Specifies that samples do not have a fixed size.</span></span>                               |
| [<span data-ttu-id="6cb16-138">**SetTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="6cb16-138">**SetTemporalCompression**</span></span>](cmediatype-settemporalcompression.md) | <span data-ttu-id="6cb16-139">指定是否使用時態壓縮來壓縮範例。</span><span class="sxs-lookup"><span data-stu-id="6cb16-139">Specifies whether samples are compressed using temporal compression.</span></span>           |
| [<span data-ttu-id="6cb16-140">**格式**</span><span class="sxs-lookup"><span data-stu-id="6cb16-140">**Format**</span></span>](cmediatype-format.md)                                 | <span data-ttu-id="6cb16-141">抓取格式區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="6cb16-141">Retrieves a pointer to the format block.</span></span>                                       |
| [<span data-ttu-id="6cb16-142">**FormatLength**</span><span class="sxs-lookup"><span data-stu-id="6cb16-142">**FormatLength**</span></span>](cmediatype-formatlength.md)                     | <span data-ttu-id="6cb16-143">抓取格式區塊的長度。</span><span class="sxs-lookup"><span data-stu-id="6cb16-143">Retrieves the length of the format block.</span></span>                                      |
| [<span data-ttu-id="6cb16-144">**SetFormatType**</span><span class="sxs-lookup"><span data-stu-id="6cb16-144">**SetFormatType**</span></span>](cmediatype-setformattype.md)                   | <span data-ttu-id="6cb16-145">指定格式類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-145">Specifies the format type.</span></span>                                                     |
| [<span data-ttu-id="6cb16-146">**FormatType**</span><span class="sxs-lookup"><span data-stu-id="6cb16-146">**FormatType**</span></span>](cmediatype-formattype.md)                         | <span data-ttu-id="6cb16-147">抓取格式類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-147">Retrieves the format type.</span></span>                                                     |
| [<span data-ttu-id="6cb16-148">**SetFormat**</span><span class="sxs-lookup"><span data-stu-id="6cb16-148">**SetFormat**</span></span>](cmediatype-setformat.md)                           | <span data-ttu-id="6cb16-149">指定格式區塊。</span><span class="sxs-lookup"><span data-stu-id="6cb16-149">Specifies the format block.</span></span>                                                    |
| [<span data-ttu-id="6cb16-150">**ResetFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="6cb16-150">**ResetFormatBuffer**</span></span>](cmediatype-resetformatbuffer.md)           | <span data-ttu-id="6cb16-151">刪除格式區塊。</span><span class="sxs-lookup"><span data-stu-id="6cb16-151">Deletes the format block.</span></span>                                                      |
| [<span data-ttu-id="6cb16-152">**AllocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="6cb16-152">**AllocFormatBuffer**</span></span>](cmediatype-allocformatbuffer.md)           | <span data-ttu-id="6cb16-153">配置格式區塊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6cb16-153">Allocates memory for the format block.</span></span>                                         |
| [<span data-ttu-id="6cb16-154">**ReallocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="6cb16-154">**ReallocFormatBuffer**</span></span>](cmediatype-reallocformatbuffer.md)       | <span data-ttu-id="6cb16-155">將格式區塊重新配置為新的大小。</span><span class="sxs-lookup"><span data-stu-id="6cb16-155">Reallocates the format block to a new size.</span></span>                                    |
| [<span data-ttu-id="6cb16-156">**InitMediaType**</span><span class="sxs-lookup"><span data-stu-id="6cb16-156">**InitMediaType**</span></span>](cmediatype-initmediatype.md)                   | <span data-ttu-id="6cb16-157">初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-157">Initializes the media type.</span></span>                                                    |
| [<span data-ttu-id="6cb16-158">**MatchesPartial**</span><span class="sxs-lookup"><span data-stu-id="6cb16-158">**MatchesPartial**</span></span>](cmediatype-matchespartial.md)                 | <span data-ttu-id="6cb16-159">判斷此媒體類型是否符合部分指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-159">Determines if this media type matches a partially specified media type.</span></span>        |
| [<span data-ttu-id="6cb16-160">**IsPartiallySpecified**</span><span class="sxs-lookup"><span data-stu-id="6cb16-160">**IsPartiallySpecified**</span></span>](cmediatype-ispartiallyspecified.md)     | <span data-ttu-id="6cb16-161">判斷是否已部分定義媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-161">Determines if the media type is partially defined.</span></span>                             |
| <span data-ttu-id="6cb16-162">運算子</span><span class="sxs-lookup"><span data-stu-id="6cb16-162">Operators</span></span>                                                           | <span data-ttu-id="6cb16-163">說明</span><span class="sxs-lookup"><span data-stu-id="6cb16-163">Description</span></span>                                                                    |
| [<span data-ttu-id="6cb16-164">**運算子 =**</span><span class="sxs-lookup"><span data-stu-id="6cb16-164">**operator =**</span></span>](cmediatype-operator-.md)                          | <span data-ttu-id="6cb16-165">多載指派運算子來複製媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6cb16-165">Overloads the assignment operator to copy a media type.</span></span>                        |
| [<span data-ttu-id="6cb16-166">**operator = =**</span><span class="sxs-lookup"><span data-stu-id="6cb16-166">**operator ==**</span></span>](cmediatype-operator--.md)                        | <span data-ttu-id="6cb16-167">測試 `CMediaType` 物件是否相等。</span><span class="sxs-lookup"><span data-stu-id="6cb16-167">Tests for equality between `CMediaType` objects.</span></span>                               |
| [<span data-ttu-id="6cb16-168">**operator！ =**</span><span class="sxs-lookup"><span data-stu-id="6cb16-168">**operator !=**</span></span>](cmediatype-operator-neq.md)                      | <span data-ttu-id="6cb16-169">測試 `CMediaType` 物件是否不相等。</span><span class="sxs-lookup"><span data-stu-id="6cb16-169">Tests for inequality between `CMediaType` objects.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="6cb16-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cb16-170">Requirements</span></span>



| <span data-ttu-id="6cb16-171">需求</span><span class="sxs-lookup"><span data-stu-id="6cb16-171">Requirement</span></span> | <span data-ttu-id="6cb16-172">值</span><span class="sxs-lookup"><span data-stu-id="6cb16-172">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb16-173">標頭</span><span class="sxs-lookup"><span data-stu-id="6cb16-173">Header</span></span><br/>  | <dl> <span data-ttu-id="6cb16-174"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6cb16-174"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6cb16-175">程式庫</span><span class="sxs-lookup"><span data-stu-id="6cb16-175">Library</span></span><br/> | <dl> <span data-ttu-id="6cb16-176"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6cb16-176"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




