---
title: WCS 色彩外觀模型設定檔架構和演算法
description: WCS 色彩外觀模型設定檔架構和演算法
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- 'Windows Color System (WCS) 、色彩外觀模型設定檔 (CAMP) '
- 'WCS (Windows 色彩系統) ，色彩外觀模型設定檔 (CAMP) '
- '影像色彩管理、色彩外觀模型設定檔 (CAMP) '
- '色彩管理、色彩外觀模型設定檔 (CAMP) '
- '色彩、色彩外觀模型設定檔 (CAMP) '
- Windows Color System (WCS) ，設定檔
- WCS (Windows 色彩系統) ，設定檔
- 影像色彩管理，設定檔
- 色彩管理，設定檔
- 色彩，設定檔
- '色彩外觀模型設定檔 (CAMP) '
- 'CAMP (色彩外觀模型設定檔) '
- '架構、色彩外觀模型設定檔 (CAMP) '
- '演算法、色彩外觀模型設定檔 (CAMP) '
- WCS 色彩外觀模型設定檔
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106988085"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a><span data-ttu-id="96439-118">WCS 色彩外觀模型設定檔架構和演算法</span><span class="sxs-lookup"><span data-stu-id="96439-118">WCS Color Appearance Model Profile Schema and Algorithm</span></span>

