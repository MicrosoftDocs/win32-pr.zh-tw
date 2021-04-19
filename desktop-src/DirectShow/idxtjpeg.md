---
description: IDxtJpeg 介面會設定「SMPTE 抹除」轉換的屬性。當 DirectShow 編輯服務轉譯了 SMPTE 抹除轉換時，會在內部使用此介面 (DES) 。
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: 'IDxtJpeg 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977671"
---
# <a name="idxtjpeg-interface"></a><span data-ttu-id="855ba-103">IDxtJpeg 介面</span><span class="sxs-lookup"><span data-stu-id="855ba-103">IDxtJpeg interface</span></span>

> [!Note]  
> <span data-ttu-id="855ba-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="855ba-104">\[Deprecated.</span></span> <span data-ttu-id="855ba-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="855ba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="855ba-106">`IDxtJpeg`介面會設定「 [SMPTE](smpte-wipe-transition.md)抹除」轉換的屬性。</span><span class="sxs-lookup"><span data-stu-id="855ba-106">The `IDxtJpeg` interface sets properties on the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

<span data-ttu-id="855ba-107">當 DirectShow 編輯服務轉譯了 SMPTE 抹除轉換時，會在內部使用此介面 (DES) 。</span><span class="sxs-lookup"><span data-stu-id="855ba-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the SMPTE Wipe transition.</span></span> <span data-ttu-id="855ba-108">DES 應用程式不需要使用此介面。</span><span class="sxs-lookup"><span data-stu-id="855ba-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="855ba-109">若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="855ba-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="855ba-110">成員</span><span class="sxs-lookup"><span data-stu-id="855ba-110">Members</span></span>

<span data-ttu-id="855ba-111">**IDxtJpeg** 介面繼承自 **IDXEffect**。</span><span class="sxs-lookup"><span data-stu-id="855ba-111">The **IDxtJpeg** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="855ba-112">**IDxtJpeg** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="855ba-112">**IDxtJpeg** also has these types of members:</span></span>

