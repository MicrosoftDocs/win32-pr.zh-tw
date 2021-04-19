---
description: IDxtCompositor 介面會設定組合器轉換的屬性。此介面是由 DirectShow 編輯服務在內部使用， (DES) 轉譯合成器轉換時使用。
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: 'IDxtCompositor 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984810"
---
# <a name="idxtcompositor-interface"></a><span data-ttu-id="95593-103">IDxtCompositor 介面</span><span class="sxs-lookup"><span data-stu-id="95593-103">IDxtCompositor interface</span></span>

> [!Note]  
> <span data-ttu-id="95593-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="95593-104">\[Deprecated.</span></span> <span data-ttu-id="95593-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="95593-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95593-106">`IDxtCompositor`介面會設定[組合](compositor-transition.md)器轉換的屬性。</span><span class="sxs-lookup"><span data-stu-id="95593-106">The `IDxtCompositor` interface sets properties on the [Compositor](compositor-transition.md) transition.</span></span>

<span data-ttu-id="95593-107">此介面是由 DirectShow 編輯服務在內部使用， (DES) 轉譯合成器轉換時使用。</span><span class="sxs-lookup"><span data-stu-id="95593-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Compositor transition.</span></span> <span data-ttu-id="95593-108">DES 應用程式不需要使用此介面。</span><span class="sxs-lookup"><span data-stu-id="95593-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="95593-109">若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="95593-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="95593-110">組合器轉換會將前景影像合成至背景影像。</span><span class="sxs-lookup"><span data-stu-id="95593-110">The Compositor transition composites a foreground image onto a background image.</span></span> <span data-ttu-id="95593-111">*來源矩形* 會定義以複合的前景影像區段。</span><span class="sxs-lookup"><span data-stu-id="95593-111">The *source rectangle* defines the section of the foreground image that is composited.</span></span> <span data-ttu-id="95593-112">*目的地矩形* 會定義接收前景影像的背景影像區段。</span><span class="sxs-lookup"><span data-stu-id="95593-112">The *destination rectangle* defines the section of the background image that receives the foreground image.</span></span> <span data-ttu-id="95593-113">下圖說明這些矩形。</span><span class="sxs-lookup"><span data-stu-id="95593-113">The following diagram illustrates these rectangles.</span></span>

![組合器轉換屬性](images/compmeasure.png)

## <a name="members"></a><span data-ttu-id="95593-115">成員</span><span class="sxs-lookup"><span data-stu-id="95593-115">Members</span></span>

<span data-ttu-id="95593-116">**IDxtCompositor** 介面繼承自 **IDXEffect**。</span><span class="sxs-lookup"><span data-stu-id="95593-116">The **IDxtCompositor** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="95593-117">**IDxtCompositor** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="95593-117">**IDxtCompositor** also has these types of members:</span></span>