[<span data-ttu-id="96439-119">概觀</span><span class="sxs-lookup"><span data-stu-id="96439-119">Overview</span></span>](#overview)

[<span data-ttu-id="96439-120">色彩外觀模型設定檔 (CAMP) 架構</span><span class="sxs-lookup"><span data-stu-id="96439-120">Color Appearance Model Profile (CAMP) Architecture</span></span>](#color-appearance-model-profile-architecture)

[<span data-ttu-id="96439-121">CAMP 架構</span><span class="sxs-lookup"><span data-stu-id="96439-121">The CAMP Schema</span></span>](#the-camp-schema)

[<span data-ttu-id="96439-122">CAMP 架構元素</span><span class="sxs-lookup"><span data-stu-id="96439-122">The CAMP Schema Elements</span></span>](#the-camp-schema-elements)

[<span data-ttu-id="96439-123">CAMP 演算法</span><span class="sxs-lookup"><span data-stu-id="96439-123">The CAMP Algorithm</span></span>](#the-camp-algorithm)

### <a name="overview"></a><span data-ttu-id="96439-124">概觀</span><span class="sxs-lookup"><span data-stu-id="96439-124">Overview</span></span>

<span data-ttu-id="96439-125">此架構可用來指定色彩外觀模型設定檔 (CAMP) 的內容。</span><span class="sxs-lookup"><span data-stu-id="96439-125">This schema is used to specify the content of a color appearance model profile (CAMP).</span></span> <span data-ttu-id="96439-126">下列各節將說明相關聯的基準演算法。</span><span class="sxs-lookup"><span data-stu-id="96439-126">The associated baseline algorithms are described in the following sections.</span></span>

<span data-ttu-id="96439-127">CAMP 是由 XML 標記所組成，可將參數值提供給 CIECAM02 基準色彩外觀模型變數。</span><span class="sxs-lookup"><span data-stu-id="96439-127">The CAMP is composed of XML tags that provide parametric values to the CIECAM02 baseline color appearance model variables.</span></span> <span data-ttu-id="96439-128">有關參數範圍的詳細資料會在基準色彩外觀模型規格和 CIECAM02 建議中提供。</span><span class="sxs-lookup"><span data-stu-id="96439-128">Details on the ranges for parameters are provided in the baseline color appearance model specification and CIECAM02 recommendation.</span></span>

### <a name="color-appearance-model-profile-architecture"></a><span data-ttu-id="96439-129">色彩外觀模型設定檔架構</span><span class="sxs-lookup"><span data-stu-id="96439-129">Color Appearance Model Profile Architecture</span></span>

![顯示 X M L 標記所組成之 CAMP 設定檔架構的圖表。](images/camp-image002new.png)

### <a name="the-camp-schema"></a><span data-ttu-id="96439-131">CAMP 架構</span><span class="sxs-lookup"><span data-stu-id="96439-131">The CAMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a><span data-ttu-id="96439-132">CAMP 架構元素</span><span class="sxs-lookup"><span data-stu-id="96439-132">The CAMP Schema Elements</span></span>

## <a name="colorappearancemodel"></a><span data-ttu-id="96439-133">ColorAppearanceModel</span><span class="sxs-lookup"><span data-stu-id="96439-133">ColorAppearanceModel</span></span>

<span data-ttu-id="96439-134">這個元素的順序如下：</span><span class="sxs-lookup"><span data-stu-id="96439-134">This element is a sequence of:</span></span>

1.  <span data-ttu-id="96439-135">ProfileName 字串，</span><span class="sxs-lookup"><span data-stu-id="96439-135">ProfileName string,</span></span>
2.  <span data-ttu-id="96439-136">選擇性描述字串，</span><span class="sxs-lookup"><span data-stu-id="96439-136">optional Description string,</span></span>
3.  <span data-ttu-id="96439-137">選用的作者字串，</span><span class="sxs-lookup"><span data-stu-id="96439-137">optional Author string,</span></span>
4.  <span data-ttu-id="96439-138">ViewingConditions 元素。</span><span class="sxs-lookup"><span data-stu-id="96439-138">ViewingConditions element.</span></span>

<span data-ttu-id="96439-139">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="96439-139">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="96439-140">字串長度限制為10000個字元。</span><span class="sxs-lookup"><span data-stu-id="96439-140">String lengths are limited to 10,000 characters.</span></span>

## <a name="namespace"></a><span data-ttu-id="96439-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="96439-141">Namespace</span></span>

<span data-ttu-id="96439-142">xmlns： cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="96439-142">xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

<span data-ttu-id="96439-143">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="96439-143">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

## <a name="version"></a><span data-ttu-id="96439-144">版本</span><span class="sxs-lookup"><span data-stu-id="96439-144">Version</span></span>

<span data-ttu-id="96439-145">&gt; &lt; 第一版的 Windows Vista 版本0.1 或 = "1.0"。</span><span class="sxs-lookup"><span data-stu-id="96439-145">Version &gt;0.1 or &lt;= "1.0" with the first release of Windows Vista.</span></span>

<span data-ttu-id="96439-146">**驗證條件：** 任何版本值 &lt; = 2.0 也都有效，可支援格式的非重大變更。</span><span class="sxs-lookup"><span data-stu-id="96439-146">**Validation conditions:** Any version value &lt;=2.0 is also valid to support non-breaking changes to the format.</span></span>

## <a name="documentation"></a><span data-ttu-id="96439-147">文件</span><span class="sxs-lookup"><span data-stu-id="96439-147">Documentation</span></span>

<span data-ttu-id="96439-148">色彩外觀模型設定檔架構。</span><span class="sxs-lookup"><span data-stu-id="96439-148">Color Appearance Model Profile Schema.</span></span>

<span data-ttu-id="96439-149">著作權 (C) Microsoft。</span><span class="sxs-lookup"><span data-stu-id="96439-149">Copyright (C) Microsoft.</span></span> <span data-ttu-id="96439-150">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="96439-150">All rights reserved.</span></span>

<span data-ttu-id="96439-151">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="96439-151">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="surroundtype"></a><span data-ttu-id="96439-152">SurroundType</span><span class="sxs-lookup"><span data-stu-id="96439-152">SurroundType</span></span>

<span data-ttu-id="96439-153">此元素為 "Average"、"Dim" 或 "深色" CIECAM02 參數的列舉，或 CIECAM02 建議 c 中的實際量化參數，即環繞的影響。</span><span class="sxs-lookup"><span data-stu-id="96439-153">This element is a either an enumeration of "Average," "Dim," or "Dark" CIECAM02 parameters or the actual quantitative parameters from the CIECAM02 recommendation c, impact of the surround.</span></span>

<span data-ttu-id="96439-154">**驗證條件：** C 參數的範圍可以從0.525 到0.69。</span><span class="sxs-lookup"><span data-stu-id="96439-154">**Validation conditions:** The c parameter can range from 0.525 to 0.69.</span></span>

## <a name="viewingconditions"></a><span data-ttu-id="96439-155">ViewingConditions</span><span class="sxs-lookup"><span data-stu-id="96439-155">ViewingConditions</span></span>

<span data-ttu-id="96439-156">此元素包含下列子項目：</span><span class="sxs-lookup"><span data-stu-id="96439-156">This element consists of the following sub-elements:</span></span>



| <span data-ttu-id="96439-157">元素</span><span class="sxs-lookup"><span data-stu-id="96439-157">Element</span></span>                    | <span data-ttu-id="96439-158">類型</span><span class="sxs-lookup"><span data-stu-id="96439-158">Type</span></span>           |
|----------------------------|----------------|
| <span data-ttu-id="96439-159">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="96439-159">WhitePoint</span></span>                 | <span data-ttu-id="96439-160">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="96439-160">WhitePointType</span></span> |
| <span data-ttu-id="96439-161">背景</span><span class="sxs-lookup"><span data-stu-id="96439-161">Background</span></span>                 | <span data-ttu-id="96439-162">CIEXYZ</span><span class="sxs-lookup"><span data-stu-id="96439-162">CIEXYZ</span></span>         |
| <span data-ttu-id="96439-163">環繞</span><span class="sxs-lookup"><span data-stu-id="96439-163">Surround</span></span>                   | <span data-ttu-id="96439-164">SurroundType</span><span class="sxs-lookup"><span data-stu-id="96439-164">SurroundType</span></span>   |
| <span data-ttu-id="96439-165">LuminanceOfAdaptingField</span><span class="sxs-lookup"><span data-stu-id="96439-165">LuminanceOfAdaptingField</span></span>   | <span data-ttu-id="96439-166">FLOAT</span><span class="sxs-lookup"><span data-stu-id="96439-166">float</span></span>          |
| <span data-ttu-id="96439-167">DegreeOfAdaptation</span><span class="sxs-lookup"><span data-stu-id="96439-167">DegreeOfAdaptation</span></span>         | <span data-ttu-id="96439-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="96439-168">float</span></span>          |
| <span data-ttu-id="96439-169">NormalizeToMediaWhitePoint</span><span class="sxs-lookup"><span data-stu-id="96439-169">NormalizeToMediaWhitePoint</span></span> | <span data-ttu-id="96439-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="96439-170">Boolean</span></span>        |



 

<span data-ttu-id="96439-171">**驗證條件：** CIEXYZ 子項目是由 NonNegativeXYZType 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="96439-171">**Validation conditions:** CIEXYZ sub-elements are validated by NonNegativeXYZType.</span></span> <span data-ttu-id="96439-172">LuminanceOfAdaptingField 的最大值為10，000cd/m ^ 2。</span><span class="sxs-lookup"><span data-stu-id="96439-172">The LuminanceOfAdaptingField is a maximum of 10,000cd/m^2.</span></span> <span data-ttu-id="96439-173">DegreeOfAdaptation 的範圍可以從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="96439-173">The DegreeOfAdaptation can range from 0.0 to 1.0.</span></span> <span data-ttu-id="96439-174">NormalizeToMediaWhitePoint 值可以是 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="96439-174">The NormalizeToMediaWhitePoint value can be either "true" or "false."</span></span> <span data-ttu-id="96439-175">如果 NormalizeToMediaWhitePoint 子項目不存在，就會有效地預設為 "true"。</span><span class="sxs-lookup"><span data-stu-id="96439-175">If the NormalizeToMediaWhitePoint sub-element is absent, it effectively defaults to "true."</span></span> <span data-ttu-id="96439-176">請參閱下列 CAMP 演算法一節。</span><span class="sxs-lookup"><span data-stu-id="96439-176">See the following CAMP algorithm section.</span></span>

## <a name="whitepointtype"></a><span data-ttu-id="96439-177">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="96439-177">WhitePointType</span></span>

<span data-ttu-id="96439-178">這個元素是 CIE 光源來源值的列舉 ( "D50"、"D65"、"A" 或 "F2" ) 或 CIEXYZ 子項目。</span><span class="sxs-lookup"><span data-stu-id="96439-178">This element is a either an enumeration of CIE light source value ("D50," "D65," "A," or "F2") or a CIEXYZ sub-element.</span></span>

<span data-ttu-id="96439-179">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="96439-179">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="ciexyztype"></a><span data-ttu-id="96439-180">CIEXYZType</span><span class="sxs-lookup"><span data-stu-id="96439-180">CIEXYZType</span></span>

<span data-ttu-id="96439-181">CIEXYZType 元素是由三個 NonNegativeFloatType 單精確度 IEEE 浮點元素所組成，名為 "X"、"Y" 和 "Z"。</span><span class="sxs-lookup"><span data-stu-id="96439-181">The CIEXYZType element is composed of three NonNegativeFloatType single-precision IEEE floating-point elements, named "X," "Y," and "Z."</span></span> <span data-ttu-id="96439-182">這些測量可以是絕對 (非相對) CIEXYZ 1931 反射值或絕對 (不是相對) CIEXYZ 1931 direct (transmissive) 值（每個計量平方單位）。</span><span class="sxs-lookup"><span data-stu-id="96439-182">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="96439-183">**驗證條件：** 這表示只有真實世界的值有效，且負值的 CIEXYZ 測量值無效。</span><span class="sxs-lookup"><span data-stu-id="96439-183">**Validation conditions:** This means that only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="96439-184">由於這些都是絕對值，因此值的範圍可能會超過 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="96439-184">Since these are absolute values, values can range well beyond 1.0f.</span></span> <span data-ttu-id="96439-185">任何 X、Y 或 Z 值的合理限制都將任意設定為 10000.0 f。</span><span class="sxs-lookup"><span data-stu-id="96439-185">A reasonable limit for any X, Y, or Z value will be arbitrarily set to 10000.0f.</span></span>

 

### <a name="the-camp-algorithm"></a><span data-ttu-id="96439-186">CAMP 演算法</span><span class="sxs-lookup"><span data-stu-id="96439-186">The CAMP Algorithm</span></span>

<span data-ttu-id="96439-187">色彩外觀模型 (凸輪) 是以 CIE CIECAM02 色彩外觀模型方程式為基礎。</span><span class="sxs-lookup"><span data-stu-id="96439-187">The color appearance model (CAM) is based on the CIE CIECAM02 color appearance model equations.</span></span>

<span data-ttu-id="96439-188">這個類別會實色外觀模型化。</span><span class="sxs-lookup"><span data-stu-id="96439-188">This class implements the color appearance modeling.</span></span> <span data-ttu-id="96439-189">請注意，WCS 凸輪 *無法* 取代，例如使用外掛程式。</span><span class="sxs-lookup"><span data-stu-id="96439-189">Note that the WCS CAM is *not* replaceable, for example, using a plug-in.</span></span> <span data-ttu-id="96439-190">它是一個設計目標，只能有一個色彩外觀模型。</span><span class="sxs-lookup"><span data-stu-id="96439-190">It is a design goal to have only one color appearance model.</span></span> <span data-ttu-id="96439-191">凸輪是以 CIECAM02 建議為基礎。</span><span class="sxs-lookup"><span data-stu-id="96439-191">The CAM is based on CIECAM02 recommendations.</span></span>

<span data-ttu-id="96439-192">CIECAM02 可以用兩種方式來使用。</span><span class="sxs-lookup"><span data-stu-id="96439-192">CIECAM02 can be used in two ways.</span></span> <span data-ttu-id="96439-193">在色階到外觀的方向中，它會提供從 CIE XYZ 空間到色彩外觀空間的對應。</span><span class="sxs-lookup"><span data-stu-id="96439-193">In the colorimetric-to-appearance direction, it provides a mapping from CIE XYZ space to color appearance space.</span></span> <span data-ttu-id="96439-194">在外觀為色度的方向中，它會將色彩外觀空間對應回 XYZ 空間。</span><span class="sxs-lookup"><span data-stu-id="96439-194">In the appearance-to-colorimetric direction, it maps from color appearance space back to XYZ space.</span></span> <span data-ttu-id="96439-195">色彩外觀會將亮度、J、色度、C 和色調（h）相互關聯。</span><span class="sxs-lookup"><span data-stu-id="96439-195">The color appearance correlates lightness, J, chroma, C, and hue, h.</span></span> <span data-ttu-id="96439-196">這三個值形成圓柱座標系統。</span><span class="sxs-lookup"><span data-stu-id="96439-196">These three values form a cylindrical coordinate system.</span></span> <span data-ttu-id="96439-197">通常，在矩形座標系統中工作變得更方便，因此計算 a = C cos h 和 b = C sin h，以提供 CIECAM02 Jab。</span><span class="sxs-lookup"><span data-stu-id="96439-197">Frequently, it turns out to be more convenient to work in a rectangular coordinate system, so compute a = C cos h and b = C sin h, to give CIECAM02 Jab.</span></span>

<span data-ttu-id="96439-198">您可以使用大於100的凸輪亮度值。</span><span class="sxs-lookup"><span data-stu-id="96439-198">You can use CAM lightness values greater than 100.</span></span> <span data-ttu-id="96439-199">採用 CIECAM02 的 CIE 委員會並未解決亮度軸的輸入值（亮度大於所採用的白色點）的行為;也就是，輸入 Y 值大於所採用的白色點 Y 值。</span><span class="sxs-lookup"><span data-stu-id="96439-199">The CIE committee that formulated CIECAM02 did not address the behavior of the lightness axis for input values with a luminance greater than the adopted white point; that is, for input Y values greater than the adopted white point Y value.</span></span> <span data-ttu-id="96439-200">測試已顯示 CIECAM02 中的亮度方程式對此類值的行為相當合理。</span><span class="sxs-lookup"><span data-stu-id="96439-200">Experimentation has shown that the luminance equations in CIECAM02 behave reasonably for such values.</span></span> <span data-ttu-id="96439-201">亮度會以指數方式增加，並遵循相同的指數 (大約 1/3) 。</span><span class="sxs-lookup"><span data-stu-id="96439-201">The lightness increases exponentially and follows the same exponent (roughly 1/3).</span></span>

<span data-ttu-id="96439-202">使用者有時會想要變更 (D) 的調整程度的計算方式。</span><span class="sxs-lookup"><span data-stu-id="96439-202">Users sometimes want to change the way that the degree of adaptation (D) is calculated.</span></span> <span data-ttu-id="96439-203">WCS 設計可讓使用者藉由變更查看條件參數中的 degreeOfadaptation 值來控制這項計算。</span><span class="sxs-lookup"><span data-stu-id="96439-203">The WCS design enables users to control this calculation by changing the degreeOfadaptation value in the viewing conditions parameters.</span></span>

<span data-ttu-id="96439-204">為了提供與使用者的 ICC 影響的預期更一致的相符，預設 CAMP 中的 degreeOfAdaptation 是1.0。</span><span class="sxs-lookup"><span data-stu-id="96439-204">To provide a more consistent match to users' ICC-influenced expectations, the degreeOfAdaptation in the default CAMPS is 1.0.</span></span> <span data-ttu-id="96439-205">這會在 MinCD 絕對以外的所有情況下產生更好的結果，其中一個可能會想要讓 WCS 透過 degreeOfAdaptation =-1) 來計算 degreeOfAdaptation (。</span><span class="sxs-lookup"><span data-stu-id="96439-205">This produces better results in all cases other than MinCD Absolute, where one might want to let WCS compute the degreeOfAdaptation (via degreeOfAdaptation = -1).</span></span>

<span data-ttu-id="96439-206">它不會使用「平均」、「維度」和「深色」的範圍值，而是會提供從值 c 計算的連續範圍值。</span><span class="sxs-lookup"><span data-stu-id="96439-206">Instead of using a surround value of "Average," "Dim," and "Dark," a continuous surround value, computed from the value c, is provided.</span></span> <span data-ttu-id="96439-207">C 的值必須是介於0.525 到0.69 之間的浮點數。</span><span class="sxs-lookup"><span data-stu-id="96439-207">The value of c must be a float between 0.525 and 0.69.</span></span>

<span data-ttu-id="96439-208">從 *c*、 *Nc* 和 *F* 可以計算，並在已提供給「平均」、「維度」和「深色」的值之間使用分段的線性插補。</span><span class="sxs-lookup"><span data-stu-id="96439-208">From *c*, *Nc* and *F* can be computed, using piecewise linear interpolation between the values already provided for "Average," "Dim," and "Dark."</span></span> <span data-ttu-id="96439-209">這是 CIE 159:2004 的 [圖 1] 所示的模型，即 CIECAM02 規格。</span><span class="sxs-lookup"><span data-stu-id="96439-209">This models what is shown in Figure 1 of CIE 159:2004, the CIECAM02 specification.</span></span>



| <span data-ttu-id="96439-210">degreeOfAdaption</span><span class="sxs-lookup"><span data-stu-id="96439-210">degreeOfAdaption</span></span>                     | <span data-ttu-id="96439-211">行為</span><span class="sxs-lookup"><span data-stu-id="96439-211">Behavior</span></span>                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="96439-212">-1.0</span><span class="sxs-lookup"><span data-stu-id="96439-212">-1.0</span></span>                                 | ![顯示預設 C I E C A M 02 行為的公式。](images/camp-image006.png)<span data-ttu-id="96439-214">這是預設的 CIECAM02 行為。</span><span class="sxs-lookup"><span data-stu-id="96439-214">This is the default CIECAM02 behavior.</span></span><br/> |
| <span data-ttu-id="96439-215">0.0 &lt; = degreeOfAdaption &lt; = 1。0</span><span class="sxs-lookup"><span data-stu-id="96439-215">0.0 &lt;= degreeOfAdaption &lt;= 1.0</span></span> | <span data-ttu-id="96439-216">*D* = degreeOfAdaptation (使用者提供的值) </span><span class="sxs-lookup"><span data-stu-id="96439-216">*D* = degreeOfAdaptation (the value supplied by the user)</span></span>                      |



 

<span data-ttu-id="96439-217">執行中也已加入特定的錯誤檢查量。</span><span class="sxs-lookup"><span data-stu-id="96439-217">A certain amount of error checking has also been added to the implementation.</span></span> <span data-ttu-id="96439-218">以下是在 CIECAM02 的 CIE 159:2004 定義中使用的方程式編號。</span><span class="sxs-lookup"><span data-stu-id="96439-218">The following equation numbers are those used in the CIE 159:2004 definition of CIECAM02.</span></span>

<span data-ttu-id="96439-219">**ColorimetricToAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="96439-219">**ColorimetricToAppearanceColors**</span></span>

<span data-ttu-id="96439-220">系統會檢查輸入值的合理：如果是 X 或 Z &lt; 0.0，或如果 &lt; 是 Y-1.0，則 HRESULT 為 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="96439-220">The input values are checked for reasonableness: If X or Z &lt; 0.0, or if Y &lt; -1.0, then the HRESULT is E\_INVALIDARG.</span></span> <span data-ttu-id="96439-221">如果-1.0 &lt; = Y &lt; 0.0，則 J、C 和 h 全都設定為0.0。</span><span class="sxs-lookup"><span data-stu-id="96439-221">If -1.0 &lt;= Y &lt; 0.0, then J, C, and h are all set to 0.0.</span></span>

<span data-ttu-id="96439-222">有些內部條件可能會產生錯誤結果。</span><span class="sxs-lookup"><span data-stu-id="96439-222">There are certain internal conditions that can produce error results.</span></span> <span data-ttu-id="96439-223">系統不會產生這樣的結果，而是會裁剪內部結果以產生範圍內的值。</span><span class="sxs-lookup"><span data-stu-id="96439-223">Instead of producing such results, the internal results are clipped to produce in-range values.</span></span> <span data-ttu-id="96439-224">這會發生在具有深色和非常彩色的色彩規格中：在方程式7.23 中，如果 &lt; 0，a = 0。</span><span class="sxs-lookup"><span data-stu-id="96439-224">This happens for specifications of colors that would be dark and impossibly chromatic: In equation 7.23, if A &lt; 0, A = 0.</span></span> <span data-ttu-id="96439-225">在方程式7.26 中，如果 t &lt; 0，t = 0。</span><span class="sxs-lookup"><span data-stu-id="96439-225">In equation 7.26, if t &lt; 0, t = 0.</span></span>

<span data-ttu-id="96439-226">**AppearanceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="96439-226">**AppearanceToColorimetricColors**</span></span>

<span data-ttu-id="96439-227">系統會檢查輸入值是否有合理。</span><span class="sxs-lookup"><span data-stu-id="96439-227">The input values are checked for reasonableness.</span></span> <span data-ttu-id="96439-228">如果 &lt; 是 c 0、C &gt; 300 或 J &gt; 500，則 HRESULT 為 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="96439-228">If C &lt; 0 , C &gt; 300, or J &gt; 500, then the HRESULT is E\_INVALIDARG.</span></span>

<span data-ttu-id="96439-229">*R '<sub>a;</sub>*、 *G '<sub>a;</sub>* 和 *B '<sub>a;</sub>*， (方 8.19-8.21) 會裁剪至範圍399.9。</span><span class="sxs-lookup"><span data-stu-id="96439-229">*R'<sub>a;</sub>*, *G'<sub>a;</sub>*, and *B'<sub>a;</sub>*, (equations 8.19 - 8.21) are clipped to the range   399.9 .</span></span>

<span data-ttu-id="96439-230">針對所有色彩外觀模型設定檔 (Camp) ，WCS 引擎會檢查採用的白色點。</span><span class="sxs-lookup"><span data-stu-id="96439-230">For all Color Appearance Model Profiles (CAMPs), the WCS engine will examine the adopted white point.</span></span> <span data-ttu-id="96439-231">如果 Y 不是100.0，則會調整採用的白色點，讓 Y 等於100.0。</span><span class="sxs-lookup"><span data-stu-id="96439-231">If Y is not 100.0, then the adopted white point will be scaled so that Y does equal 100.0.</span></span> <span data-ttu-id="96439-232">相同的縮放比例將會套用至背景值。</span><span class="sxs-lookup"><span data-stu-id="96439-232">The same scaling will be applied to the background value.</span></span> <span data-ttu-id="96439-233">調整因數為 100.0/adoptedWhitePoint。 Y。</span><span class="sxs-lookup"><span data-stu-id="96439-233">The scaling factor is 100.0/adoptedWhitePoint.Y.</span></span> <span data-ttu-id="96439-234">相同的縮放比例會套用至每個 X、Y 和 Z。如果 NormalizeToMediaWhitePoint 欄位設定為 "True"，或 CAMP 中沒有該欄位，則引擎也會將所有裝置色彩輸入調整為 DeviceToColorimetric，讓裝置媒體的 Y 值等於100.0。</span><span class="sxs-lookup"><span data-stu-id="96439-234">The same scaling factor is applied to each of X, Y, and Z. If the NormalizeToMediaWhitePoint field is set to "True," or if it is absent from the CAMP, the engine also scales all device colors input to DeviceToColorimetric so that the Y value of the device media white point equals 100.0.</span></span> <span data-ttu-id="96439-235">來自 ColorimetricToDevice 的裝置色彩將會以該縮放比例的乘法反向縮放。</span><span class="sxs-lookup"><span data-stu-id="96439-235">Device colors coming from ColorimetricToDevice will be scaled by the multiplicative inverse of that scaling factor.</span></span> <span data-ttu-id="96439-236">如果 [NormalizeToMediaWhitePoint] 旗標設定為 [False]，則不會調整色度資料。</span><span class="sxs-lookup"><span data-stu-id="96439-236">If the NormalizeToMediaWhitePoint flag is set to "False," then the colorimetric data is not scaled.</span></span>

<span data-ttu-id="96439-237">針對某些工作，調整來自 DeviceToColorimetric 的色度值是合理的。</span><span class="sxs-lookup"><span data-stu-id="96439-237">For some tasks, it makes sense to scale the colorimetric values coming from DeviceToColorimetric.</span></span> <span data-ttu-id="96439-238">凸輪中的雙曲亮度方程式實際上是針對100.0 的白色點亮度所設計。</span><span class="sxs-lookup"><span data-stu-id="96439-238">The hyperbolic lightness equations in the CAM are really designed for a white point luminance of 100.0.</span></span> <span data-ttu-id="96439-239">絕對亮度 (或 illuminance) 差異的唯一位置是在 [調整] 欄位的亮度中。</span><span class="sxs-lookup"><span data-stu-id="96439-239">The only place where a difference in the absolute luminance (or illuminance) comes into play is in the luminance of the adapting field.</span></span> <span data-ttu-id="96439-240">因此，必須使用100.0 的白色點來初始化凸輪。</span><span class="sxs-lookup"><span data-stu-id="96439-240">So the CAM must be initialized with a white point Y of 100.0.</span></span> <span data-ttu-id="96439-241">但是，如果裝置型號的中等白色點正當做採用的白色點使用，則來自裝置的所有色彩都必須據以調整，否則裝置的白色將不會有 J 值100.0。</span><span class="sxs-lookup"><span data-stu-id="96439-241">But if the device model's medium white point is being used as the adopted white point, then all colors coming from the device must be scaled accordingly, or device white will not come out with a J value of 100.0.</span></span> <span data-ttu-id="96439-242">因此，Y 值必須在度量中縮放。</span><span class="sxs-lookup"><span data-stu-id="96439-242">So the Y values have to be scaled in the measurements.</span></span> <span data-ttu-id="96439-243">您可以調整測量值，再將裝置模型初始化。</span><span class="sxs-lookup"><span data-stu-id="96439-243">The measurement values could be scaled before initializing the device model.</span></span> <span data-ttu-id="96439-244">然後，結果會在適當的範圍內。</span><span class="sxs-lookup"><span data-stu-id="96439-244">Then results would already be in the proper range.</span></span> <span data-ttu-id="96439-245">但這會讓測試裝置模型變得更困難，因為即將推出的值需要調整。</span><span class="sxs-lookup"><span data-stu-id="96439-245">But that would make testing the device model more difficult, because the values coming out would require scaling.</span></span> <span data-ttu-id="96439-246">針對裝置媒體的白色點會被認為是真正白色的工作，則需要依裝置媒體的白色點進行正規化。</span><span class="sxs-lookup"><span data-stu-id="96439-246">For tasks in which the device medium white point is perceived to be a true white, normalizing by the device media white point is desirable.</span></span>

<span data-ttu-id="96439-247">凸輪會直接從 CAMP 初始化。</span><span class="sxs-lookup"><span data-stu-id="96439-247">The CAM is initialized directly from the CAMP.</span></span> <span data-ttu-id="96439-248">這可讓開發人員根據所要執行的工作，在初始化凸輪時有彈性。</span><span class="sxs-lookup"><span data-stu-id="96439-248">This allows developers some flexibility in initializing the CAM, based upon the task they want to perform.</span></span> <span data-ttu-id="96439-249">在某些工作中，觀察者會忽略媒體白名單中的任何色度，因為它們 cognitively 「知道」來源和目的地媒體都是「白色」。</span><span class="sxs-lookup"><span data-stu-id="96439-249">In some tasks, observers will ignore any chroma in the media white points, because they cognitively "know" that the source and destination media are "white."</span></span> <span data-ttu-id="96439-250">在這種情況下，開發人員會想要使用各自的媒體重點來初始化向前和反向攝影機。</span><span class="sxs-lookup"><span data-stu-id="96439-250">In such cases, developers will want to initialize the forward and inverse CAMs with their respective media white points.</span></span> <span data-ttu-id="96439-251">在某些情況下，觀察者可能會比較媒體背景的色彩。</span><span class="sxs-lookup"><span data-stu-id="96439-251">In some cases, observers may be comparing the color of the media backgrounds.</span></span> <span data-ttu-id="96439-252">在這些情況下，建議您對這兩個裝置使用一個 CAM，而不想要根據裝置的中等白色點來調整每個裝置的色度值。</span><span class="sxs-lookup"><span data-stu-id="96439-252">In these cases, it is advisable to use one CAM for both devices, and it may be desirable not to scale each device's colorimetric values by that device's medium white point.</span></span> <span data-ttu-id="96439-253">然後，媒體的不同 tristimulus 值會導致 CIECAM02 中的不同外觀值。</span><span class="sxs-lookup"><span data-stu-id="96439-253">Then the different tristimulus values of the media will lead to different appearance values in CIECAM02.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96439-254">相關主題</span><span class="sxs-lookup"><span data-stu-id="96439-254">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96439-255">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="96439-255">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="96439-256">Windows 色彩系統架構和演算法</span><span class="sxs-lookup"><span data-stu-id="96439-256">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





