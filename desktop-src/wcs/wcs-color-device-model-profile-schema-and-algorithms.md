---
title: WCS 色彩裝置模型設定檔架構和演算法
description: 本主題提供有關 WCS 色彩裝置模型設定檔架構及其相關演算法的資訊。本主題包含下列各節 OverviewColor 裝置模型設定檔 ArchitectureThe CDMP SchemaWCS CDMP v 2.0 校正 AdditionThe CDMP 架構 ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDeviceelementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTy peMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe CDMP 基準 AlgorithmsCRT 裝置型號 BaselineLCD 裝置型號 BaselineRGB 印表機裝置型號 BaselineRGB 虛擬裝置型號 BaselineCMYK 印表機裝置型號 BaselineRGB 投影機裝置型號 BaselineICC 裝置型號 BaselineRelated 主題
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- 'Windows Color System (WCS) ，色彩裝置模型設定檔 (CDMP) '
- 'WCS (Windows 色彩系統) ，色彩裝置模型設定檔 (CDMP) '
- '影像色彩管理、色彩裝置模型設定檔 (CDMP) '
- '色彩管理、色彩裝置模型設定檔 (CDMP) '
- '色彩、色彩裝置模型設定檔 (CDMP) '
- Windows Color System (WCS) ，設定檔
- WCS (Windows 色彩系統) ，設定檔
- 影像色彩管理，設定檔
- 色彩管理，設定檔
- 色彩，設定檔
- '架構、色彩裝置模型設定檔 (CDMP) '
- '演算法、色彩裝置模型設定檔 (CDMP) '
- '色彩裝置模型設定檔 (CDMP) '
- 'CDMP (色彩裝置模型設定檔) '
- WCS 色彩裝置模型設定檔
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b671bf97625b00c99060e65be4d39c44e5b35f
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104562165"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>WCS 色彩裝置模型設定檔架構和演算法

本主題提供有關 WCS 色彩裝置模型設定檔架構及其相關演算法的資訊。

本主題包含下列幾節：

