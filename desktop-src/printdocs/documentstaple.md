---
description: 瞭解 JobStapleAllDocuments 元素，其描述輸出的裝訂特性。
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2cda02c452ebb053c71811fb2642cea7371b2f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409131"
---
# <a name="documentstaple"></a><span data-ttu-id="88edd-103">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="88edd-103">DocumentStaple</span></span>

<span data-ttu-id="88edd-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="88edd-104">This topic is not current.</span></span> <span data-ttu-id="88edd-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="88edd-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88edd-106">描述輸出的裝訂特性。</span><span class="sxs-lookup"><span data-stu-id="88edd-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="88edd-107">每份檔都會另外進行裝訂。</span><span class="sxs-lookup"><span data-stu-id="88edd-107">Each document is stapled separately.</span></span> <span data-ttu-id="88edd-108">JobStapleAllDocuments 和 DocumentStaple 關鍵字是互斥的。</span><span class="sxs-lookup"><span data-stu-id="88edd-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="88edd-109">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="88edd-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="88edd-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="88edd-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88edd-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="88edd-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="88edd-112">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="88edd-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="88edd-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="88edd-113">Element Information</span></span>



| <span data-ttu-id="88edd-114">Name</span><span class="sxs-lookup"><span data-stu-id="88edd-114">Name</span></span> | <span data-ttu-id="88edd-115">值</span><span class="sxs-lookup"><span data-stu-id="88edd-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="88edd-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="88edd-116">Element Type</span></span> <br/>   | <span data-ttu-id="88edd-117">功能</span><span class="sxs-lookup"><span data-stu-id="88edd-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="88edd-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="88edd-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88edd-119">文件</span><span class="sxs-lookup"><span data-stu-id="88edd-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="88edd-120">備註</span><span class="sxs-lookup"><span data-stu-id="88edd-120">Notes</span></span> <br/>          | <span data-ttu-id="88edd-121">頂端、底部、左方和右邊都是相對於 PageImageableSize。</span><span class="sxs-lookup"><span data-stu-id="88edd-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="88edd-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="88edd-122">Structural Content</span></span>

<span data-ttu-id="88edd-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="88edd-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="88edd-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="88edd-124">Structure Variables</span></span>

<span data-ttu-id="88edd-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="88edd-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88edd-126">Name</span><span class="sxs-lookup"><span data-stu-id="88edd-126">Name</span></span>                               | <span data-ttu-id="88edd-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="88edd-127">Data type</span></span>          | <span data-ttu-id="88edd-128">單位</span><span class="sxs-lookup"><span data-stu-id="88edd-128">Unit</span></span>                       | <span data-ttu-id="88edd-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="88edd-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="88edd-130">總結</span><span class="sxs-lookup"><span data-stu-id="88edd-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88edd-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="88edd-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="88edd-132">string</span><span class="sxs-lookup"><span data-stu-id="88edd-132">string</span></span><br/>  | <span data-ttu-id="88edd-133">字元</span><span class="sxs-lookup"><span data-stu-id="88edd-133">characters</span></span><br/>      | <span data-ttu-id="88edd-134">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="88edd-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="88edd-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="88edd-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="88edd-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="88edd-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="88edd-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="88edd-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="88edd-138">string</span><span class="sxs-lookup"><span data-stu-id="88edd-138">string</span></span><br/>  | <span data-ttu-id="88edd-139">n/a</span><span class="sxs-lookup"><span data-stu-id="88edd-139">n/a</span></span><br/>             | <span data-ttu-id="88edd-140">True、False。</span><span class="sxs-lookup"><span data-stu-id="88edd-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="88edd-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="88edd-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="88edd-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="88edd-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="88edd-143">整數</span><span class="sxs-lookup"><span data-stu-id="88edd-143">integer</span></span><br/> | <span data-ttu-id="88edd-144">度</span><span class="sxs-lookup"><span data-stu-id="88edd-144">degrees</span></span><br/>         | <span data-ttu-id="88edd-145">大於 0。</span><span class="sxs-lookup"><span data-stu-id="88edd-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="88edd-146">指定裝訂角度（相對於 PageImageableSize 的 X 方向）。</span><span class="sxs-lookup"><span data-stu-id="88edd-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="88edd-147">裝訂角度是以逆時針方向來測量。</span><span class="sxs-lookup"><span data-stu-id="88edd-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="88edd-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="88edd-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="88edd-149">整數</span><span class="sxs-lookup"><span data-stu-id="88edd-149">integer</span></span><br/> | <span data-ttu-id="88edd-150">媒體的工作表</span><span class="sxs-lookup"><span data-stu-id="88edd-150">sheets of media</span></span><br/> | <span data-ttu-id="88edd-151">大於 0。</span><span class="sxs-lookup"><span data-stu-id="88edd-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="88edd-152">指定目前所選媒體媒體的裝訂選項所支援的工作表數目。</span><span class="sxs-lookup"><span data-stu-id="88edd-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="88edd-153">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="88edd-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="88edd-154">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="88edd-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="88edd-155">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="88edd-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None" />
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="88edd-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="88edd-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88edd-157">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="88edd-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