-   [<span data-ttu-id="95593-118">方法</span><span class="sxs-lookup"><span data-stu-id="95593-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="95593-119">方法</span><span class="sxs-lookup"><span data-stu-id="95593-119">Methods</span></span>

<span data-ttu-id="95593-120">**IDxtCompositor** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="95593-120">The **IDxtCompositor** interface has these methods.</span></span>



| <span data-ttu-id="95593-121">方法</span><span class="sxs-lookup"><span data-stu-id="95593-121">Method</span></span>                                                   | <span data-ttu-id="95593-122">描述</span><span class="sxs-lookup"><span data-stu-id="95593-122">Description</span></span>                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="95593-123">**取得 \_ 高度**</span><span class="sxs-lookup"><span data-stu-id="95593-123">**get\_Height**</span></span>](idxtcompositor-get-height.md)         | <span data-ttu-id="95593-124">抓取目標矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="95593-124">Retrieves the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="95593-125">**取得 \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="95593-125">**get\_OffsetX**</span></span>](idxtcompositor-get-offsetx.md)       | <span data-ttu-id="95593-126">抓取目標矩形的水準位移。</span><span class="sxs-lookup"><span data-stu-id="95593-126">Retrieves the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="95593-127">**取得 \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="95593-127">**get\_OffsetY**</span></span>](idxtcompositor-get-offsety.md)       | <span data-ttu-id="95593-128">抓取目標矩形的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="95593-128">Retrieves the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="95593-129">**取得 \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="95593-129">**get\_SrcHeight**</span></span>](idxtcompositor-get-srcheight.md)   | <span data-ttu-id="95593-130">抓取來源矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="95593-130">Retrieves the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="95593-131">**取得 \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="95593-131">**get\_SrcOffsetX**</span></span>](idxtcompositor-get-srcoffsetx.md) | <span data-ttu-id="95593-132">抓取來源矩形的水準位移。</span><span class="sxs-lookup"><span data-stu-id="95593-132">Retrieves the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="95593-133">**取得 \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="95593-133">**get\_SrcOffsetY**</span></span>](idxtcompositor-get-srcoffsety.md) | <span data-ttu-id="95593-134">抓取來源矩形的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="95593-134">Retrieves the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="95593-135">**取得 \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="95593-135">**get\_SrcWidth**</span></span>](idxtcompositor-get-srcwidth.md)     | <span data-ttu-id="95593-136">抓取來源矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="95593-136">Retrieves the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="95593-137">**取得 \_ 寬度**</span><span class="sxs-lookup"><span data-stu-id="95593-137">**get\_Width**</span></span>](idxtcompositor-get-width.md)           | <span data-ttu-id="95593-138">抓取目標矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="95593-138">Retrieves the width of the target rectangle.</span></span><br/>             |
| [<span data-ttu-id="95593-139">**put \_ Height**</span><span class="sxs-lookup"><span data-stu-id="95593-139">**put\_Height**</span></span>](idxtcompositor-put-height.md)         | <span data-ttu-id="95593-140">指定目標矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="95593-140">Specifies the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="95593-141">**put \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="95593-141">**put\_OffsetX**</span></span>](idxtcompositor-put-offsetx.md)       | <span data-ttu-id="95593-142">指定目標矩形的水準位移。</span><span class="sxs-lookup"><span data-stu-id="95593-142">Specifies the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="95593-143">**put \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="95593-143">**put\_OffsetY**</span></span>](idxtcompositor-put-offsety.md)       | <span data-ttu-id="95593-144">指定目標矩形的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="95593-144">Specifies the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="95593-145">**put \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="95593-145">**put\_SrcHeight**</span></span>](idxtcompositor-put-srcheight.md)   | <span data-ttu-id="95593-146">指定來源矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="95593-146">Specifies the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="95593-147">**put \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="95593-147">**put\_SrcOffsetX**</span></span>](idxtcompositor-put-srcoffsetx.md) | <span data-ttu-id="95593-148">指定來源矩形的水準位移。</span><span class="sxs-lookup"><span data-stu-id="95593-148">Specifies the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="95593-149">**put \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="95593-149">**put\_SrcOffsetY**</span></span>](idxtcompositor-put-srcoffsety.md) | <span data-ttu-id="95593-150">指定來源矩形的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="95593-150">Specifies the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="95593-151">**put \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="95593-151">**put\_SrcWidth**</span></span>](idxtcompositor-put-srcwidth.md)     | <span data-ttu-id="95593-152">指定來源矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="95593-152">Specifies the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="95593-153">**put \_ 寬度**</span><span class="sxs-lookup"><span data-stu-id="95593-153">**put\_Width**</span></span>](idxtcompositor-put-width.md)           | <span data-ttu-id="95593-154">指定目標矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="95593-154">Specifies the width of the target rectangle.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="95593-155">備註</span><span class="sxs-lookup"><span data-stu-id="95593-155">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95593-156">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="95593-156">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="95593-157">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="95593-157">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="95593-158">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="95593-158">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95593-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="95593-159">Requirements</span></span>



| <span data-ttu-id="95593-160">需求</span><span class="sxs-lookup"><span data-stu-id="95593-160">Requirement</span></span> | <span data-ttu-id="95593-161">值</span><span class="sxs-lookup"><span data-stu-id="95593-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95593-162">標頭</span><span class="sxs-lookup"><span data-stu-id="95593-162">Header</span></span><br/>  | <dl> <span data-ttu-id="95593-163"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="95593-163"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="95593-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="95593-164">Library</span></span><br/> | <dl> <span data-ttu-id="95593-165"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="95593-165"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




