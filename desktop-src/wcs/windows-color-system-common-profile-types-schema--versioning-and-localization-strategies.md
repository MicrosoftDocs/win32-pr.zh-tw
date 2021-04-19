---
title: Windows Color System 一般配置檔案類型架構、版本控制和當地語系化策略
description: Windows Color System 一般配置檔案類型架構、版本控制和當地語系化策略
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Windows Color System (WCS) ，一般配置檔案類型
- WCS (Windows 色彩系統) ，一般配置檔案類型
- 影像色彩管理，一般配置檔案類型
- 色彩管理，一般配置檔案類型
- 色彩，一般配置檔案類型
- Windows Color System (WCS) ，設定檔
- WCS (Windows 色彩系統) ，設定檔
- 影像色彩管理，設定檔
- 色彩管理，設定檔
- 色彩，設定檔
- Windows Color System (WCS) ，版本控制
- WCS (Windows 色彩系統) ，版本控制
- 影像色彩管理，版本控制
- 色彩管理，版本控制
- 色彩，版本控制
- Windows Color System (WCS) ，當地語系化
- WCS (Windows 色彩系統) ，當地語系化
- 影像色彩管理，當地語系化
- 色彩管理，當地語系化
- 色彩，當地語系化
- WCS 一般配置檔案類型
- 分析取用者
- 一般配置檔案類型
- 架構，一般配置檔案類型
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814b652b654b6416b42a7a3484950273a93ea96
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106982822"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a><span data-ttu-id="c29e5-127">Windows Color System 一般配置檔案類型架構、版本控制和當地語系化策略</span><span class="sxs-lookup"><span data-stu-id="c29e5-127">Windows Color System Common Profile Types schema, Versioning and Localization Strategies</span></span>

