---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9abf6184c3164e0e5a1492911e15794ea7e1d948
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993905"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="50df9-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="50df9-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="50df9-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="50df9-105">This topic is not current.</span></span> <span data-ttu-id="50df9-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="50df9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="50df9-107">描述輸出的裝訂特性。</span><span class="sxs-lookup"><span data-stu-id="50df9-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="50df9-108">作業中的所有檔都會一起裝訂。</span><span class="sxs-lookup"><span data-stu-id="50df9-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="50df9-109">JobStapleAllDocuments 和 DocumentStaple 關鍵字是互斥的。</span><span class="sxs-lookup"><span data-stu-id="50df9-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="50df9-110">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="50df9-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="50df9-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="50df9-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="50df9-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="50df9-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="50df9-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="50df9-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="50df9-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="50df9-114">Element Information</span></span>



| <span data-ttu-id="50df9-115">Name</span><span class="sxs-lookup"><span data-stu-id="50df9-115">Name</span></span> | <span data-ttu-id="50df9-116">值</span><span class="sxs-lookup"><span data-stu-id="50df9-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="50df9-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="50df9-117">Element Type</span></span> <br/>   | <span data-ttu-id="50df9-118">功能</span><span class="sxs-lookup"><span data-stu-id="50df9-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="50df9-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="50df9-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="50df9-120">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="50df9-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="50df9-121">備註</span><span class="sxs-lookup"><span data-stu-id="50df9-121">Notes</span></span> <br/>          | <span data-ttu-id="50df9-122">頂端、底部、左方和右邊都是相對於 PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="50df9-122">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="50df9-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="50df9-123">Structural Content</span></span>

<span data-ttu-id="50df9-124">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="50df9-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="50df9-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="50df9-125">Structure Variables</span></span>

<span data-ttu-id="50df9-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="50df9-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="50df9-127">Name</span><span class="sxs-lookup"><span data-stu-id="50df9-127">Name</span></span>                               | <span data-ttu-id="50df9-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="50df9-128">Data type</span></span>          | <span data-ttu-id="50df9-129">單位</span><span class="sxs-lookup"><span data-stu-id="50df9-129">Unit</span></span>                       | <span data-ttu-id="50df9-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="50df9-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="50df9-131">總結</span><span class="sxs-lookup"><span data-stu-id="50df9-131">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50df9-132">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="50df9-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="50df9-133">字串</span><span class="sxs-lookup"><span data-stu-id="50df9-133">string</span></span><br/>  | <span data-ttu-id="50df9-134">Characters</span><span class="sxs-lookup"><span data-stu-id="50df9-134">Characters</span></span><br/>      | <span data-ttu-id="50df9-135">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="50df9-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="50df9-136">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="50df9-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="50df9-137">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="50df9-137">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="50df9-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="50df9-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="50df9-139">字串</span><span class="sxs-lookup"><span data-stu-id="50df9-139">string</span></span><br/>  | <span data-ttu-id="50df9-140">n/a</span><span class="sxs-lookup"><span data-stu-id="50df9-140">n/a</span></span><br/>             | <span data-ttu-id="50df9-141">True、False。</span><span class="sxs-lookup"><span data-stu-id="50df9-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="50df9-142">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="50df9-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="50df9-143">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="50df9-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="50df9-144">整數</span><span class="sxs-lookup"><span data-stu-id="50df9-144">integer</span></span><br/> | <span data-ttu-id="50df9-145">度</span><span class="sxs-lookup"><span data-stu-id="50df9-145">degrees</span></span><br/>         | <span data-ttu-id="50df9-146">大於 0。</span><span class="sxs-lookup"><span data-stu-id="50df9-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="50df9-147">指定裝訂角度（相對於 PageImageableSize 的寬度）。</span><span class="sxs-lookup"><span data-stu-id="50df9-147">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="50df9-148">裝訂角度是以逆時針方向來測量。</span><span class="sxs-lookup"><span data-stu-id="50df9-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="50df9-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="50df9-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="50df9-150">整數</span><span class="sxs-lookup"><span data-stu-id="50df9-150">integer</span></span><br/> | <span data-ttu-id="50df9-151">媒體的工作表</span><span class="sxs-lookup"><span data-stu-id="50df9-151">sheets of media</span></span><br/> | <span data-ttu-id="50df9-152">大於 0。</span><span class="sxs-lookup"><span data-stu-id="50df9-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="50df9-153">指定目前所選媒體媒體的裝訂選項所支援的工作表數目。</span><span class="sxs-lookup"><span data-stu-id="50df9-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="50df9-154">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="50df9-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="50df9-155">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="50df9-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="50df9-156">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="50df9-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
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

## <a name="related-topics"></a><span data-ttu-id="50df9-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="50df9-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50df9-158">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="50df9-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




