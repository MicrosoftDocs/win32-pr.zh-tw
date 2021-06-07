---
title: " (Windows 功能區架構) 的 Image 元素"
description: 表示影像。
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- 影像元素視窗功能區
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442889"
---
# <a name="image-element"></a><span data-ttu-id="33fbd-104">Image 項目</span><span class="sxs-lookup"><span data-stu-id="33fbd-104">Image element</span></span>

<span data-ttu-id="33fbd-105">表示影像。</span><span class="sxs-lookup"><span data-stu-id="33fbd-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="33fbd-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="33fbd-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="33fbd-107">屬性</span><span class="sxs-lookup"><span data-stu-id="33fbd-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33fbd-108">屬性</span><span class="sxs-lookup"><span data-stu-id="33fbd-108">Attribute</span></span></th>
<th><span data-ttu-id="33fbd-109">類型</span><span class="sxs-lookup"><span data-stu-id="33fbd-109">Type</span></span></th>
<th><span data-ttu-id="33fbd-110">必要</span><span class="sxs-lookup"><span data-stu-id="33fbd-110">Required</span></span></th>
<th><span data-ttu-id="33fbd-111">說明</span><span class="sxs-lookup"><span data-stu-id="33fbd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33fbd-112"><strong>識別碼</strong></span><span class="sxs-lookup"><span data-stu-id="33fbd-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="33fbd-113">xs： positiveInteger union xs： string</span><span class="sxs-lookup"><span data-stu-id="33fbd-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="33fbd-114">否</span><span class="sxs-lookup"><span data-stu-id="33fbd-114">No</span></span><br/></td>
<td><span data-ttu-id="33fbd-115">唯一的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="33fbd-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="33fbd-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 和 xs： string 的聯集) </span><span class="sxs-lookup"><span data-stu-id="33fbd-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="33fbd-117">介於2和59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="33fbd-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="33fbd-118">最大長度為10個字元，包括選擇性前置零。</span><span class="sxs-lookup"><span data-stu-id="33fbd-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33fbd-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="33fbd-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="33fbd-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="33fbd-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="33fbd-121">否</span><span class="sxs-lookup"><span data-stu-id="33fbd-121">No</span></span><br/></td>
<td><span data-ttu-id="33fbd-122"><dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="33fbd-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="33fbd-123">最小值為96的任何數位序列。</span><span class="sxs-lookup"><span data-stu-id="33fbd-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="33fbd-124">如果省略 MinDPI，預設值為96。</span><span class="sxs-lookup"><span data-stu-id="33fbd-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33fbd-125"><strong>來源</strong></span><span class="sxs-lookup"><span data-stu-id="33fbd-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="33fbd-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="33fbd-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="33fbd-127">否</span><span class="sxs-lookup"><span data-stu-id="33fbd-127">No</span></span><br/></td>
<td><span data-ttu-id="33fbd-128"><dt><span></span><span></span><strong></strong> (xs： anyURI) </span><span class="sxs-lookup"><span data-stu-id="33fbd-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="33fbd-129">表示 URI 的任何字元序列。</span><span class="sxs-lookup"><span data-stu-id="33fbd-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="33fbd-130">URI 值是功能區標記檔案的絕對或相對 (，) 類型為 BMP 之影像資源的路徑。</span><span class="sxs-lookup"><span data-stu-id="33fbd-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33fbd-131"><strong>符號</strong></span><span class="sxs-lookup"><span data-stu-id="33fbd-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="33fbd-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="33fbd-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="33fbd-133">否</span><span class="sxs-lookup"><span data-stu-id="33fbd-133">No</span></span><br/></td>
<td><span data-ttu-id="33fbd-134">影像的資源符號。</span><span class="sxs-lookup"><span data-stu-id="33fbd-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="33fbd-135">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="33fbd-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="33fbd-136">由字母或底線組成的字串，後面接著字母、數位或底線的任意序列，最多100個字元。</span><span class="sxs-lookup"><span data-stu-id="33fbd-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="33fbd-137">子元素</span><span class="sxs-lookup"><span data-stu-id="33fbd-137">Child elements</span></span>



| <span data-ttu-id="33fbd-138">元素</span><span class="sxs-lookup"><span data-stu-id="33fbd-138">Element</span></span>                                                               | <span data-ttu-id="33fbd-139">描述</span><span class="sxs-lookup"><span data-stu-id="33fbd-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="33fbd-140">**映射。來源**</span><span class="sxs-lookup"><span data-stu-id="33fbd-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="33fbd-141">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="33fbd-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="33fbd-142">父元素</span><span class="sxs-lookup"><span data-stu-id="33fbd-142">Parent elements</span></span>



| <span data-ttu-id="33fbd-143">元素</span><span class="sxs-lookup"><span data-stu-id="33fbd-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33fbd-144">**LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="33fbd-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="33fbd-145">**LargeImages**</span><span class="sxs-lookup"><span data-stu-id="33fbd-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="33fbd-146">**SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="33fbd-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="33fbd-147">**SmallImages**</span><span class="sxs-lookup"><span data-stu-id="33fbd-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="33fbd-148">備註</span><span class="sxs-lookup"><span data-stu-id="33fbd-148">Remarks</span></span>

<span data-ttu-id="33fbd-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="33fbd-149">Optional.</span></span>

<span data-ttu-id="33fbd-150">每個 [**命令 SmallImages**](windowsribbon-element-command-smallimages.md)、 [**SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)、 [**LargeImages**](windowsribbon-element-command-largeimages.md)或 [**LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) 元素都可能發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="33fbd-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="33fbd-151">當設計用來支援每英寸特定螢幕點的影像資源集合時 (DPI) 設定會透過一組 **影像** 元素提供給功能區架構，而架構會使用 *MinDPI* 屬性值符合目前螢幕 DPI 設定的 **影像**。</span><span class="sxs-lookup"><span data-stu-id="33fbd-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="33fbd-152">如果未使用符合目前螢幕 DPI 設定的 *MinDPI* 值來宣告 **影像** 元素，則架構會挑選最接近目前螢幕 DPI 設定的最接近 *MinDPI* 值的 **影像**，並向上調整影像資源。</span><span class="sxs-lookup"><span data-stu-id="33fbd-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="33fbd-153">否則，如果未使用 *MinDPI* 屬性值（小於目前的螢幕 DPI 設定）來宣告 **影像** 元素，則架構會挑選大於目前螢幕 DPI 設定的最接近 *MinDPI* 值，並將影像資源向下調整。</span><span class="sxs-lookup"><span data-stu-id="33fbd-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="33fbd-154">範例</span><span class="sxs-lookup"><span data-stu-id="33fbd-154">Examples</span></span>

<span data-ttu-id="33fbd-155">下列程式碼範例會示範透過一組 **影像** 元素來宣告所需的標記，此集合是設計用來支援四個特定螢幕 DPI 設定的影像資源集合。</span><span class="sxs-lookup"><span data-stu-id="33fbd-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a><span data-ttu-id="33fbd-156">項目資訊</span><span class="sxs-lookup"><span data-stu-id="33fbd-156">Element information</span></span>

* <span data-ttu-id="33fbd-157">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="33fbd-157">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="33fbd-158">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="33fbd-158">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="33fbd-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33fbd-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fbd-160">指定功能區影像資源</span><span class="sxs-lookup"><span data-stu-id="33fbd-160">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