-   [<span data-ttu-id="855ba-113">方法</span><span class="sxs-lookup"><span data-stu-id="855ba-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="855ba-114">方法</span><span class="sxs-lookup"><span data-stu-id="855ba-114">Methods</span></span>

<span data-ttu-id="855ba-115">**IDxtJpeg** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="855ba-115">The **IDxtJpeg** interface has these methods.</span></span>



| <span data-ttu-id="855ba-116">方法</span><span class="sxs-lookup"><span data-stu-id="855ba-116">Method</span></span>                                                     | <span data-ttu-id="855ba-117">描述</span><span class="sxs-lookup"><span data-stu-id="855ba-117">Description</span></span>                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="855ba-118">**ApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="855ba-118">**ApplyChanges**</span></span>](idxtjpeg-applychanges.md)              | <span data-ttu-id="855ba-119">套用已變更的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="855ba-119">Applies any properties that have changed.</span></span><br/>                                      |
| [<span data-ttu-id="855ba-120">**取得 \_ 邊框**</span><span class="sxs-lookup"><span data-stu-id="855ba-120">**get\_BorderColor**</span></span>](idxtjpeg-get-bordercolor.md)       | <span data-ttu-id="855ba-121">抓取抹除模式邊緣周圍的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="855ba-121">Retrieves the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="855ba-122">**取得 \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="855ba-122">**get\_BorderSoftness**</span></span>](idxtjpeg-get-bordersoftness.md) | <span data-ttu-id="855ba-123">抓取抹除模式邊緣周圍模糊區域的寬度。</span><span class="sxs-lookup"><span data-stu-id="855ba-123">Retrieves the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="855ba-124">**取得 \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="855ba-124">**get\_BorderWidth**</span></span>](idxtjpeg-get-borderwidth.md)       | <span data-ttu-id="855ba-125">抓取抹除模式邊緣的實心框線寬度。</span><span class="sxs-lookup"><span data-stu-id="855ba-125">Retrieves the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="855ba-126">**取得 \_ MaskName**</span><span class="sxs-lookup"><span data-stu-id="855ba-126">**get\_MaskName**</span></span>](idxtjpeg-get-maskname.md)             | <span data-ttu-id="855ba-127">抓取要當做抹除遮罩使用的 JPEG 檔案名。</span><span class="sxs-lookup"><span data-stu-id="855ba-127">Retrieves the name of a JPEG file to be used as the wipe mask.</span></span><br/>                 |
| [<span data-ttu-id="855ba-128">**取得 \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="855ba-128">**get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)               | <span data-ttu-id="855ba-129">抓取抹除的 SMPTE 清除程式碼。</span><span class="sxs-lookup"><span data-stu-id="855ba-129">Retrieves the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="855ba-130">**取得 \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="855ba-130">**get\_OffsetX**</span></span>](idxtjpeg-get-offsetx.md)               | <span data-ttu-id="855ba-131">抓取抹除來源的水準位移。</span><span class="sxs-lookup"><span data-stu-id="855ba-131">Retrieves the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="855ba-132">**取得 \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="855ba-132">**get\_OffsetY**</span></span>](idxtjpeg-get-offsety.md)               | <span data-ttu-id="855ba-133">抓取抹除來源的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="855ba-133">Retrieves the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="855ba-134">**取得 \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="855ba-134">**get\_ReplicateX**</span></span>](idxtjpeg-get-replicatex.md)         | <span data-ttu-id="855ba-135">捕獲以水準方式複寫抹除模式的次數。</span><span class="sxs-lookup"><span data-stu-id="855ba-135">Retrieves the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="855ba-136">**取得 \_ ReplicateY**</span><span class="sxs-lookup"><span data-stu-id="855ba-136">**get\_ReplicateY**</span></span>](idxtjpeg-get-replicatey.md)         | <span data-ttu-id="855ba-137">捕獲以垂直方式複寫抹除模式的次數。</span><span class="sxs-lookup"><span data-stu-id="855ba-137">Retrieves the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="855ba-138">**取得 \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="855ba-138">**get\_ScaleX**</span></span>](idxtjpeg-get-scalex.md)                 | <span data-ttu-id="855ba-139">抓取抹除水準伸展的量。</span><span class="sxs-lookup"><span data-stu-id="855ba-139">Retrieves the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="855ba-140">**取得 \_ ScaleY**</span><span class="sxs-lookup"><span data-stu-id="855ba-140">**get\_ScaleY**</span></span>](idxtjpeg-get-scaley.md)                 | <span data-ttu-id="855ba-141">抓取抹除垂直伸展的量。</span><span class="sxs-lookup"><span data-stu-id="855ba-141">Retrieves the amount by which the wipe is stretched vertically.</span></span><br/>                |
| [<span data-ttu-id="855ba-142">**LoadDefSettings**</span><span class="sxs-lookup"><span data-stu-id="855ba-142">**LoadDefSettings**</span></span>](idxtjpeg-loaddefsettings.md)        | <span data-ttu-id="855ba-143">還原清除轉換的預設設定。</span><span class="sxs-lookup"><span data-stu-id="855ba-143">Restores the default settings of the Wipe transition.</span></span><br/>                          |
| [<span data-ttu-id="855ba-144">**put \_ 邊框存放**</span><span class="sxs-lookup"><span data-stu-id="855ba-144">**put\_BorderColor**</span></span>](idxtjpeg-put-bordercolor.md)       | <span data-ttu-id="855ba-145">指定抹除模式邊緣周圍的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="855ba-145">Specifies the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="855ba-146">**put \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="855ba-146">**put\_BorderSoftness**</span></span>](idxtjpeg-put-bordersoftness.md) | <span data-ttu-id="855ba-147">指定抹除模式邊緣周圍模糊區域的寬度。</span><span class="sxs-lookup"><span data-stu-id="855ba-147">Specifies the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="855ba-148">**put \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="855ba-148">**put\_BorderWidth**</span></span>](idxtjpeg-put-borderwidth.md)       | <span data-ttu-id="855ba-149">指定沿著抹除模式邊緣的實心框線寬度。</span><span class="sxs-lookup"><span data-stu-id="855ba-149">Specifies the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="855ba-150">**put \_ MaskName**</span><span class="sxs-lookup"><span data-stu-id="855ba-150">**put\_MaskName**</span></span>](idxtjpeg-put-maskname.md)             | <span data-ttu-id="855ba-151">指定要用作抹除遮罩的 JPEG 檔案名。</span><span class="sxs-lookup"><span data-stu-id="855ba-151">Specifies the name of a JPEG file to use as the wipe mask.</span></span><br/>                     |
| [<span data-ttu-id="855ba-152">**put \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="855ba-152">**put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)               | <span data-ttu-id="855ba-153">指定抹除的 SMPTE 清除程式碼。</span><span class="sxs-lookup"><span data-stu-id="855ba-153">Specifies the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="855ba-154">**put \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="855ba-154">**put\_OffsetX**</span></span>](idxtjpeg-put-offsetx.md)               | <span data-ttu-id="855ba-155">指定抹除來源的水準位移。</span><span class="sxs-lookup"><span data-stu-id="855ba-155">Specifies the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="855ba-156">**put \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="855ba-156">**put\_OffsetY**</span></span>](idxtjpeg-put-offsety.md)               | <span data-ttu-id="855ba-157">指定抹除來源的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="855ba-157">Specifies the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="855ba-158">**put \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="855ba-158">**put\_ReplicateX**</span></span>](idxtjpeg-put-replicatex.md)         | <span data-ttu-id="855ba-159">指定以水準方式複寫抹除模式的次數。</span><span class="sxs-lookup"><span data-stu-id="855ba-159">Specifies the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="855ba-160">**put \_ ReplicateY**</span><span class="sxs-lookup"><span data-stu-id="855ba-160">**put\_ReplicateY**</span></span>](idxtjpeg-put-replicatey.md)         | <span data-ttu-id="855ba-161">指定垂直複製抹除模式的次數。</span><span class="sxs-lookup"><span data-stu-id="855ba-161">Specifies the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="855ba-162">**put \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="855ba-162">**put\_ScaleX**</span></span>](idxtjpeg-put-scalex.md)                 | <span data-ttu-id="855ba-163">指定以水準方式延展抹除的量。</span><span class="sxs-lookup"><span data-stu-id="855ba-163">Specifies the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="855ba-164">**put \_ ScaleY**</span><span class="sxs-lookup"><span data-stu-id="855ba-164">**put\_ScaleY**</span></span>](idxtjpeg-put-scaley.md)                 | <span data-ttu-id="855ba-165">指定抹除垂直伸展的量。</span><span class="sxs-lookup"><span data-stu-id="855ba-165">Specifies the amount by which the wipe is stretched vertically.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="855ba-166">備註</span><span class="sxs-lookup"><span data-stu-id="855ba-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="855ba-167">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="855ba-167">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="855ba-168">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="855ba-168">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="855ba-169">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="855ba-169">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="855ba-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="855ba-170">Requirements</span></span>



| <span data-ttu-id="855ba-171">需求</span><span class="sxs-lookup"><span data-stu-id="855ba-171">Requirement</span></span> | <span data-ttu-id="855ba-172">值</span><span class="sxs-lookup"><span data-stu-id="855ba-172">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="855ba-173">標頭</span><span class="sxs-lookup"><span data-stu-id="855ba-173">Header</span></span><br/>  | <dl> <span data-ttu-id="855ba-174"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="855ba-174"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="855ba-175">程式庫</span><span class="sxs-lookup"><span data-stu-id="855ba-175">Library</span></span><br/> | <dl> <span data-ttu-id="855ba-176"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="855ba-176"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