-   [概觀](#overview)
-   [色彩裝置模型設定檔架構](#color-device-model-profile-architecture)
-   [CDMP 架構](#the-cdmp-schema)
-   [加入 WCS CDMP 2.0 版校正](#wcs-cdmp-v20-calibration-addition)
-   [CDMP 架構元素](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [NamespaceVersion](#namespaceversion)
    -   [版本](#namespaceversion)
    -   [文件集](#documentation)
    -   [CRTDevice 元素](#crtdevice-element)
    -   [LCDDevice 元素](#lcddevice-element)
    -   [ProjectorDevice 元素](#projectordevice-element)
    -   [ScannerDevice 元素](#scannerdevice-element)
    -   [CameraDevice 元素](#cameradevice-element)
    -   [RGBPrinterDevice 元素](#rgbprinterdevice-element)
    -   [CMYKPrinterDevice 元素](#cmykprinterdevice-element)
    -   [RGBVirtualDevice 元素](#rgbvirtualdevice-element)
    -   [PlugInDeviceType](#plugindevicetype)
    -   [RGBVirtualMeasurementType](#rgbvirtualmeasurementtype)
    -   [GammaType](#gammatype)
    -   [GammaOffsetGainType](#gammaoffsetgaintype)
    -   [GammaOffsetGainLinearGainType](#gammaoffsetgainlineargaintype)
    -   [ToneResponseCurvesType](#toneresponsecurvestype)
    -   [GamutBoundarySamplesType](#gamutboundarysamplestype)
    -   [FloatPairList](#floatpairlist)
    -   [CMYKPrinterMeasurementType](#cmykprintermeasurementtype)
    -   [RGBPrinterMeasurementType](#rgbprintermeasurementtype)
    -   [RGBCaptureMeasurementType](#rgbcapturemeasurementtype)
    -   [OneBasedIndex](#onebasedindex)
    -   [RGBProjectorMeasurementType](#rgbprojectormeasurementtype)
    -   [DisplayMeasurementType](#displaymeasurementtype)
    -   [MeasurementConditionsType](#measurementconditionstype)
    -   [GeometryType](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeCMYKSampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeCMYKType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [CDMP 基準演算法](#the-cdmp-baseline-algorithms)
    -   [CRT 裝置模型基準](#crt-device-model-baseline)
    -   [LCD 裝置型號基準](#lcd-device-model-baseline)
    -   [RGB 印表機裝置型號基準](#rgb-printer-device-model-baseline)
    -   [RGB 虛擬裝置模型基準](#rgb-virtual-device-model-baseline)
    -   [CMYK 印表機裝置型號基準](#cmyk-printer-device-model-baseline)
    -   [RGB 投影機裝置型號基準](#rgb-projector-device-model-baseline)
    -   [ICC 裝置型號基準](#icc-device-model-baseline)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

此架構可用來指定 (CDMP) 之色彩裝置模型設定檔的內容。 相關聯的基準演算法如下所述。

基本裝置模型設定檔 (DMP) 架構包含取樣測量資料。

DMP XML 架構的取樣元件提供基本色彩測量目標的支援，著重在針對基準裝置模型優化的一般標準目標和目標。

此外，裝置設定檔會提供目標裝置模型的特定資訊，並提供當目標模型無法使用時，基準回溯裝置模型可以使用的原則。 設定檔實例可包含使用標準 XML 擴充機制的私用延伸模組。

## <a name="color-device-model-profile-architecture"></a>色彩裝置模型設定檔架構

![此圖顯示組成裝置模型設定檔的資訊。](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>CDMP 架構


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
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
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a>加入 WCS CDMP 2.0 版校正

CDMP 架構的 **ColorDeviceModel** 元素已在 Windows 7 中更新，以包含新的校正元素。 下圖顯示 CDMP 架構的變更。


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a>CDMP 架構元素

> [!Note]  
> 主要複本是紅色、綠色、藍色、黑色和白色的主要範例。 主要的斜坡是從最小亮度到完整主要值的色調滑軌。 色調曲線中的專案數上限為4096。

 

> [!Note]  
> DMPs 必須有測量資料。

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

這個元素的型別為 ColorDeviceModel。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="colordevicemodel"></a>ColorDeviceModel

此元素是下列子項目的序列

1.  ProfileName 字串，
2.  選擇性描述字串，
3.  選用的作者字串，
4.  選擇性的 MeasurementConditions MeasurementConditionsType、
5.  Self-Luminous 布林值，
6.  MaxColorant float、
7.  MinColorant float、
8.  元素的選擇
    1.  CRTDevice,
    2.  LCDDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. 選用擴充 ExtensionType

**驗證條件：** 每個子項目都是由它自己的類型來驗證。 字串子項目的最大值為10000個字元。 MaxColorant 子項目必須大於或等於零 (0) 且大於 MinColorant 子項目。 MinColorant 可以是負數。

### <a name="namespaceversion"></a>NamespaceVersion

xmlns： cdm = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>版本

Version = "1.0" 與 Windows Vista 搭配使用。

**驗證條件：** 任何版本值 &gt; 0.1 或 &lt; = 2.0 都有效，可支援格式的非重大變更。

### <a name="documentation"></a>文件

裝置模型設定檔架構。

著作權 (C) Microsoft。 著作權所有，並保留一切權利。

### <a name="crtdevice-element"></a>CRTDevice 元素

這個元素是 MeasurementData DisplayMeasurementType 的子項目序列。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="lcddevice-element"></a>LCDDevice 元素

這個元素是 MeasurementData DisplayMeasurementType 的子項目序列。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="projectordevice-element"></a>ProjectorDevice 元素

這個元素是 MeasurementData RGBProjectorMeasurementType 的子項目序列。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="scannerdevice-element"></a>ScannerDevice 元素

此元素是 MeasurementData RGBCaptureMeasurementType 的子項目序列

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="cameradevice-element"></a>CameraDevice 元素

此元素是 MeasurementData RGBCaptureMeasurementType 的子項目序列

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="rgbprinterdevice-element"></a>RGBPrinterDevice 元素

這個元素是 MeasurementData RGBPrinterMeasurementType 的子項目序列。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="cmykprinterdevice-element"></a>CMYKPrinterDevice 元素

這個元素是 MeasurementData CMYKPrinterMeasurementType 的子項目序列。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="rgbvirtualdevice-element"></a>RGBVirtualDevice 元素

這個元素是 RGBVirtualMeasurementDataType 子項目的序列。

**驗證條件：** 每個子項目都是由它自己的類型來驗證。

### <a name="plugindevicetype"></a>PlugInDeviceType

此元素是 GUID GUIDType 和任何子項目的序列。

**驗證條件：** GUID 是用來符合 DM 外掛程式 Dll GUID。 最多可以有100000個自訂子項目。

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

此元素是由下列專案組成的序列

1.  RGBPrimariesGroup 群組
2.  選擇
3.  -   色差補正
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   ToneResponseCurves 元素

4.  選擇性的 GamutBoundarySamples GamutBoundarySamplesType
5.  時間戳記 dateTime

**驗證條件：** 這些類型的每個子項目都有自己的驗證條件。

### <a name="gammatype"></a>GammaType

這個元素是由屬性所組成的複雜型別。

-   Gamma NonNegativeFloatType

**驗證條件：** 由產業意見反應決定。

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

這個元素是由屬性所組成的複雜型別。

-   Gamma NonNegativeFloatType
-   位移 NonNegativeFloatType
-   增益 NonNegativeFloatType

**驗證條件：** 由產業意見反應決定。

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

這個元素是由屬性所組成的複雜型別。

-   Gamma NonNegativeFloatType
-   位移 NonNegativeFloatType
-   增益 NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**驗證條件：** 由產業意見反應決定。

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

這個元素是一系列的

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

元素也有 unsignedint 類型的屬性 TRCLength。

**驗證條件：** 由產業意見反應決定。

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

這個元素是一系列的 RGB RGBTypes。

**驗證條件：** 目前未系結的最大值，會根據產業意見反應進行限制。

### <a name="floatpairlist"></a>FloatPairList

此元素是簡單類型的浮點數組清單。

**驗證條件：** 由產業意見反應決定。

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

此元素為

1. 由一連串範例 NonNegativeCMYKSampleType 組成的 ColorCube 元素順序

2. TimeStamp dateTime 屬性。

**驗證條件：** 由產業意見反應決定。

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

此元素為

1. 由一連串範例 NonNegativeRGBSampleType 組成的 ColorCube 元素順序

2. TimeStamp dateTime 屬性。

**驗證條件：** 由產業意見反應決定。

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

這個元素是一系列的

1.  的 PrimaryIndex complexType
2.  1.  白色 OneBasedIndex
    2.  選用的黑色 OneBasedIndex
    3.  選擇性的 Red OneBasedIndex
    4.  選擇性綠色 OneBasedIndex
    5.  選用藍色 OneBasedIndex
    6.  選用的青色 OneBasedIndex
    7.  選擇性的洋紅 OneBasedIndex
    8.  選擇性黃色 OneBasedIndex

3.  OneBasedIndex 行的 NeutralIndices
4.  範例 NonNegativeRGBSampleType 的 ColorSamples 序列

元素也有 TimeStamp dateTime 屬性。

**驗證條件：** 由產業意見反應決定。

### <a name="onebasedindex"></a>OneBasedIndex

此元素是簡單類型的限制基底不帶正負號的整數，其 minInclusive 值 = "1"。

**驗證條件：** 由產業意見反應決定。

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

這個元素是一系列的

1.  RGBPrimariesGroup 群組
2.  元素 ColorSamples 由範例 NonNegativeRGBSampleType 的順序組成

元素也有 TimeStamp dateTime 屬性。

**驗證條件：** 由產業意見反應決定。

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

這個元素是一系列的

1.  群組 RGBPrimariesGroup
2.  範例 NonNegativeRGBType 序列的 GrayRamp
3.  範例 NonNegativeRGBType 序列的 RedRamp
4.  範例 NonNegativeRGBType 序列的 GreenRamp
5.  範例 NonNegativeRGBType 序列的 BlueRamp

DisplayMeasurementType 元素也有 TimeStamp dateTime 屬性。

**驗證條件：** 由產業意見反應決定。

### <a name="measurementconditionstype"></a>MeasurementConditionsType

MeasurementConditionsType 是包含下列專案的子項目序列：

1.  ColorSpace 限制的字串列舉值 "CIEXYZ"
2.  選擇性的 WhitePoint NonNegativeXYZType 或 WhitePointName 字串列舉值 D50、D65、A 或 F2
3.  幾何 GeometryType
4.  ApertureSize 整數（以毫米為單位）

預設值為：

1.  RGB 和 CMYK 印表機：
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
2.  掃描器：
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
3.  顯示和 RGB 虛擬裝置：
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
4.  相機：
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  直接 GeometryType
    4.  10mm ApertureSize

**驗證條件：** 每個子專案的驗證都是由這些子項目的驗證條件所決定。 如果遺漏任何子項目，則會使用裝置模型類型特定預設值。

### <a name="geometrytype"></a>GeometryType

String

列舉值：

-   "0/45"
-   "0/擴散"
-   「擴散/0」
-   直接

**驗證條件：** 除了所列的 enumberation 值以外的任何值都無效。 這種資訊不會變更基準處理行為。

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

這個元素是一系列的

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**驗證條件：** 由產業意見反應決定。

### <a name="nonnegativecmyksampletype"></a>NonNegativeCMYKSampleType

這個元素是一系列的

1.  CMYK NonNegativeCMYKType
2.  CIEXYZ NonNegativeXYZType

元素也有選擇性的屬性標記字串

**驗證條件：** 由產業意見反應決定。

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

這個元素是一系列的

1.  RGB NonNegativeRGBType
2.  CIEXYZ NonNegativeXYZType

元素也有選擇性的屬性標記字串

**驗證條件：** 由產業意見反應決定。

### <a name="nonnegativecmyktype"></a>NonNegativeCMYKType

由屬性組成的這個元素

1.  C float
2.  M 浮點數
3.  Y 浮點數
4.  K 浮點數

**驗證條件：** 由產業意見反應決定。

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

由屬性組成的這個元素

1.  R float
2.  G float
3.  B float

**驗證條件：** 由產業意見反應決定。

### <a name="extensiontype"></a>ExtensionType

ExtensionType 元素是任何子項目類型的序列，用於非 Microsoft 應用程式的專屬資訊。

**驗證條件：** 這個元素是選擇性的。 最多可以有1000個擴充子項目。

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

NonNegativeXYZType 元素是由 NonNegativeFloatType 三個單精確度 IEEE 浮點元素所組成，名為 "X，" "Y" 和 "Z"。 這些值僅限於 DMP 設定檔測量值。 這些測量可以是絕對 (非相對) CIEXYZ 1931 反射值或絕對 (不是相對) CIEXYZ 1931 direct (transmissive) 值（每個計量平方單位）。

**驗證條件：** 只有真實世界的值有效，且負值的 CIEXYZ 測量值無效。 因為這些是絕對值，所以值可以大於 1.0 f。 任何 "X"、"Y" 或 "Z" 的合理限制。 值會任意設定為 10000.0 f。

### <a name="xyztype"></a>XYZType

XYZType 元素是由三個單精確度 IEEE 浮點值所組成： "X"、"Y" 和 "Z"。

## <a name="the-cdmp-baseline-algorithms"></a>CDMP 基準演算法

### <a name="crt-device-model-baseline"></a>CRT 裝置模型基準

若要瞭解此模型，您必須考慮特性程式和裝置模型化。 在特性程式中，系統會先透過填妥 CRT 顯示裝置的顯示緩衝區，對所取得的色彩執行 XYZ 測量。 下列範例值會為基準 CRT 裝置模型產生良好的資料：

Red： R = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、G = B = 0

綠色： G = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = B = 0

Blue： B = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = G = 0

Neutrals： R = G = B = 0、8、16、32、64、128、192、255

也可以使用15和非線性增量以外的增量。 每個紅色、綠色、藍色和中性的斜坡都必須包含至少三個範例，但建議提供更多的範例。 您必須提供純紅色、綠色、藍色、黑色和白色的範例。 這些範例不一定要有一致的間距。

建立 tristimulus 矩陣的套裝程式含兩個步驟。 首先，估計黑色點的 XYZ 值或光暈。 此步驟主要是以 \[ 稍微修改過的 Berns 3 工作 \] 為非線性優化的目標函式為基礎。 其次，根據步驟1中的結果，以及所有每個通道測量的平均計算來計算 tristimulus 矩陣，而不只是數位計數的最大值。

上述每個步驟都包含詳細的程式。 起點是在我們的) 範例中，每個 R、G 和 B 通道的 (17 個步驟。 在 chromaticity 的 *xy* 平面上繪製 XYZ 測量時，[圖 1] 中會顯示一般情況。 第一步是要解決非線性優化問題，以找出「最適合」的黑色點，將 chromaticity 中的漂移降至一次流經 R、G 和 B 通道。 \[我們會根據 Berns 3 \] 來搜尋 ( *X <sub>k</sub>*、*Y <sub>k</sub>*、*Z <sub>k</sub>* ) ，以將下列目標函式降至最低：

![顯示 Sr、Sg 和 Sb 是 R、G 和 B 通道上的資料點組合的目標函數。](images/cdmp-formula1.png)

其中 *s <sub>r</sub>*、*s <sub>G</sub>* 和 *s <sub>B</sub>* 是對應至 R、G 和 B 通道上點的資料點集合。 針對 *任何集合，* 請定義：

![顯示定義任何集合的公式。](images/cdmp-formula2.png)

在上述的中， \| *s* \| 是的基數，也就是集合中的點數目。  ![顯示點 chromaticity 的公式。](images/cdmp-formula3.png) 點的 chromaticity 座標會顯示某 ![ 點的 formaula。](images/cdmp-formula4.png) 因此， ![ 會顯示一份平均或大容量中間的公式。 ](images/cdmp-formula5.png) 是 chromaticity 平面 *中，* 集合內所有點的平均或大容量中心。 因此，會 ![ 顯示第二分鐘點總和的公式。](images/cdmp-formula6.png) 這是有關大範圍點的第二分鐘的總和，這是分佈點相關方式的量值。 最後，會 ![ 顯示三個點點分佈的總計量值公式。](images/cdmp-formula7.png) 是如何分散三個點點的整體量值，以瞭解其各自的大型中心。

在的計算中 ![ ，會顯示 f 的公式 (X、Y、Z;Xk、Yk、Zk) 。](images/cdmp-formula8.png) 如果 ![ 顯示 X 的公式 ](images/cdmp-formula9.png) ，則會略過計算，並據以調整 *S* 的基數。

儘管目標函式的複雜度很明顯，但它是 *X <sub>k</sub>* 中許多 differentiable 函式的平方總和，*Y <sub>k</sub>Z <sub>k</sub>* (17 點 2 *xy* -元件 3 channel = 102，在範例) 中，因此，會適合至標準的非線性最小平方技術，例如 Levenberg-Marquardt 演算法，也就是 WCS 中使用的演算法。 請注意，上述的目標函數與 Berns 3 中建議的函式不同，後者的函式會測量從大到大的距離的變異 \[ \] 數，因此當點與大量的點等距時，變異數就會是零，即使它們可能會分散到很多的內容也是一樣。 在此範例中，會使用第二分鐘直接 contolled 點散佈。

如同適用于非線性最小平方問題的任何反復演算法，Levenberg-Marquardt 需要初步猜測。 有兩個明顯的候選項目。 其中一個是 (0、0、0) ;另一個則是測量的黑色點。 針對 CTE，測量的黑色點會先做為初始猜測。 如果超過100個反覆運算的最大值，但未達到每個 (點的平均距離0.001 的平均距離，而此臨界值對應至目標函式) 的臨界值（ (0.001) 17 3 = 0.000051），則會執行另一輪次猜測 (0、0、0) 的反復專案。 所產生的黑色點估計值是 XYZ，相較于上一回合反復專案的最佳估計值 (以測量的黑色點做為初始猜測) 。 使用可為目標函式提供最小值的估計值。 選擇的100反復專案和0.001 的誤差距離為每個選取的廣為人知且實證。 在未來的版本中，將錯誤距離參數化可能是合理的。

步驟1的結果是估計的黑色點 ( *X <sub>k</sub>*、*Y <sub>K</sub>*、*Z <sub>K</sub>* ) 。 步驟二包含決定 tristimulus 矩陣，方法是將第一個步驟中取得之三個群集的點 chromaticity 平均。 針對 Crt，這是為了將測量錯誤的影響降到最低。 用來平均 chromaticity 的點必須與步驟1中的優化所使用的點相同。 換句話說，如果數位計數 15 (第一個點，則在優化步驟中會捨棄每個滑軌中) 的範例，而必須在平均值中完成相同的操作。 如果 ![ 顯示紅色和綠色通道中座標的平均 chromaticity 公式。](images/cdmp-formula10.png) ，並 ![ 顯示藍色通道中座標的平均 chromaticity 公式。](images/cdmp-formula11.png) 是紅色、綠色和藍色通道的平均 chromaticity 座標，而下列程式會決定 tristimulus 矩陣。 首先，請解決3？3線性系統：

![顯示解決3？3線性系統的程式第一個部分。](images/cdmp-formula12.png)

![顯示3？3線性系統的第二個部分。](images/cdmp-formula13.gif)![顯示3？3線性系統第二個部分結尾的 t 注標 b 值。](images/cdmp-formula14.gif)

*X <sub>W</sub>*、*Y <sub>W</sub>*、*Z <sub>W</sub>*

![顯示解決3？3線性系統的程式最後部分。](images/cdmp-formula15.png)

判斷出 tristimulus 矩陣之後，色調曲線的判斷會遵循標準的方法。 針對 CRT 顯示，會假設個別的通道會遵循 "GOG" 模型：

![顯示 ' G O G G ' 模型的公式。](images/cdmp-formula16.png)

其中 *k <sub>g</sub>* 是「增益」，1-*k <sub>g</sub>* 是「位移」，而？ 是 "gamma"。 Tristimulus 矩陣的反向矩陣會套用至 neutrals 的 XYZ 資料以取得線性 RGB 資料，然後使用 GOG 模型上的非線性回歸，與數位 RGB 值相互關聯。 對 R、G 和 B 通道而言，這些特性不一定相同，而且通常不相同。

Berns \[ 1 \] ： Berns、 *Billmeyer 和 Saltzman 的色彩技術原則，也就是* 3 <sub>rd</sub> Ed。 John Wiley & 兒子 (2000) 。

Berns \[ 2 \] ： Berns and Katoh，適用于電腦控制之 CRT 的數位 to radiometric transfer 函式會顯示， *CIE 專家 Symposium 的97色彩標準，適用于影像處理技術*，1997年11月。

Berns \[ 3 \] ： Berns、Fernandez 和 Taplin，Black-Level Computer-Controlled 顯示器、 *色彩研究和應用程式*、28: 379-383 Wiley 期刊、inc. (2003 的排放量進行評估) 

Kang \[ 1 \] ： Kang， *適用于電子影像裝置的色彩技術*，SPIE (1997) 

Katoh \[ 1 \] ： Katoh、Deguchi 和 BERNS、CRT 監視器的精確特性 (II) 提案適用于 CIE 方法的延伸模組，以及其驗證（ *Opt* ） 8: 397-408 (2001) 

### <a name="lcd-device-model-baseline"></a>LCD 裝置型號基準

LCD 裝置型號基準和 CRT 裝置型號基準類似。 本節將說明 LCD 模型與 CRT 模型有何不同的方式。

其中一個不同之處在于，您無法假設 LCD 顯示遵循用於 Crt 的 GOG 模型，而且會以測量資料的插補來取得語氣曲線。 因此，應更頻繁地取樣裝置中性軸。

以下是一些可為 LCD 裝置型號基準產生良好資料的典型範例值：

Red： R = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、G = B = 0

綠色： G = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = B = 0

Blue： B = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = G = 0

Neutrals： R = G = B = 0、15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255。

平均測量色彩 chromaticies 來取得裝置主要複本 chromaticities 的程式對於 Lcd 來說更重要，因為它是用於 Crt。 在 chromaticity 的 *xy* 平面上繪製 XYZ 測量時，[圖 1] 中會顯示一般情況。 請注意 chromaticity 偏離到黑點的方式。 這是因為所有 Lcd 都有特定數量的燈光流失。

![圖表，顯示使用未經修正之原始資料的 chromaticity 圖表。](images/cdmp-lcd-dmp-figure1.png)

**圖 1** ：使用未經修正之原始資料的 chromaticity 圖

從原始的 XYZ 測量中減去這項功能時，會在 [圖 2] 中描述一般情況。 這些點現在已叢集化大約三個中心，但它們在其上並不相同。 Crt 所述的平均進程可大幅改善 Lcd 的結果。

![此圖顯示使用原始資料搭配已調整之黑色點的 chromaticity 圖表。](images/cdmp-lcd-dmp-figure2.png)

**圖 2** ：使用已調整之黑色點的資料 chromaticity 圖

### <a name="rgb-capture-device-model-baseline"></a>RGB 捕獲裝置模型基準

基準 RGB 捕獲裝置模型是 IDeviceModel 類別的子類別。 在色彩捕獲裝置（如掃描器和數位攝影機）的色度特性中，會使用下列方法。 使用 capture 裝置來捕捉含有已知 CIEXYZ 值之色彩修補程式的目標。 捕捉的結果是 RGB 點陣圖影像，其中每個修補程式的色彩會以 RGB 值編碼。 這些裝置 RGB 值專屬於特定的捕獲裝置。 色度特性的目標是要建立裝置 RGB 值與 CIEXYZ 值之間的經驗關聯性，或從 RGB 到 XYZ 的數學轉換，讓模型盡可能精確地模型化。

這類數學轉換可以藉由低度的 polynomials 來合理模型化。 此程式詳述于文獻中，例如 Kang \[ 92 \] 、Kang \[ 97 \] 。 在 Kang \[ 97 中 \] ，報告的方法會在 R、G 和 B 變數中使用一組3、6、8、9、11、14或20個詞彙的 polynomials，而第三個 polynomials 回歸分別放在 CIEXYZ 空間的 X、Y、Z 元件中。 針對20詞彙多項式，格式為：

![顯示20詞彙多項式。](images/cdmp-formula20.png)

Y 和 Z 有類似的運算式。用於調整 polynomials 的數學技巧會落在「多變數線性回歸」內，並在統計資料中的任何基本文字中說明。

這種線性回歸方法不能將「右方」目標函數最小化。 根據設計，線性回歸會尋找最小平方的方案，這表示所取得的係數會將基礎空間中誤差的總總和降至最低，或等同于 Euclidean 距離的平方總和。 在實務上，您想要將平方的總和降至最低？Es，哪裡？E 是其中一個接受的標準，例如 CIE94。 將此目標函數最小化是非線性回歸問題。

在新的引擎中，實驗室到 XYZ 是回歸入的 CIE 色彩空間，而20詞彙的三次多項式則是做為捕獲裝置的模型，或係數 ls，例如 bs，讓下列 polynomials 將平方的總和降至最低？E <sub>CIE94</sub> s。

![顯示一組多項式公式。](images/cdmp-formula21.png)

解決方案 ( *l <sub>i</sub>*， *<sub>i</sub>*， *b <sub>i</sub>* ) 在60維度實數的網際空間 **R** 203 中，這種情況下的總錯誤最小化：

![顯示要最小化的錯誤總數。](images/cdmp-formula22.png)

其中的總和是透過所有資料點配對 (*R <sub>i</sub>*、*G <sub>i</sub>*、*B <sub>i</sub>*;*L <sub>i</sub>*、*u <sub>i</sub>*、*v <sub>i</sub>* ) 在取樣的資料集中，再加上其他控制點以詳述如下。 這是非線性回歸問題，因為參數 *？<sub></sub>* i、 *<sub>i</sub>*、* <sub>i</sub>* 以非線性方式進入目標函式， (不會 quadratically) 。

因為目標函數？ 是否為參數的非線性 (和 nonquadratic) 函數 *？<sub></sub>我*、 *<sub>i</sub>* 和 * <sub>i</sub>*，您必須使用反復的技巧來解決優化問題。 因為目標函式的形式是平方的總和，所以會使用稱為 Levenberg-Marquardt 演算法的標準優化技術。 這是針對非線性最小平方問題所選擇的方法。 針對 Levenberg-Marquardt 之類的反復演算法，您必須提供初始猜測。 在尋找正確的最小值時，良好的初始猜測通常很重要。 在這種情況下，初步猜測的一個絕佳候選項是線性回歸問題的解決方案。 首先，藉由定義二個目標函式，將實驗室空間中 Euclidean 距離的平方總和降至最低：

![顯示定義的二次目標函數。](images/cdmp-formula23.png)

這類「線性最小平方」問題的數學解決方案已知。 因為 *？<sub>我</sub>* 只顯示在 *L* 模型中， *<sub>我</sub>* 只顯示在 *u* 模型中，而 * <sub>i</sub>* 只出現在 *v* 模型中;優化問題可以分解成三個 subproblems：一個用於 *L*、一個用於 *u* ，另一個用於 *v*。 考慮 *l* 方等。  (*u* 方程式和 *v* 方程式，請完全遵循相同的引數。 ) 將 *L* 中的錯誤平方總和降至最低的問題，可在最小平方的意義下陳述為解決下列矩陣方程式：

![顯示 L 的矩陣方程式。](images/cdmp-formula24.png)

其中 *N* 是 (原始取樣點的資料點總數，再加上以下面所述的方式建立的控制點) 。 一般而言， *N* 是大於20，所以前面的方程式是過度決定的，需要最少的平方解決方案。 的關閉表單解決方案 **？** 可供使用：

![顯示關閉表單解決方案。](images/cdmp-formula25.png)

在實務上，使用封閉表單解決方案的直接評估不會使用，因為它的數值屬性不佳。 相反地，會將某種矩陣分解演算法套用至係數矩陣，以將方程式的系統縮減為標準格式。 在目前的執行中，單值分解 (SVD) 會套用至矩陣 **R** ，然後會解決產生的分解系統。

線性回歸問題的解決方案，以表示 ![ 線性回歸問題的解決方案。](images/cdmp-formula26.png) ，會用來做為 Levenberg-Marquardt 演算法的起點。 在此演算法中，會計算試用步驟，並將點移到更接近最佳解決方案。 試用步驟會滿足一組線性方程序，取決於目前點上衍生的功能值和值。 基於這個原因，目標函數的衍生專案？ 關於參數 *嗎？<sub></sub>我，我**是 Levenberg-Marquardt 演算法 <sub></sub> <sub></sub>的必要* 輸入。 雖然有60個參數，但有一個快捷方式可讓您計算較少的。 依微積分的鏈規則，

![顯示允許使用微積分鏈規則之快捷方式的方程式。](images/cdmp-formula27.png)

其中 *j* = 1、2、、20、 *L <sub>i</sub>*、*u <sub>i</sub>*、*v <sub>i</sub>* 是第 *i* 個取樣點的 CIELAB 值，而 *R <sub>ij</sub>* 是上面所定義之矩陣 **R** 的 (*i*，*j* ) 第一個專案。 因此，您可以使用數位向前差異來計算 *L*、*a* 和 *b* 的衍生型，而不是計算60參數的衍生。

此外，也必須設定反復演算法的停止準則。 在目前的執行中，如果 mean 平方 DECIE94 小於1，或所執行的反覆運算次數已超過10，就會終止反覆運算。 數位10來自實際的體驗，如果前幾個反復專案沒有大幅減少錯誤，則在以 oscillatory 的方式移動點時，可能不會有進一步的反復專案，亦即演算法可能無法收斂。 即使在演算法分歧的情況下，我們也可以確定 DECIE94 不會比我們所啟動的參數更糟，也就是使用從線性回歸取得的參數。

即使使用上述的非線性回歸方法，還是有幾個問題需要調整。 其中一個問題是 polynomials 傾向于在資料點以外超過或 undershoot。 在調整過程中，可能會引進人工智慧的人工 maxima 和最小值。 您可以使用低度的 polynomials 來 counteracted 這一點，這是您不應使用超過三度的原因。 更嚴重的 overshooting 或 undershooting 層面是，雖然多項式可能會採用任何真正的價值，但它嘗試建立模型的空間通常具有實體條件約束和實際的條件約束。 CIEXYZ 必須具有所有 X、Y、Z 非負的，這是實體條件約束。 在實務上，它們只會以數百（而不是上千或更高）的量值來取得值。 同樣地，CIELAB 或 CIELUV 也有自己的實體和實際條件約束。 當 RGB 空間填滿樣本點時，overshooting 或 undershooting 的問題並不嚴重。 不過，取自捕獲裝置的已捕捉 RGB 點通常不會一致地填滿 RGB 空間。 這些點可能只會填滿 RGB cube 的內部80% 或更糟的部分，它們可能位於較低的維度各種方式。 發生這種情況時，回歸 polynomials 可能會在推斷資料點以外的值時執行不佳的作業，有時會傳回不實際的預測。 您需要一個一律傳回合理實際值的模型。 這需要可有效控制回歸 polynomials 界限行為的方法，方法是將額外的成本強加于 RGB cube 界限附近的 polynomials。 進一步的量值，以確保 polynomials 一律會傳回實際值，方法是將輸出裁剪至 CIE 光譜 locus 內。

此時掃描器模型和攝影機模型會彼此分離。 攝影機模型預期會推斷至超出取樣點的區域，包括「高光」、掃描器模型不需要相同的外推。 掃描器目標應涵蓋的特性與要掃描的印刷材質類似。 掃描器模型仍然必須健全，因為它不會傳回不實際的值，但不需要在特性目標以外的範圍外推入。 為了確保穩定性，上面的 L-多項式會在100裁剪，也就是說，多項式模型會強制不要在掃描器目標的 "Dmin" 之外推斷。

攝影機模型預期會推斷為高光，因此不需要在100上進行裁剪。 相反地，會使用下列演算法。

引入了人工智慧點，以在取樣不足的區域中控制 polynomials 的行為。 藉由策略性地將這些控制點和適當的值放在一起，就能以所需的方向「提取」 polynomials。 在目前的執行中，會使用對應至 RGB cube 角落的八個控制點。 如果裝置值正規化為 unity，則這些點為：

*R* = 0、 *G* = 0、 *B* = 0

*R* = 0、 *G* = 0、 *B* = 1

*R* = 0、 *G* = 1、 *B* = 0

*R* = 0。 *G* = 1， *B* = 1

*R* = 1、 *G* = 0、 *B* = 0

*R* = 1、 *G* = 0、 *B* = 1

*R* = 1、 *G* = 1、 *B* = 0

*R* = 1、 *G* = 1、 *B* = 1

除了  =   = 與 *L* = 100、 *u* v = 0 CIELAB 值相關聯的白色 R G *B* = 1 之外，  = 下列的外推演算法會用來判斷要關聯的適當 CIELAB 值。 一般來說，針對指定的 (*r*、*g*、*b* ) ，權數會與取樣資料集中的每個 (*R <sub>i</sub>*、*G <sub>i</sub>*、*b <sub>)</sub>* 相關聯。 指派權數有兩個目標。 首先，權數與 (*r*、*g*、*b* ) 和 (*r <sub>i</sub>*、*g <sub>i</sub>*、*b <sub></sub>* ) 之間的距離成反比。 第二，您想要捨棄或指派權數0至的點，這些點與指定點的色調不同 (*R*、*G*、*B* ) 。 若要將色調列入考慮，請考慮位於錐形內的點，其頂點位於 (0，0，0) ，其軸與 (0、0、0)  (*R*、*G*、*B* ) 和其半垂直角度的線條相符？ 滿足 cos？ = 0.9。 如需此錐形的圖例，請參閱圖3。

![顯示鄰近地區形狀的圖表。](images/cdmp-lcd-dmp-figure3.png)

**圖 3** ：依角度和距離篩選範例點。 所描述的鄰近地區圖形僅供說明之用。 實際的圖形取決於所使用的距離;如果使用1個標準，則它是鑽石形的鄰近地區。

在此錐形中，會根據 RGB 距離執行第二個篩選，此距離會使用1個標準，定義于

![顯示錐形中第二個篩選的公式。](images/cdmp-formula28.png)

使用目前的錐形，初始搜尋是在0.1 距離的點（從 (*R*、*G*、*B* ) ）。 如果在此半徑內找不到任何點，則會增加0.1 的半徑，並重新啟動搜尋。 如果下一個圓形神經網路沒有任何點，則會以0.1 增加半徑。 此程式會繼續進行，直到 radius 超過 MaxDist/5 為止，其中 MaxDist = 3，以1個標準的案例為例。 如果找不到任何點，則會藉由減少 cos 來放大錐形？ 0.05，也就是增加角度？ 然後以增加的半徑重新開機整個進程。 此程式會繼續進行，直到找到非空白的點集合或 cos？ 到達0，也就是錐形已開啟成為平面。 此時，藉由增加半徑來重新開機搜尋，不同之處在于搜尋會繼續進行，直到 radius 到達 MaxDist 為止。 這可保證在最糟的情況下，將會發現非空白的點集合。 此演算法會在 [圖 4] 的流程圖中摘要說明。

![顯示演算法流程的圖表。](images/cdmp-lcd-dmp-figure4.png)

**圖 4** ：用來判斷用於輸入 RGB 值之內推樣本點集合的流程圖

假設先前的進程產生了非空白的點， (*R <sub>i</sub>*、*G <sub>i</sub>*、b ) 和 *對應 <sub></sub>* 的 (*L <sub>i</sub>*，*a <sub>i</sub>*，*b <sub>i</sub>* ) ，然後針對每個這 *類的點*，指定的 *權數 <sub></sub>*

![顯示每個點的權數公式。](images/cdmp-formula29.png)

最後，extrapolant 的定義是由

![顯示 extrapolant 的定義。](images/cdmp-formula30.png)

上述方程式組成「反向距離加權方法」的實例，通常稱為 Shepard 方法。 藉由從 eq (6) 透過演算法執行每個點，就會取得八個控制點，每個都有 *R*、*G*、*B* 和 *L*、*a*、*B* 值，並使用原始範例資料放入集區中。

若要確保模型一律會產生有效的色彩值，以及整體色彩處理管線的系統完整性和穩定性，您必須對多項式模型的輸出執行最終裁剪。 CIE 的視覺範圍是由 achromatic 元件所描述 (*Y* 或 *L* ) 以及彩色元件 (*xy* 或 *a'b '*，其與 projective 轉換) 的 XYZ 空間相關。 在目前的執行中，會使用 *a'b '* chromaticity，因為它與 CIELUV 空間直接相關。 針對任何 *CIELAB* 值，請先將 *L* 剪切至非負數值：

![顯示左至非負數值的剪切。](images/cdmp-formula31.png)

若要允許內建高光，請在100（實驗室空間中的 *l* 的「傳統」上限）裁剪 *l* 。

接下來，如果 *L* = 0，則會裁剪 *a* 和 *b* ，使 a *= b =* 0。 如果是 *L* ？ 0，計算

![如果 L = 0，則會顯示公式。](images/cdmp-formula32.png)

這些是 *a'b* 圖中的向量元件，從白色點 (*u？ '*，*v？ '* ) 至有問題的色彩。 將 CIE 光譜 locus 定義為 (*'*，*b '* ) ，由波長參數化之所有點的凸殼？：

![顯示波長的公式。](images/cdmp-formula33.png)

其中 ![ 顯示 CIE 色彩比對的函式。](images/cdmp-formula34.png) 這是兩度觀察者的 CIE 色彩比對函數。 如果向量位於 CIE locus 之外，則會將色彩裁剪為 CIE locus 上的點，也就是 locus 與向量所定義之線條的交集。 請參閱圖 5。 如果發生裁剪， *a* 和 *b* 值會先減去 *a？ '* 來重建 和 *b？* 」 從裁剪 *的 a* 和 *b*，然後乘以 13 *L*。

![顯示剪切演算法圖形的圖表。](images/cdmp-lcd-dmp-figure5.png)

**圖 5** ：裁剪 CIE 視覺範圍外的實驗室值演算法

在目前的執行中， *a'b* 」平面中的 CIE 光譜 locus 會以35區段的分段線性曲線表示， (對應到 360 nm 至 700 nm （含）) 的波長。 藉由排序線段，讓其白色點的 subtended 角度成為遞增（相當於遞減的波長），簡單的二進位搜尋就可以找到與上述向量形成的光線相交的線段。

### <a name="rgb-printer-device-model-baseline"></a>RGB 印表機裝置型號基準

RGB 印表機的裝置特性包含了裝置的經驗模型，可針對任何指定的 RGB 值預測裝置獨立的 CIELUV 色彩

有兩種方式可以建立經驗模型。 其中一種方式是使用 RGB 印表機的裝置資料，而另一種方式是流量分析參數資料。 第一個方法是使用 RGB 印表機裝置的使用者所提供的測量資料， (LUT) 來建造3-d 查閱資料表。 度量資料包含一致取樣 RGB 修補程式的 XYZ 值。 每個元件的一般取樣大小為9或17。 每個修補程式都會以 CIEXYZ 空間中的 colorimeter 或 spectrophotometer 來測量。 然後，修補程式的 XYZ 值會轉換成 CIELUV 值，形成 3-d LUT。 在裝置模型中，Sakamoto 的 tetrahedral 插補方法會套用至 3-d LUT，以預測給定 RGB 資料的 CIELUV 資料。  (將我們的專利 4275413 (Sakamoto et. ) ，美國專利 4511989 (Sakamoto) ，Kang \[ 1 \] 。 提及的兩項專利已過期。請 ) 。 第二個方法中傳遞的分析參數資料只是先前建立的 LUT。 一般而言，該 LUT 是使用第一個方法建立的，雖然它可以是手動建立的。

在目前的色彩管理中，來源對應會定義為從 RGB 空間進入與裝置無關的 CIEXYZ 色彩空間的地圖。 目的地圖定義為從裝置獨立的 CIEXYZ 色彩空間到 RGB 空間的地圖。 它是來源對應的反向。

經驗模型直接用於來源對應。 它會先將指定的 RGB 資料對應至 CIELUV 資料，並轉換成 XYZ 資料。 在目的地對應中，與裝置無關的 CIEXYZ 資料會先轉換成 CIELUV 資料。 然後，經驗模型和傳統的 Newton-Raphson 方法會用來預測 CIELUV 資料的最佳 RGB 資料。 從 CieLUV 轉換成 RGB 資料的詳細資料如下所示：

從 RGB 產生 3-d LUT 至 CieLUV 之後，會使用 RGB 上的 tetrahedral 插補來建立從 RGB 到 LUV 的對應。 此對應會以下列方程式表示：

![顯示從 R G B 到 L U V 的地圖方程式。](images/cdmp-image125.png)

地圖反轉是針對任何色彩的求解所組成 ![顯示 L U V。](images/cdmp-image127.png) ，下列非線性方程序系統：

![顯示 lolving 任何色彩 L U V 的非線性方程序。](images/cdmp-image129.png)

以傳統 Newton-Raphson 方法為基礎的非線性方程序是在新的 CTE 中使用。 初始 <sub>的猜測</sub>或 *先驗* 看到 (R 0、G 0、B 0 ) 是藉由搜尋由預先計算 (RGB、Luv) 配對之統一8x8x8 方格所組成的「種子矩陣」來取得。 選擇最接近 L u v 的 RGB 對應 Luv \* \* \* 。 種子矩陣中的每個點都會對應到資料格的中心，如此一來，反覆運算就不會以 RGB cube 界限的點開始。 換句話說，種子的 RGB 是由下列定義：步驟 = 1/8 s <sub>ijk</sub> = (步驟/2 + (i-1) 步驟、步驟/2 + (j-1) 步驟、步驟/2 + (k-1) 步驟) *，在 newton-raphson 的第一個* 步驟中，下一個預估會 ![ 顯示下一次評估的變數。](images/cdmp-image133.png) 是由公式取得：

![顯示估計值的公式。](images/cdmp-image135.png)

當 CIELUV) 空間中的錯誤 (距離小於 CTE) 中 (0.1 的預先設定容錯層級，或反覆運算數目超過 CTE (中允許的反覆運算次數上限時，會停止反復專案) 10。 容錯和反覆運算次數的值廣為人知且實證判定為有效。 在未來的版本中，容錯值可能會變更。

Jacobian 矩陣是使用向前差異來計算，但界限點 (一或多個 R、G、B 是 1) ，而改用反向差異。 線性系統不會計算 Jacobian 矩陣的反向，而是會使用具有完整切換的 Gauss-Jordan 消除來直接解決線性系統。

在反復專案結束時，仍可能無法進行聚合，因為 Newton-Raphson 是「本機」演算法，也就是說，只有當您從接近真正解決方案的初步猜測開始時，才會順利運作。 如果在 Newton-Raphson 反復專案結束時，尚未達成在預先定義的誤差容錯內的聚合，則會以一組新的種子重新開機反復專案，定義如下。

例如，目前為止取得的最佳解決方案是 (r、g、b) 。 從這個解決方案中，N posteriori 種子是衍生的，其中 N = 4。 在直覺的情況下，解決方案會在與 N 相依的步驟大小中「朝中心」移動。請參閱圖6。

![顯示解決方案更動方向的圖表。](images/cdmp-image136.png)

**圖 6** ：解決方案的更動方向取決於它所在的 octant。

換句話說，如果 r &gt; 0.5，r 通道上的值會減少，否則值會增加。 G 和 B 通道都有類似的邏輯。 精確定義如下：

更動 = 0.5/ (N + 1) 

Dir (r) =-1 如果 r &gt; 0.5; 否則為 + 1。 類似于 Dir (g) 和 Dir (b) 

第 j 個 a posteriori 種子，s????, 是 (r + Dir (r) \* j \* 更動、g + dir (g) \* j \* 更動、b + dir (b) \* j \* 更動) 

嘗試第一個???? 如果它在容錯範圍內提供新的解決方案，您可以停止。 否則，請嘗試第二秒???? 依此類推，直到第 n 秒????。

[圖 7] 顯示整個演算法的圖解。

![顯示將裝置模型反轉的流程的圖表。](images/cdmp-image138.png)

**圖 7** ：反轉裝置模型的圖解

### <a name="rgb-virtual-device-model-baseline"></a>RGB 虛擬裝置模型基準

此裝置模型 (DM) 是簡單的矩陣/語氣複製演算法。 矩陣衍生自使用標準色彩科學演算法的白色點和主要複本。 色調複製品曲線是根據 CurveType 和 ParametricType (的 ICC 描述衍生的測量參數，或視需要) 反轉。 內部演算法的詳細資料將在額外驗證高動態範圍的問題之後提供。

RGB 虛擬裝置模型是一種理想化的矩陣/語氣複製曲線 RGB，類似于 ICC 三元件矩陣設定檔的設計。 DM 的「虛擬測量」參數包含一個白色點值 (絕對 CIEXYZ) 、RGB 主要值 (絕對 CIEXYZ) ，以及以與 DMP 架構一致之 XML 格式的 ParametricCurveType 和 CurveType 為基礎的音調複製品曲線。

下表顯示在 IRGBVirtualDeviceModelBase 中的 ICC parametricCurveType 函式類型編碼和對應支援。



| 函式類型                                         | 參數                          | 類型                                     | 注意                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![顯示 ' GammaType ' 函式。](images/cdmp-image154.png)<br/> | g<br/>              | GammaType<br/>                 | 常見的執行<br/>           |
| ![顯示 ' GammaOffsetGainType ' 函式。](images/cdmp-image156.png)<br/> | ga b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![顯示 ' GammaOffsetGainOffsetType ' 函式。](images/cdmp-image158.png)<br/> | ga b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![顯示 ' GammaOffsetGainGainType ' 函式。](images/cdmp-image160.png)<br/> | ga b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2。1<br/>  (sRGB) <br/> |
| ![顯示 ' g a b c d e f ' 參數的函式。](images/cdmp-image162.png)<br/> | ga b c d e f<br/>   | N/A<br/>                       | 在 WCS 中不受支援<br/>            |



 

RGB 虛擬裝置的色調曲線會在輸入資料、pDeviceColors 和矩陣相乘之間的 DeviceToColorimetric 中套用。 若為 ColorimetricToDevice，則必須使用方法來將色調曲線反轉。 在基準執行中，這是由 DeviceToColorimetric 所使用的相同色調曲線中的直接插補來完成。

曲線應該在設定檔中指定為浮點數中的數位配對。 第一個數位代表 pDeviceColors 中的值。 第二個數字代表音訊曲線的輸出。 色調曲線中的所有值都必須介於 minColorantUsed 和 maxColorantUsed 之間。 色調曲線必須包含至少兩個專案：一個用於 minColorantUsed，一個用於 maxColorantUsed。 ToneCurve 中的專案數上限為2048。 一般而言，資料表中的專案越多，就越能更精確地建立曲率的模型。 在專案之間執行分段的線性插補。

您可以考慮替代的插補方法。 如果您知道裝置的基礎行為，則可以使用較高順序曲線更精確地使用範例和模型。 但是，如果您使用錯誤的曲線類型，就會很不精確。 如果沒有詳細資訊，您就不能猜測曲線類型。 因此，請使用線性插補並提供許多資料點。

### <a name="cmyk-printer-device-model-baseline"></a>CMYK 印表機裝置型號基準

CMYK 印表機的裝置特性包括：建立裝置的經驗模型，以預測任何指定之 CMYK 值的列印色彩。 特性也包含此模型的反轉，讓您可以指定要列印的特定色彩之 CMYK 值的處方。 這通常是根據 CIEXYZ 或 CIELAB 值來定義。

通常會使用包含 CMYK 修補程式的 IT 8.7/3 目標。 修補程式是以妥善定義的方式來取樣 CMYK 空間，如此一來，就會形成在 C、M、Y 和 K) 中具有非統一間距的矩形格線 (。 接著會使用 colorimeter 或 spectrophotometer 來測量每個修補程式。 CIEXYZ 值中的量值接著會形成一個查閱資料表 (LUT) ，其中會使用 Sakamoto 的插補方法來建立印表機的經驗模型。 美國專利 4275413 (Sakamoto et ) 、US 專利 4511989 (Sakamoto) 、Kang \[ 1 \] 。 提及的兩項專利已過期。

由 CMYK 印表機基準裝置模型接受之裝置模型設定檔所需的 CMYK 測量範例特定需求如下所示。  (範例組最清楚地描述為一組 CMY 範例 cube，每個 cube 都與特定的 K 層級相關聯。 ) 

-   至少必須為 K = 0 和 K = 100 層級提供有效的 CMY cube。
-   中繼 K 層級的間距可能不一致。
-   不含有效 CMY cube 的任何中繼 K 層級都將被忽略。
-   CMY cube 可能會使用非統一的取樣間隔 (方格間距) ，但相同的取樣間隔集合必須用於指定 K 層級之 CMY cube 中的所有 C、M 和 Y 維度。
-   每個 K 層級 CMY cube 都可以使用不同的取樣間隔數目和間距。
-   所有 CMY cube 都必須包含 CMY cube 的「角落」，也就是 CMY 範例位於 \[ 0、0、0 \] 、 \[ 0、0100 \] 、 \[ 0100、0 \] 、 \[ 100、0、0 \] 、 \[ 0100100 \] 、 \[ 100、0100 \] 、 \[ 100100、0 \] 、 \[ 100100100 \] 。
-   任何中繼 CMY 格線層級都必須在每個通道中進行完整取樣。 換句話說，CMY cube 內的每個立體方格交集都必須有一個樣本。
-   針對 K = 0 和 K = 100 CMY cube，2x2x2 「僅限角落」的 cube 是接受為有效的最小值。

    \[注意：在 K = 0 和 K = 100 層級中，3x3x3 CMY cube 將會處理為2x2x2 「僅限角落」的 cube;中繼範例層級會被忽略。 4x4x4 和大型 cube 將會使用所有的格線範例。\]

-   針對中繼 K 層級，4x4x4 CMY cube 是接受為有效的最小值。

高品質的設定檔將會使用更精細的取樣方格，而不是有效性的最小需求，通常是9x9x9x9 或更高的版本。 IT 8.7/3、IT 8.7/4 和 ECI 目標的範例會產生有效的裝置模型設定檔 (DMPs) 用於 CMYK 印表機基準裝置模型。 雖然此裝置模型可以略過這些目標中不相關的 (外網格) 範例，但並不保證可以針對其他目標執行此動作，因此建議您從會進入此裝置模型設定檔的度量集合中移除無關的樣本。

印表機模型的反轉會帶來更多的問題。 由於 CIECAM 中有輸入色彩，因此有問題指出此色彩是否在印表機範圍內。 另外還有關于色彩外觀空間中點相片順序的問題。 雖然我們可以將 CMYK 值排列成落在矩形方格上（如同在 IT 8.7/3 目標中所做的），但也不能將產生的印刷色彩視為色彩外觀空間中的色彩。 一般情況下，它們會散佈在沒有特定模式的色彩外觀空間中。

散佈點的反轉問題通常有兩種方法。 其中一個方法是使用基本三維實體（例如 tetrahedra）的印表機範圍幾何。 色彩外觀空間中的印表機色域可能會從 CMY (K) 空間的對應子格引發，請參閱「無回應 \[ 93 \] ，Kang 97」 \[ \] 。這種方法的優點是計算簡易性。 在四面體的案例中，只會在插補中使用四個點。 另一方面，結果主要取決於幾個點，這表示測量誤差會對結果產生顯著的影響。 Interpolant 也可能不會太平滑。 第二種方法不會假設任何細分，而且是以散佈資料插補的技術為基礎。 傳統的範例是 Shepard 插補的技巧，或反向加權方法 (參閱 Shepard \[ 68 \]) 。 在這裡，輸入點周圍有幾個點是以某種方式來選擇，每個都指派權數，通常與距離成正比，而 interpolant 則視為相鄰點的加權平均值。 在此方法中，相鄰點的選擇是效能的最重要。 雖然很少的點可能會導致 interpolant 不准確且不平滑，但太多點會造成高的計算成本，因為權數通常是非線性函式，而計算成本高昂。

以上所述的兩種方法都有問題。 細分方法的本質取決於合理的雜訊，而 interpolant 通常不會很流暢。 散佈的資料插補更能容忍資料雜訊，通常會提供更流暢的 interpolant，但其計算成本更高。

新的 CTE 會採用替代方法。 將 CMYK 裝置視為數個 CMY 裝置的集合，其中每個裝置都有特定的黑色 (K) 值。 使用採用做為參數亮度和色度的選取演算法，即會選擇黑色層級。 CMY 值的取得方式是使用 RGB 印表機演算法在其他地方使用的牛頓方法，將對應的 CMY 反轉為 Luv 資料表。

使用下列步驟。

1.  列印特性目標，也就是 IT 8.7/3 目標，也就是包含每個定期或不規則間距間隔之 CMYK 空間取樣的目標。
2.  使用 spectrophotometer 測量目標，並將度量轉換為 CIELUV 空間。
3.  將從 CMYK 到 Luv 的向前地圖進行結構。
4.  使用正向對應，以針對 K 值範圍的 Luv 對應來建立一組 CMY。
5.  針對任何輸入 Luv 值，您可以選取上述步驟4中所述的其中一個對應來取得對應的 CMYK 值，並使用牛頓的方法進行反轉，以取得選取的 K 值伴隨的 CMY colorant。

步驟1和2（標準程式）是由不屬於新 CTE 的程式碼剖析程式所執行。 IT 8.7/3 目標包含在 C、M、Y 和 K 各層級的所有 CMYK 值都有相當詳細的取樣。或者，您可以使用 C、M、Y 和 K 通道的統一取樣的自訂目標。 列印目標之後，就可以使用 spectrophotometer 或 colorimeter 來測量每個修補程式的 XYZ 值，而且可以使用 CIELUV 模型將 XYZ 值轉換成 Luv 值。

步驟3：在 CMYK 空間的矩形方格上套用任何已知的插補技術（例如 tetrahedral 或 multilinear 方法），即可達成將從 CMYK 到 Luv 的向前地圖結構。 在新的 CTE 中，會使用4維度的 tetrahedral 插補。 因為 CMY 取樣方格在每個層級上通常都不同，所以我們會使用超取樣的技術，如下所述。 針對指定的 CMYK 點，將 K 層級會先根據 K 值來決定。 然後，在每個 k 層級上引進「超級格線」，這是兩個 K 層級上 CMY 格線的聯集。 在每個 K 層級上，任何新引進之格線點的 Luv 值都是由該 K 層級內的3維度 tetrahedral 插補所取得。 最後，會在這個新方格上執行特定 CMYK 點的4維 tetrahedral 插補。

![顯示 supersampling 的圖表。](images/cdmp-image163.png)

**圖 8** ： Supersampling

步驟4會將一組 CMY 對 Luv 的查閱資料表 (LUTs) 。 在步驟3中所建立的向前地圖會重複呼叫，以重新取樣 CMYK 空間。 CMYK 色彩空間的取樣是使用 K 的偶數間距以及不同但仍平均間距的 CMY 取樣。

步驟5是使用任何輸入 Luv 點的步驟4中所建立的 LUTs 來取得 CMYK 值的程式。 您可以藉由分析亮度以及所要求 Luv 中的色彩程度，來選擇 K 的適當值。 選取資料表之後，就會使用牛頓的方法 (從資料表取得 CMY 值，如先前) 的 RGB 印表機裝置型號所述。

CIELUV 空間會在印表機模型中使用，而不是 CIEJab，因為裝置型號應該僅以 DMP 提供的色度資料為基礎。 DMP 包含每個已測量修補程式的色度資料（包括媒體的白色點），因此可以將 CIEXYZ 資料轉換成 CIELUV 資料。 但是，無法轉換成 CIECAM02 JCh 或 Jab，因為無法存取 DMP 中的狀況資訊。

### <a name="rgb-projector-device-model-baseline"></a>RGB 投影機裝置型號基準

注意：許多 RGB 投影機都有一個以上的操作模式。 在一種模式中（通常是預設值，而且可能稱為「簡報」），投影機的色彩回應最適合最大亮度。 不過，在此模式中，投影機無法重現輕量、稍微彩色的色彩，例如淺黃色和一些充實聲。 在另一個模式中（通常稱為「電影」、「影片」或「sRGB」），投影機最適合用來重現實際影像和自然場景。 在此模式中，最大亮度會進行取捨，以改善色彩重現的整體品質。 若要使用 RGB 投影機取得滿意的色彩複製品，必須將投影機放置在可重現平滑色彩的模式中。

![顯示 D L P 裝置模型的圖表。](images/cdmp-image167.png)

**圖 9** ： DLP 裝置模型

傳入的 RGB 值會傳遞兩個計算路徑。 第一個是矩陣模型，它會產生 XYZ 值。 這會緊接在從 XYZ 轉換成 Luv 的後面。 第二個是使用 tetrahedral 插補的非統一 LUT 插補。 插補的輸出已在 Luv 空間中（依結構）。 系統會新增這兩個輸出，以取得預測的 Luv 值。 這最後會轉換成 XYZ，也就是 DLP 裝置的色度模型預期輸出。

由於投影機是顯示裝置，因此也支援將模型反轉，也就是從 XYZ 轉換成 RGB。 由於裝置模型會將 RGB 空間轉換成 XYZ 空間，這兩者都是三維，因此反轉相當於在三個未知的情況下解決三個非線性方程序。 這可以透過標準的方程式求解技術來完成，例如，牛頓 Newton-raphson。 不過，最好先將 XYZ 轉換成 Luv，然後將 Luv 反轉為 RGB 轉換，因為 Luv 空間比 XYZ 空間更 perceptually 線性。

### <a name="icc-device-model-baseline"></a>ICC 裝置型號基準

引用的 ICC 工作流程互通性是藉由建立特殊的 ICC 裝置基準裝置模型設定檔來啟用，此設定檔會儲存設定檔物件，並使用無作業的 XYZ 設定檔建立 ICC 轉換。 然後，這項轉換會用來在裝置和 CIEXYZ 色彩之間轉譯。

![顯示 C I T E I C C 工作流程互通性的圖表。](images/cdmp-image168.png)

**圖 10** ：引用 ICC 工作流程互通性

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本色彩管理概念](basic-color-management-concepts.md)
</dt> <dt>

[Windows 色彩系統架構和演算法](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





