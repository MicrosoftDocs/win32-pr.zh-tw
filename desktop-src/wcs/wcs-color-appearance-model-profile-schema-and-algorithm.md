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
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>WCS 色彩外觀模型設定檔架構和演算法

[概觀](#overview)

[色彩外觀模型設定檔 (CAMP) 架構](#color-appearance-model-profile-architecture)

[CAMP 架構](#the-camp-schema)

[CAMP 架構元素](#the-camp-schema-elements)

[CAMP 演算法](#the-camp-algorithm)

### <a name="overview"></a>概觀

此架構可用來指定色彩外觀模型設定檔 (CAMP) 的內容。 下列各節將說明相關聯的基準演算法。

CAMP 是由 XML 標記所組成，可將參數值提供給 CIECAM02 基準色彩外觀模型變數。 有關參數範圍的詳細資料會在基準色彩外觀模型規格和 CIECAM02 建議中提供。

### <a name="color-appearance-model-profile-architecture"></a>色彩外觀模型設定檔架構

![顯示 X M L 標記所組成之 CAMP 設定檔架構的圖表。](images/camp-image002new.png)

### <a name="the-camp-schema"></a>CAMP 架構


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



## <a name="the-camp-schema-elements"></a>CAMP 架構元素

## <a name="colorappearancemodel"></a>ColorAppearanceModel

這個元素的順序如下：

1.  ProfileName 字串，
2.  選擇性描述字串，
3.  選用的作者字串，
4.  ViewingConditions 元素。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。 字串長度限制為10000個字元。

## <a name="namespace"></a>命名空間

xmlns： cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>版本

&gt; &lt; 第一版的 Windows Vista 版本0.1 或 = "1.0"。

**驗證條件：** 任何版本值 &lt; = 2.0 也都有效，可支援格式的非重大變更。

## <a name="documentation"></a>文件

色彩外觀模型設定檔架構。

著作權 (C) Microsoft。 著作權所有，並保留一切權利。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

## <a name="surroundtype"></a>SurroundType

此元素為 "Average"、"Dim" 或 "深色" CIECAM02 參數的列舉，或 CIECAM02 建議 c 中的實際量化參數，即環繞的影響。

**驗證條件：** C 參數的範圍可以從0.525 到0.69。

## <a name="viewingconditions"></a>ViewingConditions

此元素包含下列子項目：



| 元素                    | 類型           |
|----------------------------|----------------|
| WhitePoint                 | WhitePointType |
| 背景                 | CIEXYZ         |
| 環繞                   | SurroundType   |
| LuminanceOfAdaptingField   | FLOAT          |
| DegreeOfAdaptation         | FLOAT          |
| NormalizeToMediaWhitePoint | Boolean        |



 

**驗證條件：** CIEXYZ 子項目是由 NonNegativeXYZType 進行驗證。 LuminanceOfAdaptingField 的最大值為10，000cd/m ^ 2。 DegreeOfAdaptation 的範圍可以從0.0 到1.0。 NormalizeToMediaWhitePoint 值可以是 "true" 或 "false"。 如果 NormalizeToMediaWhitePoint 子項目不存在，就會有效地預設為 "true"。 請參閱下列 CAMP 演算法一節。

## <a name="whitepointtype"></a>WhitePointType

這個元素是 CIE 光源來源值的列舉 ( "D50"、"D65"、"A" 或 "F2" ) 或 CIEXYZ 子項目。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

## <a name="ciexyztype"></a>CIEXYZType

CIEXYZType 元素是由三個 NonNegativeFloatType 單精確度 IEEE 浮點元素所組成，名為 "X"、"Y" 和 "Z"。 這些測量可以是絕對 (非相對) CIEXYZ 1931 反射值或絕對 (不是相對) CIEXYZ 1931 direct (transmissive) 值（每個計量平方單位）。

**驗證條件：** 這表示只有真實世界的值有效，且負值的 CIEXYZ 測量值無效。 由於這些都是絕對值，因此值的範圍可能會超過 1.0 f。 任何 X、Y 或 Z 值的合理限制都將任意設定為 10000.0 f。

 

### <a name="the-camp-algorithm"></a>CAMP 演算法

色彩外觀模型 (凸輪) 是以 CIE CIECAM02 色彩外觀模型方程式為基礎。

這個類別會實色外觀模型化。 請注意，WCS 凸輪 *無法* 取代，例如使用外掛程式。 它是一個設計目標，只能有一個色彩外觀模型。 凸輪是以 CIECAM02 建議為基礎。

CIECAM02 可以用兩種方式來使用。 在色階到外觀的方向中，它會提供從 CIE XYZ 空間到色彩外觀空間的對應。 在外觀為色度的方向中，它會將色彩外觀空間對應回 XYZ 空間。 色彩外觀會將亮度、J、色度、C 和色調（h）相互關聯。 這三個值形成圓柱座標系統。 通常，在矩形座標系統中工作變得更方便，因此計算 a = C cos h 和 b = C sin h，以提供 CIECAM02 Jab。

您可以使用大於100的凸輪亮度值。 採用 CIECAM02 的 CIE 委員會並未解決亮度軸的輸入值（亮度大於所採用的白色點）的行為;也就是，輸入 Y 值大於所採用的白色點 Y 值。 測試已顯示 CIECAM02 中的亮度方程式對此類值的行為相當合理。 亮度會以指數方式增加，並遵循相同的指數 (大約 1/3) 。

使用者有時會想要變更 (D) 的調整程度的計算方式。 WCS 設計可讓使用者藉由變更查看條件參數中的 degreeOfadaptation 值來控制這項計算。

為了提供與使用者的 ICC 影響的預期更一致的相符，預設 CAMP 中的 degreeOfAdaptation 是1.0。 這會在 MinCD 絕對以外的所有情況下產生更好的結果，其中一個可能會想要讓 WCS 透過 degreeOfAdaptation =-1) 來計算 degreeOfAdaptation (。

它不會使用「平均」、「維度」和「深色」的範圍值，而是會提供從值 c 計算的連續範圍值。 C 的值必須是介於0.525 到0.69 之間的浮點數。

從 *c*、 *Nc* 和 *F* 可以計算，並在已提供給「平均」、「維度」和「深色」的值之間使用分段的線性插補。 這是 CIE 159:2004 的 [圖 1] 所示的模型，即 CIECAM02 規格。



| degreeOfAdaption                     | 行為                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![顯示預設 C I E C A M 02 行為的公式。](images/camp-image006.png)這是預設的 CIECAM02 行為。<br/> |
| 0.0 &lt; = degreeOfAdaption &lt; = 1。0 | *D* = degreeOfAdaptation (使用者提供的值)                       |



 

執行中也已加入特定的錯誤檢查量。 以下是在 CIECAM02 的 CIE 159:2004 定義中使用的方程式編號。

**ColorimetricToAppearanceColors**

系統會檢查輸入值的合理：如果是 X 或 Z &lt; 0.0，或如果 &lt; 是 Y-1.0，則 HRESULT 為 E \_ INVALIDARG。 如果-1.0 &lt; = Y &lt; 0.0，則 J、C 和 h 全都設定為0.0。

有些內部條件可能會產生錯誤結果。 系統不會產生這樣的結果，而是會裁剪內部結果以產生範圍內的值。 這會發生在具有深色和非常彩色的色彩規格中：在方程式7.23 中，如果 &lt; 0，a = 0。 在方程式7.26 中，如果 t &lt; 0，t = 0。

**AppearanceToColorimetricColors**

系統會檢查輸入值是否有合理。 如果 &lt; 是 c 0、C &gt; 300 或 J &gt; 500，則 HRESULT 為 E \_ INVALIDARG。

*R '<sub>a;</sub>*、 *G '<sub>a;</sub>* 和 *B '<sub>a;</sub>*， (方 8.19-8.21) 會裁剪至範圍399.9。

針對所有色彩外觀模型設定檔 (Camp) ，WCS 引擎會檢查採用的白色點。 如果 Y 不是100.0，則會調整採用的白色點，讓 Y 等於100.0。 相同的縮放比例將會套用至背景值。 調整因數為 100.0/adoptedWhitePoint。 Y。 相同的縮放比例會套用至每個 X、Y 和 Z。如果 NormalizeToMediaWhitePoint 欄位設定為 "True"，或 CAMP 中沒有該欄位，則引擎也會將所有裝置色彩輸入調整為 DeviceToColorimetric，讓裝置媒體的 Y 值等於100.0。 來自 ColorimetricToDevice 的裝置色彩將會以該縮放比例的乘法反向縮放。 如果 [NormalizeToMediaWhitePoint] 旗標設定為 [False]，則不會調整色度資料。

針對某些工作，調整來自 DeviceToColorimetric 的色度值是合理的。 凸輪中的雙曲亮度方程式實際上是針對100.0 的白色點亮度所設計。 絕對亮度 (或 illuminance) 差異的唯一位置是在 [調整] 欄位的亮度中。 因此，必須使用100.0 的白色點來初始化凸輪。 但是，如果裝置型號的中等白色點正當做採用的白色點使用，則來自裝置的所有色彩都必須據以調整，否則裝置的白色將不會有 J 值100.0。 因此，Y 值必須在度量中縮放。 您可以調整測量值，再將裝置模型初始化。 然後，結果會在適當的範圍內。 但這會讓測試裝置模型變得更困難，因為即將推出的值需要調整。 針對裝置媒體的白色點會被認為是真正白色的工作，則需要依裝置媒體的白色點進行正規化。

凸輪會直接從 CAMP 初始化。 這可讓開發人員根據所要執行的工作，在初始化凸輪時有彈性。 在某些工作中，觀察者會忽略媒體白名單中的任何色度，因為它們 cognitively 「知道」來源和目的地媒體都是「白色」。 在這種情況下，開發人員會想要使用各自的媒體重點來初始化向前和反向攝影機。 在某些情況下，觀察者可能會比較媒體背景的色彩。 在這些情況下，建議您對這兩個裝置使用一個 CAM，而不想要根據裝置的中等白色點來調整每個裝置的色度值。 然後，媒體的不同 tristimulus 值會導致 CIECAM02 中的不同外觀值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本色彩管理概念](basic-color-management-concepts.md)
</dt> <dt>

[Windows 色彩系統架構和演算法](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





