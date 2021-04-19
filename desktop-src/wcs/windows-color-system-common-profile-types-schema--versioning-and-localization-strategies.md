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
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Windows Color System 一般配置檔案類型架構、版本控制和當地語系化策略

-   [WCS 一般配置檔案類型架構 V1](#wcs-common-profile-types-schema-v1)
-   [WCS 一般配置檔案類型架構 V2 新增專案](#wcs-common-profile-types-schema-v2-additions)
-   [WCS 設定檔架構版本控制](#wcs-profile-schema-versioning)
-   [WCS 設定檔當地語系化](#wcs-profile-localization)
    -   [表示可當地語系化的元素](#expressing-localizable-elements)
    -   [架構支援](#schema-support)
    -   [選取語言](#selecting-the-language)
    -   [內建設定檔](#built-in-profiles)
-   [相關主題](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>WCS 一般配置檔案類型架構 V1

以下提供適用于 WCS 一般配置檔案類型的 v1.0 架構定義。


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



僅支援 UTF-8 或 UTF-16 編碼。 強烈建議您不要採用所有其他 XML 編碼，以保持最佳互通性。

## <a name="wcs-common-profile-types-schema-v2-additions"></a>WCS 一般配置檔案類型架構 V2 新增專案

在 Windows 7 中，已更新 WCS 一般配置檔案類型架構，以包含支援 [WCS 校正架構](wcs-calibration-schema.md)的類型。


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



## <a name="wcs-profile-schema-versioning"></a>WCS 設定檔架構版本控制

在此附錄中，「設定檔取用者」一詞是指 WCS 軟體或使用 WCS 設定檔的協力廠商軟體元件。

較新版本的設定檔取用者將能夠取用根據舊版架構所撰寫的 WCS 設定檔。 若要充分利用最新的架構版本中定義的功能，通常會需要最新版本的設定檔取用者。 不過，較舊的設定檔取用者可以取用根據較新版本的架構所撰寫的設定檔。 設定檔取用者可以忽略它不了解的 XML 元素和屬性。 結果會是正確的，但相較于最新版本的設定檔取用者所達成的結果，效能或精確度可能會降低。

以下是設定檔取用者的版本控制方針：

-   指定的設定檔取用者版本，必須從版本命名空間辨識所有元素和屬性，或全部都不是。
-   如果設定檔取用者遇到不了解的命名空間中的專案或屬性，則必須將它視為錯誤狀況，除非設定檔包含有關回退處理的明確指引。
-   [開放式封裝規格](https://www.microsoft.com/whdc/xps/xpspkg.mspx)會定義其他命名空間 URI （標記相容性命名空間），以定義提供此回溯處理指引的元素和屬性。
-   所有設定檔取用者的所有版本都必須辨識並遵守標記相容性命名空間中的所有元素和屬性。
-   以新版本的設定檔架構為基礎的分析取用者必須支援所有先前定義的版本命名空間。

在1.0 版中，WCS 會辨識下列命名空間中的元素和屬性：

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

以下示範標記相容性的範例。


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



## <a name="wcs-profile-localization"></a>WCS 設定檔當地語系化

**需求**

WCS 設定檔包含某些元素，例如 ProfileName 和描述，其中包含人們看得懂的文字。 這是可當地語系化的文字。

以下是設定檔建立者的版本控制指導方針：

-   針對由協力廠商所建立的設定檔（例如印表機製造商），設定檔作者應納入多種語言的描述性文字。
-   下列元素應可當地語系化： 

    | 元素     | CDMP | GMMP | 營地 |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Description | x    | x    | x    |
    | 作者      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>表示可當地語系化的元素

每個可當地語系化的元素都包含一或多個 wcs： Text 子項目，而不是直接包含文字，而每個專案都必須指定 xml： lang 屬性。 如 [xml 規格](http://www.w3.org/TR/REC-xml/) 區段 2.12 ( 「語言識別」 ) 所述，xml： lang 屬性的值必須是 IETF RFC 3066 語言識別項，例如 "en-us"、"en" 或 "fr-fr"。 在 WCS 架構中，xml： lang 屬性的值不能是空字串 ""，即使 XML 在一般情況下允許這種情況也一樣。 例如：


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



沒有兩個 wcs： Text 元素可以有相同的 xml： lang 屬性。 每個 WCS 設定檔架構都必須針對每個可當地語系化的元素分別強制執行這個條件約束。 僅支援 UTF-8 與 UTF-16 編碼。

### <a name="schema-support"></a>架構支援

此設計利用 WCS 一般配置檔案類型架構中定義的 XSD 類型 wcs： LocalizedText 和 wcs： MultiLocalizedType：


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



每個 WCS 設定檔架構都會將每個可當地語系化的專案宣告為類型 MultiLocalizedType，例如：


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



CDMP 架構會強制執行 cdm： Description 元素的每個 wcs： Text 子系必須有唯一的 xml： lang 屬性的條件約束。 它會對其他可當地語系化的元素強制執行相同的條件約束。 CAMP 和 GMMP 架構也相同。

### <a name="selecting-the-language"></a>選取語言

當您決定要顯示之可當地語系化專案的語言版本時，應用程式程式碼應該選取「最接近的版本」至「目前的語言」。 「最接近的版本」和「目前語言」真正的意義是與平臺相依;請參閱下文。 如果設定檔不包含符合目前語言的語言版本，則應用程式應該選取設定檔中的第一個版本， (可當地語系化元素) 的第一個 wcs： Text 子項目。

在 Windows Vista 上，語言選擇的完成方式如下：每個執行緒都有相關聯的「慣用 UI 語言」清單，可透過呼叫 [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages)來取得。 此清單會依使用者喜好設定順序傳回。 比方說，在設定為美式英文的系統上， **GetThreadPreferredUILanguages** 傳回的清單是 {"en-us"，"en"}。 這表示： 1) 美式英文（如果有的話）。 2) 否則，請使用英文的任何區域性變化，例如 "en-us" 或單純的 "en"。

針對清單中的每個語言，在清單順序中，UI 程式碼會尋找其 xml： lang 屬性完全相符的 wcs： Text 元素。 使用第一個相符的版本。 如果沒有版本符合，則會使用第一個 wcs： Text 元素。

### <a name="built-in-profiles"></a>內建設定檔

Windows Vista 隨附的標準 WCS 設定檔（例如 sRGB. cdmp）具有與其他設定檔相同的可當地語系化屬性。

標準 Windows 方案是將當地語系化的字串放在 MUI DLL 中，並將其參考如下：


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



在 Windows 系統上，描述文字會從適當當地語系化版本的 MUI 資源的資源識別碼101中解壓縮，以進行 mscms.dll。 非 Windows 系統會使用 wcs： Text 子項目，如上所述。

我們在每個 WCS 設定檔架構的根項目上引進一個選擇性的全域唯一識別碼屬性。 標準設定檔 wcsRGB. cdmp 看起來可能像這樣：


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



在 windows 隨附的 WCS 色彩設定檔中，色彩 CPL 會顯示資源中的描述性資訊，而不是來自設定檔中的 wcs： Text 元素。 這可讓 Windows 以所有支援的語言顯示這些設定檔的當地語系化資訊，而不需要 themlselves 設定檔以包含所有語言的描述性資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本色彩管理概念](basic-color-management-concepts.md)
</dt> <dt>

[Windows 色彩系統架構和演算法](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 