-   [<span data-ttu-id="c29e5-128">WCS 一般配置檔案類型架構 V1</span><span class="sxs-lookup"><span data-stu-id="c29e5-128">WCS Common Profile Types Schema V1</span></span>](#wcs-common-profile-types-schema-v1)
-   [<span data-ttu-id="c29e5-129">WCS 一般配置檔案類型架構 V2 新增專案</span><span class="sxs-lookup"><span data-stu-id="c29e5-129">WCS Common Profile Types Schema V2 Additions</span></span>](#wcs-common-profile-types-schema-v2-additions)
-   [<span data-ttu-id="c29e5-130">WCS 設定檔架構版本控制</span><span class="sxs-lookup"><span data-stu-id="c29e5-130">WCS Profile Schema Versioning</span></span>](#wcs-profile-schema-versioning)
-   [<span data-ttu-id="c29e5-131">WCS 設定檔當地語系化</span><span class="sxs-lookup"><span data-stu-id="c29e5-131">WCS Profile Localization</span></span>](#wcs-profile-localization)
    -   [<span data-ttu-id="c29e5-132">表示可當地語系化的元素</span><span class="sxs-lookup"><span data-stu-id="c29e5-132">Expressing localizable elements</span></span>](#expressing-localizable-elements)
    -   [<span data-ttu-id="c29e5-133">架構支援</span><span class="sxs-lookup"><span data-stu-id="c29e5-133">Schema Support</span></span>](#schema-support)
    -   [<span data-ttu-id="c29e5-134">選取語言</span><span class="sxs-lookup"><span data-stu-id="c29e5-134">Selecting the Language</span></span>](#selecting-the-language)
    -   [<span data-ttu-id="c29e5-135">內建設定檔</span><span class="sxs-lookup"><span data-stu-id="c29e5-135">Built-in profiles</span></span>](#built-in-profiles)
-   [<span data-ttu-id="c29e5-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="c29e5-136">Related topics</span></span>](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a><span data-ttu-id="c29e5-137">WCS 一般配置檔案類型架構 V1</span><span class="sxs-lookup"><span data-stu-id="c29e5-137">WCS Common Profile Types Schema V1</span></span>

<span data-ttu-id="c29e5-138">以下提供適用于 WCS 一般配置檔案類型的 v1.0 架構定義。</span><span class="sxs-lookup"><span data-stu-id="c29e5-138">The following provides the v1.0 schema definition for the WCS Common Profile Types.</span></span>


```XML
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:import namespace="http://www.w3.org/XML/1998/namespace" />

  <xs:annotation>
    <xs:documentation xml:lang="en">
      Common types used in WCS profile schemas.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:simpleType name="NonNegativeFloatType">
    <xs:restriction base="xs:float">
      <xs:minInclusive value="0"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="NonNegativeCIEXYZType">
    <xs:attribute name="X" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Z" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="LocalizedTextType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute ref="xml:lang" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="MultiLocalizedTextType">
    <xs:sequence>
      <xs:element name="Text" type="wcs:LocalizedTextType" minOccurs="1" />
    </xs:sequence>
  </xs:complexType>

</xs:schema>

```



<span data-ttu-id="c29e5-139">僅支援 UTF-8 或 UTF-16 編碼。</span><span class="sxs-lookup"><span data-stu-id="c29e5-139">Only UTF-8 or UTF-16 encodings are supported.</span></span> <span data-ttu-id="c29e5-140">強烈建議您不要採用所有其他 XML 編碼，以保持最佳互通性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-140">All other XML encodings are strongly discouraged in order to preserve optimum interoperability.</span></span>

## <a name="wcs-common-profile-types-schema-v2-additions"></a><span data-ttu-id="c29e5-141">WCS 一般配置檔案類型架構 V2 新增專案</span><span class="sxs-lookup"><span data-stu-id="c29e5-141">WCS Common Profile Types Schema V2 Additions</span></span>

<span data-ttu-id="c29e5-142">在 Windows 7 中，已更新 WCS 一般配置檔案類型架構，以包含支援 [WCS 校正架構](wcs-calibration-schema.md)的類型。</span><span class="sxs-lookup"><span data-stu-id="c29e5-142">In Windows 7, the WCS Common Profile Types schema has been updated to include types to support the [WCS Calibration schema](wcs-calibration-schema.md).</span></span>


```XML
  <xs:complexType name="ParameterizedCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="GreenTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="BlueTRC" type="wcs:ParameterizedCurveType"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="ParameterizedCurveType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset1" type="xs:float" use="optional"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset2" type="xs:float " use="optional"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset3" type="xs:float" use="optional"/>
  </xs:complexType>

  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="wcs:FloatList"/>
      <xs:element name="Output" type="wcs:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="wcs:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="2" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
```



## <a name="wcs-profile-schema-versioning"></a><span data-ttu-id="c29e5-143">WCS 設定檔架構版本控制</span><span class="sxs-lookup"><span data-stu-id="c29e5-143">WCS Profile Schema Versioning</span></span>

<span data-ttu-id="c29e5-144">在此附錄中，「設定檔取用者」一詞是指 WCS 軟體或使用 WCS 設定檔的協力廠商軟體元件。</span><span class="sxs-lookup"><span data-stu-id="c29e5-144">In this Appendix, the term "profile consumer" refers to the WCS software, or to a third-party software component that consumes WCS profiles.</span></span>

<span data-ttu-id="c29e5-145">較新版本的設定檔取用者將能夠取用根據舊版架構所撰寫的 WCS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c29e5-145">Newer versions of profile consumers will be able to consume WCS profiles written according to older versions of the schemas.</span></span> <span data-ttu-id="c29e5-146">若要充分利用最新的架構版本中定義的功能，通常會需要最新版本的設定檔取用者。</span><span class="sxs-lookup"><span data-stu-id="c29e5-146">To take full advantage of features defined in the newest version of the schemas, the newest version of a profile consumer will generally be required.</span></span> <span data-ttu-id="c29e5-147">不過，較舊的設定檔取用者可以取用根據較新版本的架構所撰寫的設定檔。</span><span class="sxs-lookup"><span data-stu-id="c29e5-147">However, older profile consumers can consume profiles written according to newer versions of the schemas.</span></span> <span data-ttu-id="c29e5-148">設定檔取用者可以忽略它不了解的 XML 元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-148">The profile consumer can ignore XML elements and attributes that it does not understand.</span></span> <span data-ttu-id="c29e5-149">結果會是正確的，但相較于最新版本的設定檔取用者所達成的結果，效能或精確度可能會降低。</span><span class="sxs-lookup"><span data-stu-id="c29e5-149">The results will be correct, but performance or fidelity may degraded as compared to the results achieved with the newest version of the profile consumer.</span></span>

<span data-ttu-id="c29e5-150">以下是設定檔取用者的版本控制方針：</span><span class="sxs-lookup"><span data-stu-id="c29e5-150">The following are versioning guidelines for profile consumers:</span></span>

-   <span data-ttu-id="c29e5-151">指定的設定檔取用者版本，必須從版本命名空間辨識所有元素和屬性，或全部都不是。</span><span class="sxs-lookup"><span data-stu-id="c29e5-151">A given version of a profile consumer must recognize either all of the elements and attributes from a version namespace, or none of them.</span></span>
-   <span data-ttu-id="c29e5-152">如果設定檔取用者遇到不了解的命名空間中的專案或屬性，則必須將它視為錯誤狀況，除非設定檔包含有關回退處理的明確指引。</span><span class="sxs-lookup"><span data-stu-id="c29e5-152">If a profile consumer encounters an element or attribute from a namespace that it does not understand, it must treat this as an error condition, unless the profile contains explicit guidance on fallback processing.</span></span>
-   <span data-ttu-id="c29e5-153">[開放式封裝規格](https://www.microsoft.com/whdc/xps/xpspkg.mspx)會定義其他命名空間 URI （標記相容性命名空間），以定義提供此回溯處理指引的元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-153">The [Open Packaging Specification](https://www.microsoft.com/whdc/xps/xpspkg.mspx) defines an additional namespace URI, the markup compatibility namespace, which defines elements and attributes that provide this fallback processing guidance.</span></span>
-   <span data-ttu-id="c29e5-154">所有設定檔取用者的所有版本都必須辨識並遵守標記相容性命名空間中的所有元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-154">All versions of all profile consumers must recognize and respect all the elements and attributes in the markup compatibility namespace.</span></span>
-   <span data-ttu-id="c29e5-155">以新版本的設定檔架構為基礎的分析取用者必須支援所有先前定義的版本命名空間。</span><span class="sxs-lookup"><span data-stu-id="c29e5-155">Profile consumers based on a new version of the profile schemas must support all previously defined version namespaces.</span></span>

<span data-ttu-id="c29e5-156">在1.0 版中，WCS 會辨識下列命名空間中的元素和屬性：</span><span class="sxs-lookup"><span data-stu-id="c29e5-156">In the v1.0 release, WCS recognizes elements and attributes from the following namespaces:</span></span>

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

<span data-ttu-id="c29e5-157">以下示範標記相容性的範例。</span><span class="sxs-lookup"><span data-stu-id="c29e5-157">The following demonstrates an example of markup compatibility.</span></span>


```XML
<?xml version="1.0" encoding="utf-8" ?>
<ColorAppearanceModel
  xmlns=http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
  xmlns:cam2=http://schemas.microsoft.com/windows/2007/08/color/ColorAppearanceModel
  xmlns:mc=http://schemas.microsoft.com/winfx/2005/02/markup-compatibility
  xs:schemaLocation="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel ColorAppearanceModel.xsd"
  xmlns:xs='http://www.w3.org/2001/XMLSchema-instance'
  mc:Ignorable="cam2">

  <ProfileName>Default profile for ICC viewing conditions</ProfileName>
  <mc:AlternateContent>
    <mc:Choice Requires="cam2">
      <cam2:AudioDescription source="ProfileExplanation.wav"/>
    </mc:Choice>
    <mc:Fallback>
      <Description>Appropriate for a print in a D50 viewing booth</Description>
        </mc:Fallback>
  </mc:AlternateContent>
  <Author>Microsoft</Author>

  <ViewingConditions>
    <WhitePointName>D50</WhitePointName>
    <Background X="19.3" Y="20.0" Z="16.5" />
    <Surround>Average</Surround>
    <LuminanceOfAdaptingField>31.8</LuminanceOfAdaptingField>
    <DegreeOfAdaptation>-1</DegreeOfAdaptation>
    <cam2:Humidity>30%</cam2:Humidity>
  </ViewingConditions>

</ColorAppearanceModel>
```



## <a name="wcs-profile-localization"></a><span data-ttu-id="c29e5-158">WCS 設定檔當地語系化</span><span class="sxs-lookup"><span data-stu-id="c29e5-158">WCS Profile Localization</span></span>

<span data-ttu-id="c29e5-159">**需求**</span><span class="sxs-lookup"><span data-stu-id="c29e5-159">**Requirements**</span></span>

<span data-ttu-id="c29e5-160">WCS 設定檔包含某些元素，例如 ProfileName 和描述，其中包含人們看得懂的文字。</span><span class="sxs-lookup"><span data-stu-id="c29e5-160">WCS profiles contain certain elements such as ProfileName and Description which contain human-readable text.</span></span> <span data-ttu-id="c29e5-161">這是可當地語系化的文字。</span><span class="sxs-lookup"><span data-stu-id="c29e5-161">This text is localizable.</span></span>

<span data-ttu-id="c29e5-162">以下是設定檔建立者的版本控制指導方針：</span><span class="sxs-lookup"><span data-stu-id="c29e5-162">The following are versioning guidelines for profile creators:</span></span>

-   <span data-ttu-id="c29e5-163">針對由協力廠商所建立的設定檔（例如印表機製造商），設定檔作者應納入多種語言的描述性文字。</span><span class="sxs-lookup"><span data-stu-id="c29e5-163">For profiles created by 3rd parties such as printer manufacturers, the profile author should incorporate descriptive text in multiple languages.</span></span>
-   <span data-ttu-id="c29e5-164">下列元素應可當地語系化：</span><span class="sxs-lookup"><span data-stu-id="c29e5-164">The following elements should be localizable:</span></span> 

    | <span data-ttu-id="c29e5-165">元素</span><span class="sxs-lookup"><span data-stu-id="c29e5-165">Element</span></span>     | <span data-ttu-id="c29e5-166">CDMP</span><span class="sxs-lookup"><span data-stu-id="c29e5-166">CDMP</span></span> | <span data-ttu-id="c29e5-167">GMMP</span><span class="sxs-lookup"><span data-stu-id="c29e5-167">GMMP</span></span> | <span data-ttu-id="c29e5-168">營地</span><span class="sxs-lookup"><span data-stu-id="c29e5-168">CAMP</span></span> |
    |-------------|------|------|------|
    | <span data-ttu-id="c29e5-169">ProfileName</span><span class="sxs-lookup"><span data-stu-id="c29e5-169">ProfileName</span></span> | <span data-ttu-id="c29e5-170">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-170">x</span></span>    | <span data-ttu-id="c29e5-171">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-171">x</span></span>    | <span data-ttu-id="c29e5-172">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-172">x</span></span>    |
    | <span data-ttu-id="c29e5-173">Description</span><span class="sxs-lookup"><span data-stu-id="c29e5-173">Description</span></span> | <span data-ttu-id="c29e5-174">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-174">x</span></span>    | <span data-ttu-id="c29e5-175">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-175">x</span></span>    | <span data-ttu-id="c29e5-176">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-176">x</span></span>    |
    | <span data-ttu-id="c29e5-177">作者</span><span class="sxs-lookup"><span data-stu-id="c29e5-177">Author</span></span>      | <span data-ttu-id="c29e5-178">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-178">x</span></span>    | <span data-ttu-id="c29e5-179">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-179">x</span></span>    | <span data-ttu-id="c29e5-180">x</span><span class="sxs-lookup"><span data-stu-id="c29e5-180">x</span></span>    |

    

     

### <a name="expressing-localizable-elements"></a><span data-ttu-id="c29e5-181">表示可當地語系化的元素</span><span class="sxs-lookup"><span data-stu-id="c29e5-181">Expressing localizable elements</span></span>

<span data-ttu-id="c29e5-182">每個可當地語系化的元素都包含一或多個 wcs： Text 子項目，而不是直接包含文字，而每個專案都必須指定 xml： lang 屬性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-182">Instead of directly containing text, each localizable element contains one or more wcs:Text sub-elements, each of which must specify the xml:lang attribute.</span></span> <span data-ttu-id="c29e5-183">如 [xml 規格](http://www.w3.org/TR/REC-xml/) 區段 2.12 ( 「語言識別」 ) 所述，xml： lang 屬性的值必須是 IETF RFC 3066 語言識別項，例如 "en-us"、"en" 或 "fr-fr"。</span><span class="sxs-lookup"><span data-stu-id="c29e5-183">As described in the [XML specification](http://www.w3.org/TR/REC-xml/) Section 2.12 ("Language Identification"), the value of the xml:lang attribute must be an IETF RFC 3066 language identifier such as "en-US", "en", or "fr-FR".</span></span> <span data-ttu-id="c29e5-184">在 WCS 架構中，xml： lang 屬性的值不能是空字串 ""，即使 XML 在一般情況下允許這種情況也一樣。</span><span class="sxs-lookup"><span data-stu-id="c29e5-184">In WCS schemas, the value of the xml:lang attribute must not be the empty string "", even though XML allows this in the general case.</span></span> <span data-ttu-id="c29e5-185">例如：</span><span class="sxs-lookup"><span data-stu-id="c29e5-185">For example:</span></span>


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



<span data-ttu-id="c29e5-186">沒有兩個 wcs： Text 元素可以有相同的 xml： lang 屬性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-186">No two wcs:Text elements can have the same xml:lang attribute.</span></span> <span data-ttu-id="c29e5-187">每個 WCS 設定檔架構都必須針對每個可當地語系化的元素分別強制執行這個條件約束。</span><span class="sxs-lookup"><span data-stu-id="c29e5-187">Each WCS profile schema must enforce this constraint separately for each localizable element.</span></span> <span data-ttu-id="c29e5-188">僅支援 UTF-8 與 UTF-16 編碼。</span><span class="sxs-lookup"><span data-stu-id="c29e5-188">Only UTF-8 and UTF-16 encodings are supported.</span></span>

### <a name="schema-support"></a><span data-ttu-id="c29e5-189">架構支援</span><span class="sxs-lookup"><span data-stu-id="c29e5-189">Schema Support</span></span>

<span data-ttu-id="c29e5-190">此設計利用 WCS 一般配置檔案類型架構中定義的 XSD 類型 wcs： LocalizedText 和 wcs： MultiLocalizedType：</span><span class="sxs-lookup"><span data-stu-id="c29e5-190">The design makes use of the XSD types wcs:LocalizedText and wcs:MultiLocalizedType defined in the WCS Common Profile Type schema:</span></span>


```XML
    <xs:complexType name="LocalizedText">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="xml:lang" type="xs:string" use="required"/>
            <xs:extension/>
        <xs:simpleContent/>
    </xs:complexType/>

    <xs:complexType name="MultiLocalizedType">
        <xs:element name="Text" type="cam:LocalizedText" minOccurs="1"/>
    </xs:complexType>
```



<span data-ttu-id="c29e5-191">每個 WCS 設定檔架構都會將每個可當地語系化的專案宣告為類型 MultiLocalizedType，例如：</span><span class="sxs-lookup"><span data-stu-id="c29e5-191">Each WCS profile schema declares each localizable element to be of type MultiLocalizedType, for example:</span></span>


```XML
<xs:schema 
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
    targetNamespace=
        "http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    version="1.0">
    <xs:import namespace=
        "http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"/>

    <xs:element name="cdm:Description" type="wcs:MultiLocalizableType" minOccurs="0"/>

    <xs:unique name="uniqueDescriptionLanguage">
      <xs:selector xpath="cdm:ColorDeviceModel/cdm:Description/wcs:Text"/>
      <xs:field xpath="@xml:lang"/>
    </unique>

    ...
</xs:schema>
```



<span data-ttu-id="c29e5-192">CDMP 架構會強制執行 cdm： Description 元素的每個 wcs： Text 子系必須有唯一的 xml： lang 屬性的條件約束。</span><span class="sxs-lookup"><span data-stu-id="c29e5-192">The CDMP schema enforces the constraint that each wcs:Text child of the cdm:Description element must have a unique xml:lang attribute.</span></span> <span data-ttu-id="c29e5-193">它會對其他可當地語系化的元素強制執行相同的條件約束。</span><span class="sxs-lookup"><span data-stu-id="c29e5-193">It enforces the same constraint for the other localizable elements.</span></span> <span data-ttu-id="c29e5-194">CAMP 和 GMMP 架構也相同。</span><span class="sxs-lookup"><span data-stu-id="c29e5-194">The CAMP and GMMP schemas do the same.</span></span>

### <a name="selecting-the-language"></a><span data-ttu-id="c29e5-195">選取語言</span><span class="sxs-lookup"><span data-stu-id="c29e5-195">Selecting the Language</span></span>

<span data-ttu-id="c29e5-196">當您決定要顯示之可當地語系化專案的語言版本時，應用程式程式碼應該選取「最接近的版本」至「目前的語言」。</span><span class="sxs-lookup"><span data-stu-id="c29e5-196">When deciding which language version of a localizable element to display, application code should select the "closest version" to the "current language".</span></span> <span data-ttu-id="c29e5-197">「最接近的版本」和「目前語言」真正的意義是與平臺相依;請參閱下文。</span><span class="sxs-lookup"><span data-stu-id="c29e5-197">What "closest version" and "current language" actually mean is platform-dependent; see below.</span></span> <span data-ttu-id="c29e5-198">如果設定檔不包含符合目前語言的語言版本，則應用程式應該選取設定檔中的第一個版本， (可當地語系化元素) 的第一個 wcs： Text 子項目。</span><span class="sxs-lookup"><span data-stu-id="c29e5-198">If the profile does not contain a language version that matches the current language, the application should select the first version in the profile (the first wcs:Text child element of the localizable element).</span></span>

<span data-ttu-id="c29e5-199">在 Windows Vista 上，語言選擇的完成方式如下：每個執行緒都有相關聯的「慣用 UI 語言」清單，可透過呼叫 [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages)來取得。</span><span class="sxs-lookup"><span data-stu-id="c29e5-199">On Windows Vista, the language selection is done as follows: Each thread has an associated list of "preferred UI languages", which can be obtained by calling [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span></span> <span data-ttu-id="c29e5-200">此清單會依使用者喜好設定順序傳回。</span><span class="sxs-lookup"><span data-stu-id="c29e5-200">The list is returned in order of user preference.</span></span> <span data-ttu-id="c29e5-201">比方說，在設定為美式英文的系統上， **GetThreadPreferredUILanguages** 傳回的清單是 {"en-us"，"en"}。</span><span class="sxs-lookup"><span data-stu-id="c29e5-201">For instance, on a system set up for US English, the list returned by **GetThreadPreferredUILanguages** is { "en-US", "en" }.</span></span> <span data-ttu-id="c29e5-202">這表示： 1) 美式英文（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="c29e5-202">This means: 1) US English if present.</span></span> <span data-ttu-id="c29e5-203">2) 否則，請使用英文的任何區域性變化，例如 "en-us" 或單純的 "en"。</span><span class="sxs-lookup"><span data-stu-id="c29e5-203">2) Otherwise, use any regional variant of English, such as "en-GB" or just plain "en".</span></span>

<span data-ttu-id="c29e5-204">針對清單中的每個語言，在清單順序中，UI 程式碼會尋找其 xml： lang 屬性完全相符的 wcs： Text 元素。</span><span class="sxs-lookup"><span data-stu-id="c29e5-204">For each language in that list, in list order, the UI code looks for a wcs:Text element whose xml:lang attribute is an exact match.</span></span> <span data-ttu-id="c29e5-205">使用第一個相符的版本。</span><span class="sxs-lookup"><span data-stu-id="c29e5-205">The first matching version is used.</span></span> <span data-ttu-id="c29e5-206">如果沒有版本符合，則會使用第一個 wcs： Text 元素。</span><span class="sxs-lookup"><span data-stu-id="c29e5-206">If no version matches, the first wcs:Text element is used.</span></span>

### <a name="built-in-profiles"></a><span data-ttu-id="c29e5-207">內建設定檔</span><span class="sxs-lookup"><span data-stu-id="c29e5-207">Built-in profiles</span></span>

<span data-ttu-id="c29e5-208">Windows Vista 隨附的標準 WCS 設定檔（例如 sRGB. cdmp）具有與其他設定檔相同的可當地語系化屬性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-208">The standard WCS profiles shipped with Windows Vista, such as sRGB.cdmp, have the same localizable properties as other profiles.</span></span>

<span data-ttu-id="c29e5-209">標準 Windows 方案是將當地語系化的字串放在 MUI DLL 中，並將其參考如下：</span><span class="sxs-lookup"><span data-stu-id="c29e5-209">The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:</span></span>


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



<span data-ttu-id="c29e5-210">在 Windows 系統上，描述文字會從適當當地語系化版本的 MUI 資源的資源識別碼101中解壓縮，以進行 mscms.dll。</span><span class="sxs-lookup"><span data-stu-id="c29e5-210">On a Windows system, the description text would be extracted from resource ID 101 in the appropriate localized version of the MUI resources for mscms.dll.</span></span> <span data-ttu-id="c29e5-211">非 Windows 系統會使用 wcs： Text 子項目，如上所述。</span><span class="sxs-lookup"><span data-stu-id="c29e5-211">Non-Windows systems would use the wcs:Text sub-elements as described above.</span></span>

<span data-ttu-id="c29e5-212">我們在每個 WCS 設定檔架構的根項目上引進一個選擇性的全域唯一識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="c29e5-212">We introduce an optional, globally unique ID attribute on the root element of each WCS profile schema.</span></span> <span data-ttu-id="c29e5-213">標準設定檔 wcsRGB. cdmp 看起來可能像這樣：</span><span class="sxs-lookup"><span data-stu-id="c29e5-213">The standard profile wcsRGB.cdmp might look like this:</span></span>


```XML
<cdm:ColorDeviceModel
    ID=http://schemas.microsoft.com/2005/02/color/profiles/wcsRGB.cdmp
    ... >
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello.</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour.</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceModel>
```



<span data-ttu-id="c29e5-214">在 windows 隨附的 WCS 色彩設定檔中，色彩 CPL 會顯示資源中的描述性資訊，而不是來自設定檔中的 wcs： Text 元素。</span><span class="sxs-lookup"><span data-stu-id="c29e5-214">For the WCS color profiles shipped with windows, the Color CPL displays descriptive information from the resources, rather than from the wcs:Text elements in the profiles.</span></span> <span data-ttu-id="c29e5-215">這可讓 Windows 以所有支援的語言顯示這些設定檔的當地語系化資訊，而不需要 themlselves 設定檔以包含所有語言的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="c29e5-215">This allows Windows to display localized information for these profiles in all supported languages, without requiring the profiles themlselves to contain descriptive information in all languages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c29e5-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="c29e5-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c29e5-217">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="c29e5-217">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="c29e5-218">Windows 色彩系統架構和演算法</span><span class="sxs-lookup"><span data-stu-id="c29e5-218">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 