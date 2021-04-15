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
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a><span data-ttu-id="d85b4-118">WCS 色彩裝置模型設定檔架構和演算法</span><span class="sxs-lookup"><span data-stu-id="d85b4-118">WCS Color Device Model Profile Schema and Algorithms</span></span>

<span data-ttu-id="d85b4-119">本主題提供有關 WCS 色彩裝置模型設定檔架構及其相關演算法的資訊。</span><span class="sxs-lookup"><span data-stu-id="d85b4-119">This topic provides information about the WCS Color Device Model Profile Schema and its associated algorithms.</span></span>

<span data-ttu-id="d85b4-120">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="d85b4-120">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d85b4-121">概觀</span><span class="sxs-lookup"><span data-stu-id="d85b4-121">Overview</span></span>](#overview)
-   [<span data-ttu-id="d85b4-122">色彩裝置模型設定檔架構</span><span class="sxs-lookup"><span data-stu-id="d85b4-122">Color Device Model Profile Architecture</span></span>](#color-device-model-profile-architecture)
-   [<span data-ttu-id="d85b4-123">CDMP 架構</span><span class="sxs-lookup"><span data-stu-id="d85b4-123">The CDMP Schema</span></span>](#the-cdmp-schema)
-   [<span data-ttu-id="d85b4-124">加入 WCS CDMP 2.0 版校正</span><span class="sxs-lookup"><span data-stu-id="d85b4-124">WCS CDMP v2.0 Calibration Addition</span></span>](#wcs-cdmp-v20-calibration-addition)
-   [<span data-ttu-id="d85b4-125">CDMP 架構元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-125">The CDMP Schema Elements</span></span>](#the-cdmp-schema-elements)
    -   [<span data-ttu-id="d85b4-126">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="d85b4-126">ColorDeviceModelProfile</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="d85b4-127">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="d85b4-127">ColorDeviceModel</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="d85b4-128">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="d85b4-128">NamespaceVersion</span></span>](#namespaceversion)
    -   [<span data-ttu-id="d85b4-129">版本</span><span class="sxs-lookup"><span data-stu-id="d85b4-129">Version</span></span>](#namespaceversion)
    -   [<span data-ttu-id="d85b4-130">文件集</span><span class="sxs-lookup"><span data-stu-id="d85b4-130">Documentation</span></span>](#documentation)
    -   [<span data-ttu-id="d85b4-131">CRTDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-131">CRTDevice element</span></span>](#crtdevice-element)
    -   [<span data-ttu-id="d85b4-132">LCDDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-132">LCDDevice element</span></span>](#lcddevice-element)
    -   [<span data-ttu-id="d85b4-133">ProjectorDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-133">ProjectorDevice element</span></span>](#projectordevice-element)
    -   [<span data-ttu-id="d85b4-134">ScannerDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-134">ScannerDevice element</span></span>](#scannerdevice-element)
    -   [<span data-ttu-id="d85b4-135">CameraDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-135">CameraDevice element</span></span>](#cameradevice-element)
    -   [<span data-ttu-id="d85b4-136">RGBPrinterDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-136">RGBPrinterDevice element</span></span>](#rgbprinterdevice-element)
    -   [<span data-ttu-id="d85b4-137">CMYKPrinterDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-137">CMYKPrinterDevice element</span></span>](#cmykprinterdevice-element)
    -   [<span data-ttu-id="d85b4-138">RGBVirtualDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-138">RGBVirtualDevice element</span></span>](#rgbvirtualdevice-element)
    -   [<span data-ttu-id="d85b4-139">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="d85b4-139">PlugInDeviceType</span></span>](#plugindevicetype)
    -   [<span data-ttu-id="d85b4-140">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-140">RGBVirtualMeasurementType</span></span>](#rgbvirtualmeasurementtype)
    -   [<span data-ttu-id="d85b4-141">GammaType</span><span class="sxs-lookup"><span data-stu-id="d85b4-141">GammaType</span></span>](#gammatype)
    -   [<span data-ttu-id="d85b4-142">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="d85b4-142">GammaOffsetGainType</span></span>](#gammaoffsetgaintype)
    -   [<span data-ttu-id="d85b4-143">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="d85b4-143">GammaOffsetGainLinearGainType</span></span>](#gammaoffsetgainlineargaintype)
    -   [<span data-ttu-id="d85b4-144">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="d85b4-144">ToneResponseCurvesType</span></span>](#toneresponsecurvestype)
    -   [<span data-ttu-id="d85b4-145">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="d85b4-145">GamutBoundarySamplesType</span></span>](#gamutboundarysamplestype)
    -   [<span data-ttu-id="d85b4-146">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="d85b4-146">FloatPairList</span></span>](#floatpairlist)
    -   [<span data-ttu-id="d85b4-147">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-147">CMYKPrinterMeasurementType</span></span>](#cmykprintermeasurementtype)
    -   [<span data-ttu-id="d85b4-148">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-148">RGBPrinterMeasurementType</span></span>](#rgbprintermeasurementtype)
    -   [<span data-ttu-id="d85b4-149">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-149">RGBCaptureMeasurementType</span></span>](#rgbcapturemeasurementtype)
    -   [<span data-ttu-id="d85b4-150">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-150">OneBasedIndex</span></span>](#onebasedindex)
    -   [<span data-ttu-id="d85b4-151">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-151">RGBProjectorMeasurementType</span></span>](#rgbprojectormeasurementtype)
    -   [<span data-ttu-id="d85b4-152">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-152">DisplayMeasurementType</span></span>](#displaymeasurementtype)
    -   [<span data-ttu-id="d85b4-153">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="d85b4-153">MeasurementConditionsType</span></span>](#measurementconditionstype)
    -   [<span data-ttu-id="d85b4-154">GeometryType</span><span class="sxs-lookup"><span data-stu-id="d85b4-154">GeometryType</span></span>](#geometrytype)
    -   [<span data-ttu-id="d85b4-155">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="d85b4-155">RGBPrimariesGroup</span></span>](#rgbprimariesgroup)
    -   [<span data-ttu-id="d85b4-156">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="d85b4-156">NonNegativeCMYKSampleType</span></span>](#nonnegativecmyksampletype)
    -   [<span data-ttu-id="d85b4-157">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="d85b4-157">NonNegativeRGBSampleType</span></span>](#nonnegativergbsampletype)
    -   [<span data-ttu-id="d85b4-158">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="d85b4-158">NonNegativeCMYKType</span></span>](#nonnegativecmyktype)
    -   [<span data-ttu-id="d85b4-159">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="d85b4-159">NonNegativeRGBType</span></span>](#nonnegativergbtype)
    -   [<span data-ttu-id="d85b4-160">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d85b4-160">ExtensionType</span></span>](#extensiontype)
    -   [<span data-ttu-id="d85b4-161">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-161">NonNegativeXYZType</span></span>](#nonnegativexyztype)
    -   [<span data-ttu-id="d85b4-162">XYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-162">XYZType</span></span>](#nonnegativexyztype)
-   [<span data-ttu-id="d85b4-163">CDMP 基準演算法</span><span class="sxs-lookup"><span data-stu-id="d85b4-163">The CDMP Baseline Algorithms</span></span>](#the-cdmp-baseline-algorithms)
    -   [<span data-ttu-id="d85b4-164">CRT 裝置模型基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-164">CRT Device Model Baseline</span></span>](#crt-device-model-baseline)
    -   [<span data-ttu-id="d85b4-165">LCD 裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-165">LCD Device Model Baseline</span></span>](#lcd-device-model-baseline)
    -   [<span data-ttu-id="d85b4-166">RGB 印表機裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-166">RGB Printer Device Model Baseline</span></span>](#rgb-printer-device-model-baseline)
    -   [<span data-ttu-id="d85b4-167">RGB 虛擬裝置模型基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-167">RGB Virtual Device Model Baseline</span></span>](#rgb-virtual-device-model-baseline)
    -   [<span data-ttu-id="d85b4-168">CMYK 印表機裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-168">CMYK Printer Device Model Baseline</span></span>](#cmyk-printer-device-model-baseline)
    -   [<span data-ttu-id="d85b4-169">RGB 投影機裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-169">RGB Projector Device Model Baseline</span></span>](#rgb-projector-device-model-baseline)
    -   [<span data-ttu-id="d85b4-170">ICC 裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-170">ICC Device Model Baseline</span></span>](#icc-device-model-baseline)
-   [<span data-ttu-id="d85b4-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="d85b4-171">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d85b4-172">概觀</span><span class="sxs-lookup"><span data-stu-id="d85b4-172">Overview</span></span>

<span data-ttu-id="d85b4-173">此架構可用來指定 (CDMP) 之色彩裝置模型設定檔的內容。</span><span class="sxs-lookup"><span data-stu-id="d85b4-173">This schema is used to specify the content of a color device model profile(CDMP).</span></span> <span data-ttu-id="d85b4-174">相關聯的基準演算法如下所述。</span><span class="sxs-lookup"><span data-stu-id="d85b4-174">The associated baseline algorithms are described below.</span></span>

<span data-ttu-id="d85b4-175">基本裝置模型設定檔 (DMP) 架構包含取樣測量資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-175">The basic device model profile (DMP) schema consists of the sampling measurement data.</span></span>

<span data-ttu-id="d85b4-176">DMP XML 架構的取樣元件提供基本色彩測量目標的支援，著重在針對基準裝置模型優化的一般標準目標和目標。</span><span class="sxs-lookup"><span data-stu-id="d85b4-176">The sampling component of the DMP XML schema provides support for basic color measurement targets, focusing on common standard targets and targets optimized for the baseline device models.</span></span>

<span data-ttu-id="d85b4-177">此外，裝置設定檔會提供目標裝置模型的特定資訊，並提供當目標模型無法使用時，基準回溯裝置模型可以使用的原則。</span><span class="sxs-lookup"><span data-stu-id="d85b4-177">In addition, the device profile provides specific information on the targeted device model and provides a policy that the baseline fallback device model can use if the targeted model is unavailable.</span></span> <span data-ttu-id="d85b4-178">設定檔實例可包含使用標準 XML 擴充機制的私用延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d85b4-178">The profile instances can include private extensions using standard XML extension mechanisms.</span></span>

## <a name="color-device-model-profile-architecture"></a><span data-ttu-id="d85b4-179">色彩裝置模型設定檔架構</span><span class="sxs-lookup"><span data-stu-id="d85b4-179">Color Device Model Profile Architecture</span></span>

![此圖顯示組成裝置模型設定檔的資訊。](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a><span data-ttu-id="d85b4-181">CDMP 架構</span><span class="sxs-lookup"><span data-stu-id="d85b4-181">The CDMP Schema</span></span>


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



## <a name="wcs-cdmp-v20-calibration-addition"></a><span data-ttu-id="d85b4-182">加入 WCS CDMP 2.0 版校正</span><span class="sxs-lookup"><span data-stu-id="d85b4-182">WCS CDMP v2.0 Calibration Addition</span></span>

<span data-ttu-id="d85b4-183">CDMP 架構的 **ColorDeviceModel** 元素已在 Windows 7 中更新，以包含新的校正元素。</span><span class="sxs-lookup"><span data-stu-id="d85b4-183">The **ColorDeviceModel** element of the CDMP schema has been updated in Windows 7 to include the new calibration element.</span></span> <span data-ttu-id="d85b4-184">下圖顯示 CDMP 架構的變更。</span><span class="sxs-lookup"><span data-stu-id="d85b4-184">The following shows the change to the CDMP schema.</span></span>


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



## <a name="the-cdmp-schema-elements"></a><span data-ttu-id="d85b4-185">CDMP 架構元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-185">The CDMP Schema Elements</span></span>

> [!Note]  
> <span data-ttu-id="d85b4-186">主要複本是紅色、綠色、藍色、黑色和白色的主要範例。</span><span class="sxs-lookup"><span data-stu-id="d85b4-186">Primaries are primary samples of red, green, blue, black, and white.</span></span> <span data-ttu-id="d85b4-187">主要的斜坡是從最小亮度到完整主要值的色調滑軌。</span><span class="sxs-lookup"><span data-stu-id="d85b4-187">A primary ramp is a tonal ramp from least luminance to full primary value.</span></span> <span data-ttu-id="d85b4-188">色調曲線中的專案數上限為4096。</span><span class="sxs-lookup"><span data-stu-id="d85b4-188">The maximum number of entries in a tone ramp is 4096.</span></span>

 

> [!Note]  
> <span data-ttu-id="d85b4-189">DMPs 必須有測量資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-189">DMPs are required to have measurement data.</span></span>

 

### <a name="colordevicemodelprofile"></a><span data-ttu-id="d85b4-190">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="d85b4-190">ColorDeviceModelProfile</span></span>

<span data-ttu-id="d85b4-191">這個元素的型別為 ColorDeviceModel。</span><span class="sxs-lookup"><span data-stu-id="d85b4-191">This element is of type ColorDeviceModel.</span></span>

<span data-ttu-id="d85b4-192">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-192">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="colordevicemodel"></a><span data-ttu-id="d85b4-193">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="d85b4-193">ColorDeviceModel</span></span>

<span data-ttu-id="d85b4-194">此元素是下列子項目的序列</span><span class="sxs-lookup"><span data-stu-id="d85b4-194">This element is a sequence of the following sub-elements</span></span>

1.  <span data-ttu-id="d85b4-195">ProfileName 字串，</span><span class="sxs-lookup"><span data-stu-id="d85b4-195">ProfileName string,</span></span>
2.  <span data-ttu-id="d85b4-196">選擇性描述字串，</span><span class="sxs-lookup"><span data-stu-id="d85b4-196">optional Description string,</span></span>
3.  <span data-ttu-id="d85b4-197">選用的作者字串，</span><span class="sxs-lookup"><span data-stu-id="d85b4-197">optional Author string,</span></span>
4.  <span data-ttu-id="d85b4-198">選擇性的 MeasurementConditions MeasurementConditionsType、</span><span class="sxs-lookup"><span data-stu-id="d85b4-198">optional MeasurementConditions MeasurementConditionsType,</span></span>
5.  <span data-ttu-id="d85b4-199">Self-Luminous 布林值，</span><span class="sxs-lookup"><span data-stu-id="d85b4-199">Self-Luminous Boolean,</span></span>
6.  <span data-ttu-id="d85b4-200">MaxColorant float、</span><span class="sxs-lookup"><span data-stu-id="d85b4-200">MaxColorant float,</span></span>
7.  <span data-ttu-id="d85b4-201">MinColorant float、</span><span class="sxs-lookup"><span data-stu-id="d85b4-201">MinColorant float,</span></span>
8.  <span data-ttu-id="d85b4-202">元素的選擇</span><span class="sxs-lookup"><span data-stu-id="d85b4-202">Choice of elements</span></span>
    1.  <span data-ttu-id="d85b4-203">CRTDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-203">CRTDevice,</span></span>
    2.  <span data-ttu-id="d85b4-204">LCDDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-204">LCDDevice,</span></span>
    3.  <span data-ttu-id="d85b4-205">RGBProjectorDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-205">RGBProjectorDevice,</span></span>
    4.  <span data-ttu-id="d85b4-206">ScannerDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-206">ScannerDevice,</span></span>
    5.  <span data-ttu-id="d85b4-207">CameraDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-207">CameraDevice,</span></span>
    6.  <span data-ttu-id="d85b4-208">RGBPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-208">RGBPrinterDevice,</span></span>
    7.  <span data-ttu-id="d85b4-209">CMYKPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-209">CMYKPrinterDevice,</span></span>
    8.  <span data-ttu-id="d85b4-210">RGBVirtualDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-210">RGBVirtualDevice,</span></span>
9.  <span data-ttu-id="d85b4-211">PlugInDevice,</span><span class="sxs-lookup"><span data-stu-id="d85b4-211">PlugInDevice,</span></span>
10. <span data-ttu-id="d85b4-212">選用擴充 ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d85b4-212">optional Extension ExtensionType</span></span>

<span data-ttu-id="d85b4-213">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-213">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="d85b4-214">字串子項目的最大值為10000個字元。</span><span class="sxs-lookup"><span data-stu-id="d85b4-214">String sub-elements have a maximum of 10,000 characters.</span></span> <span data-ttu-id="d85b4-215">MaxColorant 子項目必須大於或等於零 (0) 且大於 MinColorant 子項目。</span><span class="sxs-lookup"><span data-stu-id="d85b4-215">The MaxColorant sub-element must be greater than or equal to zero (0) and greater than the MinColorant sub-element.</span></span> <span data-ttu-id="d85b4-216">MinColorant 可以是負數。</span><span class="sxs-lookup"><span data-stu-id="d85b4-216">The MinColorant can be negative.</span></span>

### <a name="namespaceversion"></a><span data-ttu-id="d85b4-217">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="d85b4-217">NamespaceVersion</span></span>

<span data-ttu-id="d85b4-218">xmlns： cdm = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="d85b4-218">xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

<span data-ttu-id="d85b4-219">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="d85b4-219">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

### <a name="version"></a><span data-ttu-id="d85b4-220">版本</span><span class="sxs-lookup"><span data-stu-id="d85b4-220">Version</span></span>

<span data-ttu-id="d85b4-221">Version = "1.0" 與 Windows Vista 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d85b4-221">Version = "1.0" with Windows Vista.</span></span>

<span data-ttu-id="d85b4-222">**驗證條件：** 任何版本值 &gt; 0.1 或 &lt; = 2.0 都有效，可支援格式的非重大變更。</span><span class="sxs-lookup"><span data-stu-id="d85b4-222">**Validation conditions:** Any version value &gt;0.1 or &lt;=2.0 is valid to support non-breaking changes to the format.</span></span>

### <a name="documentation"></a><span data-ttu-id="d85b4-223">文件</span><span class="sxs-lookup"><span data-stu-id="d85b4-223">Documentation</span></span>

<span data-ttu-id="d85b4-224">裝置模型設定檔架構。</span><span class="sxs-lookup"><span data-stu-id="d85b4-224">Device Model Profile schema.</span></span>

<span data-ttu-id="d85b4-225">著作權 (C) Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d85b4-225">Copyright (C) Microsoft.</span></span> <span data-ttu-id="d85b4-226">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="d85b4-226">All rights reserved.</span></span>

### <a name="crtdevice-element"></a><span data-ttu-id="d85b4-227">CRTDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-227">CRTDevice element</span></span>

<span data-ttu-id="d85b4-228">這個元素是 MeasurementData DisplayMeasurementType 的子項目序列。</span><span class="sxs-lookup"><span data-stu-id="d85b4-228">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="d85b4-229">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-229">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="lcddevice-element"></a><span data-ttu-id="d85b4-230">LCDDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-230">LCDDevice element</span></span>

<span data-ttu-id="d85b4-231">這個元素是 MeasurementData DisplayMeasurementType 的子項目序列。</span><span class="sxs-lookup"><span data-stu-id="d85b4-231">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="d85b4-232">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-232">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="projectordevice-element"></a><span data-ttu-id="d85b4-233">ProjectorDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-233">ProjectorDevice element</span></span>

<span data-ttu-id="d85b4-234">這個元素是 MeasurementData RGBProjectorMeasurementType 的子項目序列。</span><span class="sxs-lookup"><span data-stu-id="d85b4-234">This element is a sequence of sub-elements of a MeasurementData RGBProjectorMeasurementType.</span></span>

<span data-ttu-id="d85b4-235">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-235">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="scannerdevice-element"></a><span data-ttu-id="d85b4-236">ScannerDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-236">ScannerDevice element</span></span>

<span data-ttu-id="d85b4-237">此元素是 MeasurementData RGBCaptureMeasurementType 的子項目序列</span><span class="sxs-lookup"><span data-stu-id="d85b4-237">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="d85b4-238">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-238">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cameradevice-element"></a><span data-ttu-id="d85b4-239">CameraDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-239">CameraDevice element</span></span>

<span data-ttu-id="d85b4-240">此元素是 MeasurementData RGBCaptureMeasurementType 的子項目序列</span><span class="sxs-lookup"><span data-stu-id="d85b4-240">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="d85b4-241">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-241">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbprinterdevice-element"></a><span data-ttu-id="d85b4-242">RGBPrinterDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-242">RGBPrinterDevice element</span></span>

<span data-ttu-id="d85b4-243">這個元素是 MeasurementData RGBPrinterMeasurementType 的子項目序列。</span><span class="sxs-lookup"><span data-stu-id="d85b4-243">This element is a sequence of sub-elements of a MeasurementData RGBPrinterMeasurementType.</span></span>

<span data-ttu-id="d85b4-244">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-244">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cmykprinterdevice-element"></a><span data-ttu-id="d85b4-245">CMYKPrinterDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-245">CMYKPrinterDevice element</span></span>

<span data-ttu-id="d85b4-246">這個元素是 MeasurementData CMYKPrinterMeasurementType 的子項目序列。</span><span class="sxs-lookup"><span data-stu-id="d85b4-246">This element is a sequence of sub-elements of a MeasurementData CMYKPrinterMeasurementType.</span></span>

<span data-ttu-id="d85b4-247">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-247">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbvirtualdevice-element"></a><span data-ttu-id="d85b4-248">RGBVirtualDevice 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-248">RGBVirtualDevice element</span></span>

<span data-ttu-id="d85b4-249">這個元素是 RGBVirtualMeasurementDataType 子項目的序列。</span><span class="sxs-lookup"><span data-stu-id="d85b4-249">This element is a sequence of sub-elements of a RGBVirtualMeasurementDataType.</span></span>

<span data-ttu-id="d85b4-250">**驗證條件：** 每個子項目都是由它自己的類型來驗證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-250">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="plugindevicetype"></a><span data-ttu-id="d85b4-251">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="d85b4-251">PlugInDeviceType</span></span>

<span data-ttu-id="d85b4-252">此元素是 GUID GUIDType 和任何子項目的序列。</span><span class="sxs-lookup"><span data-stu-id="d85b4-252">This element is a sequence of a GUID GUIDType and any sub-elements.</span></span>

<span data-ttu-id="d85b4-253">**驗證條件：** GUID 是用來符合 DM 外掛程式 Dll GUID。</span><span class="sxs-lookup"><span data-stu-id="d85b4-253">**Validation conditions:** The GUID is used to match the DM PlugIn Dll GUID.</span></span> <span data-ttu-id="d85b4-254">最多可以有100000個自訂子項目。</span><span class="sxs-lookup"><span data-stu-id="d85b4-254">There are a maximum of 100,000 custom sub-elements.</span></span>

### <a name="rgbvirtualmeasurementtype"></a><span data-ttu-id="d85b4-255">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-255">RGBVirtualMeasurementType</span></span>

<span data-ttu-id="d85b4-256">此元素是由下列專案組成的序列</span><span class="sxs-lookup"><span data-stu-id="d85b4-256">This element is a sequence consisting of</span></span>

1.  <span data-ttu-id="d85b4-257">RGBPrimariesGroup 群組</span><span class="sxs-lookup"><span data-stu-id="d85b4-257">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="d85b4-258">選擇</span><span class="sxs-lookup"><span data-stu-id="d85b4-258">A choice of</span></span>
3.  -   <span data-ttu-id="d85b4-259">色差補正</span><span class="sxs-lookup"><span data-stu-id="d85b4-259">Gamma</span></span>
    -   <span data-ttu-id="d85b4-260">GammaOffsetGain</span><span class="sxs-lookup"><span data-stu-id="d85b4-260">GammaOffsetGain</span></span>
    -   <span data-ttu-id="d85b4-261">GammaOffsetGainLinearGam</span><span class="sxs-lookup"><span data-stu-id="d85b4-261">GammaOffsetGainLinearGam</span></span>
    -   <span data-ttu-id="d85b4-262">ToneResponseCurves 元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-262">ToneResponseCurves elements</span></span>

4.  <span data-ttu-id="d85b4-263">選擇性的 GamutBoundarySamples GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="d85b4-263">optional GamutBoundarySamples GamutBoundarySamplesType</span></span>
5.  <span data-ttu-id="d85b4-264">時間戳記 dateTime</span><span class="sxs-lookup"><span data-stu-id="d85b4-264">TimeStamp dateTime</span></span>

<span data-ttu-id="d85b4-265">**驗證條件：** 這些類型的每個子項目都有自己的驗證條件。</span><span class="sxs-lookup"><span data-stu-id="d85b4-265">**Validation conditions:** Each sub-element of these types has its own validation conditions.</span></span>

### <a name="gammatype"></a><span data-ttu-id="d85b4-266">GammaType</span><span class="sxs-lookup"><span data-stu-id="d85b4-266">GammaType</span></span>

<span data-ttu-id="d85b4-267">這個元素是由屬性所組成的複雜型別。</span><span class="sxs-lookup"><span data-stu-id="d85b4-267">This element is a complex type consisting of the attribute</span></span>

-   <span data-ttu-id="d85b4-268">Gamma NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-268">Gamma NonNegativeFloatType</span></span>

<span data-ttu-id="d85b4-269">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-269">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgaintype"></a><span data-ttu-id="d85b4-270">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="d85b4-270">GammaOffsetGainType</span></span>

<span data-ttu-id="d85b4-271">這個元素是由屬性所組成的複雜型別。</span><span class="sxs-lookup"><span data-stu-id="d85b4-271">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="d85b4-272">Gamma NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-272">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="d85b4-273">位移 NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-273">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="d85b4-274">增益 NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-274">Gain NonNegativeFloatType</span></span>

<span data-ttu-id="d85b4-275">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-275">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgainlineargaintype"></a><span data-ttu-id="d85b4-276">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="d85b4-276">GammaOffsetGainLinearGainType</span></span>

<span data-ttu-id="d85b4-277">這個元素是由屬性所組成的複雜型別。</span><span class="sxs-lookup"><span data-stu-id="d85b4-277">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="d85b4-278">Gamma NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-278">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="d85b4-279">位移 NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-279">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="d85b4-280">增益 NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-280">Gain NonNegativeFloatType</span></span>
-   <span data-ttu-id="d85b4-281">LinearGain NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="d85b4-281">LinearGain NonNegativeFloatType</span></span>
-   <span data-ttu-id="d85b4-282">TransitionPoint NonNegativeFloatType.</span><span class="sxs-lookup"><span data-stu-id="d85b4-282">TransitionPoint NonNegativeFloatType.</span></span>

<span data-ttu-id="d85b4-283">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-283">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="toneresponsecurvestype"></a><span data-ttu-id="d85b4-284">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="d85b4-284">ToneResponseCurvesType</span></span>

<span data-ttu-id="d85b4-285">這個元素是一系列的</span><span class="sxs-lookup"><span data-stu-id="d85b4-285">This element is a sequence of</span></span>

1.  <span data-ttu-id="d85b4-286">RedTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="d85b4-286">RedTRC FloatPairList</span></span>
2.  <span data-ttu-id="d85b4-287">GreenTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="d85b4-287">GreenTRC FloatPairList</span></span>
3.  <span data-ttu-id="d85b4-288">BlueTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="d85b4-288">BlueTRC FloatPairList</span></span>

<span data-ttu-id="d85b4-289">元素也有 unsignedint 類型的屬性 TRCLength。</span><span class="sxs-lookup"><span data-stu-id="d85b4-289">The element also has an attribute TRCLength of unsignedint type.</span></span>

<span data-ttu-id="d85b4-290">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-290">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gamutboundarysamplestype"></a><span data-ttu-id="d85b4-291">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="d85b4-291">GamutBoundarySamplesType</span></span>

<span data-ttu-id="d85b4-292">這個元素是一系列的 RGB RGBTypes。</span><span class="sxs-lookup"><span data-stu-id="d85b4-292">This element is a sequence of RGB RGBTypes.</span></span>

<span data-ttu-id="d85b4-293">**驗證條件：** 目前未系結的最大值，會根據產業意見反應進行限制。</span><span class="sxs-lookup"><span data-stu-id="d85b4-293">**Validation conditions:** Currently unbounded maximum occurences, to be capped based on industry feedback.</span></span>

### <a name="floatpairlist"></a><span data-ttu-id="d85b4-294">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="d85b4-294">FloatPairList</span></span>

<span data-ttu-id="d85b4-295">此元素是簡單類型的浮點數組清單。</span><span class="sxs-lookup"><span data-stu-id="d85b4-295">This element is a simple type of list of pairs of floats.</span></span>

<span data-ttu-id="d85b4-296">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-296">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="cmykprintermeasurementtype"></a><span data-ttu-id="d85b4-297">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-297">CMYKPrinterMeasurementType</span></span>

<span data-ttu-id="d85b4-298">此元素為</span><span class="sxs-lookup"><span data-stu-id="d85b4-298">This element is a</span></span>

1. <span data-ttu-id="d85b4-299">由一連串範例 NonNegativeCMYKSampleType 組成的 ColorCube 元素順序</span><span class="sxs-lookup"><span data-stu-id="d85b4-299">sequence of ColorCube element consisting of a sequence of Sample NonNegativeCMYKSampleType</span></span>

2. <span data-ttu-id="d85b4-300">TimeStamp dateTime 屬性。</span><span class="sxs-lookup"><span data-stu-id="d85b4-300">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d85b4-301">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-301">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprintermeasurementtype"></a><span data-ttu-id="d85b4-302">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-302">RGBPrinterMeasurementType</span></span>

<span data-ttu-id="d85b4-303">此元素為</span><span class="sxs-lookup"><span data-stu-id="d85b4-303">This element is a</span></span>

1. <span data-ttu-id="d85b4-304">由一連串範例 NonNegativeRGBSampleType 組成的 ColorCube 元素順序</span><span class="sxs-lookup"><span data-stu-id="d85b4-304">sequence of ColorCube element consisting of a sequence of Sample NonNegativeRGBSampleType</span></span>

2. <span data-ttu-id="d85b4-305">TimeStamp dateTime 屬性。</span><span class="sxs-lookup"><span data-stu-id="d85b4-305">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d85b4-306">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-306">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbcapturemeasurementtype"></a><span data-ttu-id="d85b4-307">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-307">RGBCaptureMeasurementType</span></span>

<span data-ttu-id="d85b4-308">這個元素是一系列的</span><span class="sxs-lookup"><span data-stu-id="d85b4-308">This element is a sequence of</span></span>

1.  <span data-ttu-id="d85b4-309">的 PrimaryIndex complexType</span><span class="sxs-lookup"><span data-stu-id="d85b4-309">PrimaryIndex complexType of</span></span>
2.  1.  <span data-ttu-id="d85b4-310">白色 OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-310">White OneBasedIndex</span></span>
    2.  <span data-ttu-id="d85b4-311">選用的黑色 OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-311">Optional Black OneBasedIndex</span></span>
    3.  <span data-ttu-id="d85b4-312">選擇性的 Red OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-312">Optional Red OneBasedIndex</span></span>
    4.  <span data-ttu-id="d85b4-313">選擇性綠色 OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-313">Optional Green OneBasedIndex</span></span>
    5.  <span data-ttu-id="d85b4-314">選用藍色 OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-314">Optional Blue OneBasedIndex</span></span>
    6.  <span data-ttu-id="d85b4-315">選用的青色 OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-315">Optional Cyan OneBasedIndex</span></span>
    7.  <span data-ttu-id="d85b4-316">選擇性的洋紅 OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-316">Optional Magenta OneBasedIndex</span></span>
    8.  <span data-ttu-id="d85b4-317">選擇性黃色 OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-317">Optional Yellow OneBasedIndex</span></span>

3.  <span data-ttu-id="d85b4-318">OneBasedIndex 行的 NeutralIndices</span><span class="sxs-lookup"><span data-stu-id="d85b4-318">NeutralIndices of lines of OneBasedIndex</span></span>
4.  <span data-ttu-id="d85b4-319">範例 NonNegativeRGBSampleType 的 ColorSamples 序列</span><span class="sxs-lookup"><span data-stu-id="d85b4-319">ColorSamples sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="d85b4-320">元素也有 TimeStamp dateTime 屬性。</span><span class="sxs-lookup"><span data-stu-id="d85b4-320">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d85b4-321">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-321">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="onebasedindex"></a><span data-ttu-id="d85b4-322">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="d85b4-322">OneBasedIndex</span></span>

<span data-ttu-id="d85b4-323">此元素是簡單類型的限制基底不帶正負號的整數，其 minInclusive 值 = "1"。</span><span class="sxs-lookup"><span data-stu-id="d85b4-323">This element is a simple type of restriction base unsigned int with minInclusive value = "1."</span></span>

<span data-ttu-id="d85b4-324">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-324">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprojectormeasurementtype"></a><span data-ttu-id="d85b4-325">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-325">RGBProjectorMeasurementType</span></span>

<span data-ttu-id="d85b4-326">這個元素是一系列的</span><span class="sxs-lookup"><span data-stu-id="d85b4-326">This element is a sequence of</span></span>

1.  <span data-ttu-id="d85b4-327">RGBPrimariesGroup 群組</span><span class="sxs-lookup"><span data-stu-id="d85b4-327">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="d85b4-328">元素 ColorSamples 由範例 NonNegativeRGBSampleType 的順序組成</span><span class="sxs-lookup"><span data-stu-id="d85b4-328">element ColorSamples consisting of sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="d85b4-329">元素也有 TimeStamp dateTime 屬性。</span><span class="sxs-lookup"><span data-stu-id="d85b4-329">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d85b4-330">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-330">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="displaymeasurementtype"></a><span data-ttu-id="d85b4-331">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="d85b4-331">DisplayMeasurementType</span></span>

<span data-ttu-id="d85b4-332">這個元素是一系列的</span><span class="sxs-lookup"><span data-stu-id="d85b4-332">This element is a sequence of</span></span>

1.  <span data-ttu-id="d85b4-333">群組 RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="d85b4-333">group RGBPrimariesGroup</span></span>
2.  <span data-ttu-id="d85b4-334">範例 NonNegativeRGBType 序列的 GrayRamp</span><span class="sxs-lookup"><span data-stu-id="d85b4-334">GrayRamp of sequence of Sample NonNegativeRGBType</span></span>
3.  <span data-ttu-id="d85b4-335">範例 NonNegativeRGBType 序列的 RedRamp</span><span class="sxs-lookup"><span data-stu-id="d85b4-335">RedRamp of sequence of Sample NonNegativeRGBType</span></span>
4.  <span data-ttu-id="d85b4-336">範例 NonNegativeRGBType 序列的 GreenRamp</span><span class="sxs-lookup"><span data-stu-id="d85b4-336">GreenRamp of sequence of Sample NonNegativeRGBType</span></span>
5.  <span data-ttu-id="d85b4-337">範例 NonNegativeRGBType 序列的 BlueRamp</span><span class="sxs-lookup"><span data-stu-id="d85b4-337">BlueRamp of sequence of Sample NonNegativeRGBType</span></span>

<span data-ttu-id="d85b4-338">DisplayMeasurementType 元素也有 TimeStamp dateTime 屬性。</span><span class="sxs-lookup"><span data-stu-id="d85b4-338">The DisplayMeasurementType element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d85b4-339">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-339">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="measurementconditionstype"></a><span data-ttu-id="d85b4-340">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="d85b4-340">MeasurementConditionsType</span></span>

<span data-ttu-id="d85b4-341">MeasurementConditionsType 是包含下列專案的子項目序列：</span><span class="sxs-lookup"><span data-stu-id="d85b4-341">The MeasurementConditionsType is a sequence of sub-elements that contains:</span></span>

1.  <span data-ttu-id="d85b4-342">ColorSpace 限制的字串列舉值 "CIEXYZ"</span><span class="sxs-lookup"><span data-stu-id="d85b4-342">ColorSpace restricted string enumeration value of "CIEXYZ"</span></span>
2.  <span data-ttu-id="d85b4-343">選擇性的 WhitePoint NonNegativeXYZType 或 WhitePointName 字串列舉值 D50、D65、A 或 F2</span><span class="sxs-lookup"><span data-stu-id="d85b4-343">optional choice of WhitePoint NonNegativeXYZType or WhitePointName string enumeration of values D50, D65, A, or F2</span></span>
3.  <span data-ttu-id="d85b4-344">幾何 GeometryType</span><span class="sxs-lookup"><span data-stu-id="d85b4-344">Geometry GeometryType</span></span>
4.  <span data-ttu-id="d85b4-345">ApertureSize 整數（以毫米為單位）</span><span class="sxs-lookup"><span data-stu-id="d85b4-345">ApertureSize integer in millimeters</span></span>

<span data-ttu-id="d85b4-346">預設值為：</span><span class="sxs-lookup"><span data-stu-id="d85b4-346">Defaults are:</span></span>

1.  <span data-ttu-id="d85b4-347">RGB 和 CMYK 印表機：</span><span class="sxs-lookup"><span data-stu-id="d85b4-347">RGB and CMYK Printers:</span></span>
    1.  <span data-ttu-id="d85b4-348">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="d85b4-348">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d85b4-349">D50 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="d85b4-349">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="d85b4-350">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="d85b4-350">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="d85b4-351">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="d85b4-351">10mm ApertureSize</span></span>
2.  <span data-ttu-id="d85b4-352">掃描器：</span><span class="sxs-lookup"><span data-stu-id="d85b4-352">Scanners:</span></span>
    1.  <span data-ttu-id="d85b4-353">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="d85b4-353">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d85b4-354">D50 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="d85b4-354">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="d85b4-355">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="d85b4-355">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="d85b4-356">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="d85b4-356">10mm ApertureSize</span></span>
3.  <span data-ttu-id="d85b4-357">顯示和 RGB 虛擬裝置：</span><span class="sxs-lookup"><span data-stu-id="d85b4-357">Displays and RGB Virtual Device:</span></span>
    1.  <span data-ttu-id="d85b4-358">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="d85b4-358">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d85b4-359">D65 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="d85b4-359">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="d85b4-360">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="d85b4-360">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="d85b4-361">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="d85b4-361">10mm ApertureSize</span></span>
4.  <span data-ttu-id="d85b4-362">相機：</span><span class="sxs-lookup"><span data-stu-id="d85b4-362">Cameras:</span></span>
    1.  <span data-ttu-id="d85b4-363">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="d85b4-363">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d85b4-364">D65 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="d85b4-364">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="d85b4-365">直接 GeometryType</span><span class="sxs-lookup"><span data-stu-id="d85b4-365">Direct GeometryType</span></span>
    4.  <span data-ttu-id="d85b4-366">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="d85b4-366">10mm ApertureSize</span></span>

<span data-ttu-id="d85b4-367">**驗證條件：** 每個子專案的驗證都是由這些子項目的驗證條件所決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-367">**Validation conditions:** Validation of each sub-element is determined by validation conditions for those sub-elements.</span></span> <span data-ttu-id="d85b4-368">如果遺漏任何子項目，則會使用裝置模型類型特定預設值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-368">If any sub-element is missing, the device model type specific default is used.</span></span>

### <a name="geometrytype"></a><span data-ttu-id="d85b4-369">GeometryType</span><span class="sxs-lookup"><span data-stu-id="d85b4-369">GeometryType</span></span>

<span data-ttu-id="d85b4-370">String</span><span class="sxs-lookup"><span data-stu-id="d85b4-370">String</span></span>

<span data-ttu-id="d85b4-371">列舉值：</span><span class="sxs-lookup"><span data-stu-id="d85b4-371">Enumeration values:</span></span>

-   <span data-ttu-id="d85b4-372">"0/45"</span><span class="sxs-lookup"><span data-stu-id="d85b4-372">"0/45"</span></span>
-   <span data-ttu-id="d85b4-373">"0/擴散"</span><span class="sxs-lookup"><span data-stu-id="d85b4-373">"0/diffuse"</span></span>
-   <span data-ttu-id="d85b4-374">「擴散/0」</span><span class="sxs-lookup"><span data-stu-id="d85b4-374">"diffuse/0"</span></span>
-   <span data-ttu-id="d85b4-375">直接</span><span class="sxs-lookup"><span data-stu-id="d85b4-375">"Direct"</span></span>

<span data-ttu-id="d85b4-376">**驗證條件：** 除了所列的 enumberation 值以外的任何值都無效。</span><span class="sxs-lookup"><span data-stu-id="d85b4-376">**Validation conditions:** Any value except the enumberation values listed is invalid.</span></span> <span data-ttu-id="d85b4-377">這種資訊不會變更基準處理行為。</span><span class="sxs-lookup"><span data-stu-id="d85b4-377">This information will not change baseline processing behavior.</span></span>

### <a name="rgbprimariesgroup"></a><span data-ttu-id="d85b4-378">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="d85b4-378">RGBPrimariesGroup</span></span>

<span data-ttu-id="d85b4-379">這個元素是一系列的</span><span class="sxs-lookup"><span data-stu-id="d85b4-379">This element is a sequence of</span></span>

1.  <span data-ttu-id="d85b4-380">WhitePrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-380">WhitePrimary NonNegativeXYZType</span></span>
2.  <span data-ttu-id="d85b4-381">RedPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-381">RedPrimary NonNegativeXYZType</span></span>
3.  <span data-ttu-id="d85b4-382">GreenPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-382">GreenPrimary NonNegativeXYZType</span></span>
4.  <span data-ttu-id="d85b4-383">BluePrimary NonNegativeXYZTYpe</span><span class="sxs-lookup"><span data-stu-id="d85b4-383">BluePrimary NonNegativeXYZTYpe</span></span>
5.  <span data-ttu-id="d85b4-384">BlackPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-384">BlackPrimary NonNegativeXYZType</span></span>

<span data-ttu-id="d85b4-385">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-385">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyksampletype"></a><span data-ttu-id="d85b4-386">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="d85b4-386">NonNegativeCMYKSampleType</span></span>

<span data-ttu-id="d85b4-387">這個元素是一系列的</span><span class="sxs-lookup"><span data-stu-id="d85b4-387">This element is a sequence of</span></span>

1.  <span data-ttu-id="d85b4-388">CMYK NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="d85b4-388">CMYK NonNegativeCMYKType</span></span>
2.  <span data-ttu-id="d85b4-389">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-389">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="d85b4-390">元素也有選擇性的屬性標記字串</span><span class="sxs-lookup"><span data-stu-id="d85b4-390">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="d85b4-391">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-391">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbsampletype"></a><span data-ttu-id="d85b4-392">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="d85b4-392">NonNegativeRGBSampleType</span></span>

<span data-ttu-id="d85b4-393">這個元素是一系列的</span><span class="sxs-lookup"><span data-stu-id="d85b4-393">This element is a sequence of</span></span>

1.  <span data-ttu-id="d85b4-394">RGB NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="d85b4-394">RGB NonNegativeRGBType</span></span>
2.  <span data-ttu-id="d85b4-395">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-395">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="d85b4-396">元素也有選擇性的屬性標記字串</span><span class="sxs-lookup"><span data-stu-id="d85b4-396">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="d85b4-397">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-397">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyktype"></a><span data-ttu-id="d85b4-398">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="d85b4-398">NonNegativeCMYKType</span></span>

<span data-ttu-id="d85b4-399">由屬性組成的這個元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-399">This element consisting of attributes</span></span>

1.  <span data-ttu-id="d85b4-400">C float</span><span class="sxs-lookup"><span data-stu-id="d85b4-400">C float</span></span>
2.  <span data-ttu-id="d85b4-401">M 浮點數</span><span class="sxs-lookup"><span data-stu-id="d85b4-401">M float</span></span>
3.  <span data-ttu-id="d85b4-402">Y 浮點數</span><span class="sxs-lookup"><span data-stu-id="d85b4-402">Y float</span></span>
4.  <span data-ttu-id="d85b4-403">K 浮點數</span><span class="sxs-lookup"><span data-stu-id="d85b4-403">K float</span></span>

<span data-ttu-id="d85b4-404">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-404">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbtype"></a><span data-ttu-id="d85b4-405">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="d85b4-405">NonNegativeRGBType</span></span>

<span data-ttu-id="d85b4-406">由屬性組成的這個元素</span><span class="sxs-lookup"><span data-stu-id="d85b4-406">This element consisting of attributes</span></span>

1.  <span data-ttu-id="d85b4-407">R float</span><span class="sxs-lookup"><span data-stu-id="d85b4-407">R float</span></span>
2.  <span data-ttu-id="d85b4-408">G float</span><span class="sxs-lookup"><span data-stu-id="d85b4-408">G float</span></span>
3.  <span data-ttu-id="d85b4-409">B float</span><span class="sxs-lookup"><span data-stu-id="d85b4-409">B float</span></span>

<span data-ttu-id="d85b4-410">**驗證條件：** 由產業意見反應決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-410">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="extensiontype"></a><span data-ttu-id="d85b4-411">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d85b4-411">ExtensionType</span></span>

<span data-ttu-id="d85b4-412">ExtensionType 元素是任何子項目類型的序列，用於非 Microsoft 應用程式的專屬資訊。</span><span class="sxs-lookup"><span data-stu-id="d85b4-412">The ExtensionType element is a sequence of any sub-element type and is used for proprietary information from non-Microsoft applications.</span></span>

<span data-ttu-id="d85b4-413">**驗證條件：** 這個元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d85b4-413">**Validation conditions:** This element is optional.</span></span> <span data-ttu-id="d85b4-414">最多可以有1000個擴充子項目。</span><span class="sxs-lookup"><span data-stu-id="d85b4-414">There can be a maximum of 1000 extension sub-elements.</span></span>

### <a name="nonnegativexyztype"></a><span data-ttu-id="d85b4-415">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-415">NonNegativeXYZType</span></span>

<span data-ttu-id="d85b4-416">NonNegativeXYZType 元素是由 NonNegativeFloatType 三個單精確度 IEEE 浮點元素所組成，名為 "X，" "Y" 和 "Z"。</span><span class="sxs-lookup"><span data-stu-id="d85b4-416">The NonNegativeXYZType element is composed of NonNegativeFloatType three single-precision IEEE floating-point elements named "X," "Y," and "Z."</span></span> <span data-ttu-id="d85b4-417">這些值僅限於 DMP 設定檔測量值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-417">These values are limited to the DMP profiles measurement values.</span></span> <span data-ttu-id="d85b4-418">這些測量可以是絕對 (非相對) CIEXYZ 1931 反射值或絕對 (不是相對) CIEXYZ 1931 direct (transmissive) 值（每個計量平方單位）。</span><span class="sxs-lookup"><span data-stu-id="d85b4-418">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="d85b4-419">**驗證條件：** 只有真實世界的值有效，且負值的 CIEXYZ 測量值無效。</span><span class="sxs-lookup"><span data-stu-id="d85b4-419">**Validation conditions:** Only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="d85b4-420">因為這些是絕對值，所以值可以大於 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="d85b4-420">Because these are absolute values, values can be greater than 1.0f.</span></span> <span data-ttu-id="d85b4-421">任何 "X"、"Y" 或 "Z" 的合理限制。</span><span class="sxs-lookup"><span data-stu-id="d85b4-421">A reasonable limit for any "X," "Y," or "Z."</span></span> <span data-ttu-id="d85b4-422">值會任意設定為 10000.0 f。</span><span class="sxs-lookup"><span data-stu-id="d85b4-422">value is arbitrarily set to 10000.0f.</span></span>

### <a name="xyztype"></a><span data-ttu-id="d85b4-423">XYZType</span><span class="sxs-lookup"><span data-stu-id="d85b4-423">XYZType</span></span>

<span data-ttu-id="d85b4-424">XYZType 元素是由三個單精確度 IEEE 浮點值所組成： "X"、"Y" 和 "Z"。</span><span class="sxs-lookup"><span data-stu-id="d85b4-424">The XYZType element is composed of three single-precision IEEE floating-point values: "X," "Y," and "Z."</span></span>

## <a name="the-cdmp-baseline-algorithms"></a><span data-ttu-id="d85b4-425">CDMP 基準演算法</span><span class="sxs-lookup"><span data-stu-id="d85b4-425">The CDMP Baseline Algorithms</span></span>

### <a name="crt-device-model-baseline"></a><span data-ttu-id="d85b4-426">CRT 裝置模型基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-426">CRT Device Model Baseline</span></span>

<span data-ttu-id="d85b4-427">若要瞭解此模型，您必須考慮特性程式和裝置模型化。</span><span class="sxs-lookup"><span data-stu-id="d85b4-427">To understand this model, you must consider both the characterization process and the device modeling.</span></span> <span data-ttu-id="d85b4-428">在特性程式中，系統會先透過填妥 CRT 顯示裝置的顯示緩衝區，對所取得的色彩執行 XYZ 測量。</span><span class="sxs-lookup"><span data-stu-id="d85b4-428">In the characterization process, XYZ measurements are first performed on the colors obtained by filling the display buffer of a CRT display device.</span></span> <span data-ttu-id="d85b4-429">下列範例值會為基準 CRT 裝置模型產生良好的資料：</span><span class="sxs-lookup"><span data-stu-id="d85b4-429">The following example values will generate good data for the baseline CRT device model:</span></span>

<span data-ttu-id="d85b4-430">Red： R = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、G = B = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="d85b4-431">綠色： G = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = B = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="d85b4-432">Blue： B = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = G = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="d85b4-433">Neutrals： R = G = B = 0、8、16、32、64、128、192、255</span><span class="sxs-lookup"><span data-stu-id="d85b4-433">Neutrals: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255</span></span>

<span data-ttu-id="d85b4-434">也可以使用15和非線性增量以外的增量。</span><span class="sxs-lookup"><span data-stu-id="d85b4-434">Increments other than 15 and nonlinear increments can also be used.</span></span> <span data-ttu-id="d85b4-435">每個紅色、綠色、藍色和中性的斜坡都必須包含至少三個範例，但建議提供更多的範例。</span><span class="sxs-lookup"><span data-stu-id="d85b4-435">Each red, green, blue, and neutral ramp must contain at least three samples, but providing more samples is recommended.</span></span> <span data-ttu-id="d85b4-436">您必須提供純紅色、綠色、藍色、黑色和白色的範例。</span><span class="sxs-lookup"><span data-stu-id="d85b4-436">You must provide samples for pure red, green, blue, black, and white.</span></span> <span data-ttu-id="d85b4-437">這些範例不一定要有一致的間距。</span><span class="sxs-lookup"><span data-stu-id="d85b4-437">The samples do not have to be uniformly spaced.</span></span>

<span data-ttu-id="d85b4-438">建立 tristimulus 矩陣的套裝程式含兩個步驟。</span><span class="sxs-lookup"><span data-stu-id="d85b4-438">The process of building the tristimulus matrix consists of two steps.</span></span> <span data-ttu-id="d85b4-439">首先，估計黑色點的 XYZ 值或光暈。</span><span class="sxs-lookup"><span data-stu-id="d85b4-439">First, estimate the black point XYZ value, or the flare.</span></span> <span data-ttu-id="d85b4-440">此步驟主要是以 \[ 稍微修改過的 Berns 3 工作 \] 為非線性優化的目標函式為基礎。</span><span class="sxs-lookup"><span data-stu-id="d85b4-440">This step is based largely on work of Berns\[3\] with a slightly modified objective function for the nonlinear optimization.</span></span> <span data-ttu-id="d85b4-441">其次，根據步驟1中的結果，以及所有每個通道測量的平均計算來計算 tristimulus 矩陣，而不只是數位計數的最大值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-441">Second, calculate tristimulus matrix based on the result from step one and also from an averaging calculation on all of the per-channel measurements, not just the one for maximum digital count.</span></span>

<span data-ttu-id="d85b4-442">上述每個步驟都包含詳細的程式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-442">Each of these steps contains detailed procedures.</span></span> <span data-ttu-id="d85b4-443">起點是在我們的) 範例中，每個 R、G 和 B 通道的 (17 個步驟。</span><span class="sxs-lookup"><span data-stu-id="d85b4-443">The starting point is the ramps (17 steps in our example) for each of R, G, and B channels.</span></span> <span data-ttu-id="d85b4-444">在 chromaticity 的 *xy* 平面上繪製 XYZ 測量時，[圖 1] 中會顯示一般情況。</span><span class="sxs-lookup"><span data-stu-id="d85b4-444">When the XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="d85b4-445">第一步是要解決非線性優化問題，以找出「最適合」的黑色點，將 chromaticity 中的漂移降至一次流經 R、G 和 B 通道。</span><span class="sxs-lookup"><span data-stu-id="d85b4-445">Step one consists of solving a nonlinear optimization problem to find the "best fit" black point that will minimize the drift in chromaticity as one traverses along the R, G, and B channels.</span></span> <span data-ttu-id="d85b4-446">\[我們會根據 Berns 3 \] 來搜尋 ( *X <sub>k</sub>*、*Y <sub>k</sub>*、*Z <sub>k</sub>* ) ，以將下列目標函式降至最低：</span><span class="sxs-lookup"><span data-stu-id="d85b4-446">Based on Berns\[3\], we seek ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ) that minimizes the following objective function:</span></span>

![顯示 Sr、Sg 和 Sb 是 R、G 和 B 通道上的資料點組合的目標函數。](images/cdmp-formula1.png)

<span data-ttu-id="d85b4-448">其中 *s <sub>r</sub>*、*s <sub>G</sub>* 和 *s <sub>B</sub>* 是對應至 R、G 和 B 通道上點的資料點集合。</span><span class="sxs-lookup"><span data-stu-id="d85b4-448">where *S <sub>R</sub>*,*S <sub>G</sub>*, and *S<sub>B</sub>* are the set of data points corresponding to the points on the R, G, and B channels.</span></span> <span data-ttu-id="d85b4-449">針對 *任何集合，* 請定義：</span><span class="sxs-lookup"><span data-stu-id="d85b4-449">For any set *S*, define:</span></span>

![顯示定義任何集合的公式。](images/cdmp-formula2.png)

<span data-ttu-id="d85b4-451">在上述的中， \| *s* \| 是的基數，也就是集合中的點數目。  ![顯示點 chromaticity 的公式。](images/cdmp-formula3.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-451">In the preceding, \| *S* \| is the cardinality of *S*, i.e., the number of points in the set *S*. ![Shows a formula for the chromaticity of a point.](images/cdmp-formula3.png)</span></span> <span data-ttu-id="d85b4-452">點的 chromaticity 座標會顯示某 ![ 點的 formaula。](images/cdmp-formula4.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-452">is the chromaticity coordinates of the point ![Shows a formaula for a point.](images/cdmp-formula4.png)</span></span> <span data-ttu-id="d85b4-453">因此， ![ 會顯示一份平均或大容量中間的公式。 ](images/cdmp-formula5.png) 是 chromaticity 平面 *中，* 集合內所有點的平均或大容量中心。</span><span class="sxs-lookup"><span data-stu-id="d85b4-453">, so ![Shows a formula for the average or center of mass.](images/cdmp-formula5.png), is the average, or center of mass, of all the points in the set *S* in the chromaticity plane.</span></span> <span data-ttu-id="d85b4-454">因此，會 ![ 顯示第二分鐘點總和的公式。](images/cdmp-formula6.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-454">Thus, ![Shows a formula for the sum of a second moments of points.](images/cdmp-formula6.png)</span></span> <span data-ttu-id="d85b4-455">這是有關大範圍點的第二分鐘的總和，這是分佈點相關方式的量值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-455">is the sum of second moments of the points about the center of mass and is a measure of how spread out the points are about it.</span></span> <span data-ttu-id="d85b4-456">最後，會 ![ 顯示三個點點分佈的總計量值公式。](images/cdmp-formula7.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-456">Finally, ![Shows a formula for the total measure of the spread of three clusters of points.](images/cdmp-formula7.png)</span></span> <span data-ttu-id="d85b4-457">是如何分散三個點點的整體量值，以瞭解其各自的大型中心。</span><span class="sxs-lookup"><span data-stu-id="d85b4-457">is a total measure of how spread out the three clusters of points are about their respective centers of mass.</span></span>

<span data-ttu-id="d85b4-458">在的計算中 ![ ，會顯示 f 的公式 (X、Y、Z;Xk、Yk、Zk) 。](images/cdmp-formula8.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-458">In the calculation of ![Shows a formula of f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png)</span></span> <span data-ttu-id="d85b4-459">如果 ![ 顯示 X 的公式 ](images/cdmp-formula9.png) ，則會略過計算，並據以調整 *S* 的基數。</span><span class="sxs-lookup"><span data-stu-id="d85b4-459">, if ![Shows a formula for X.](images/cdmp-formula9.png) , then the calculation is skipped, and the cardinality of *S* is adjusted accordingly.</span></span>

<span data-ttu-id="d85b4-460">儘管目標函式的複雜度很明顯，但它是 *X <sub>k</sub>* 中許多 differentiable 函式的平方總和，*Y <sub>k</sub>Z <sub>k</sub>* (17 點 2 *xy* -元件 3 channel = 102，在範例) 中，因此，會適合至標準的非線性最小平方技術，例如 Levenberg-Marquardt 演算法，也就是 WCS 中使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-460">Despite the apparent complexity of the objective function, it is a sum of the squares of many differentiable functions in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 points   2 *xy* -components   3 channels = 102, in the example), and, therefore, is amenable to standard nonlinear least squares techniques, such as the Levenberg-Marquardt algorithm, which is the algorithm used in WCS.</span></span> <span data-ttu-id="d85b4-461">請注意，上述的目標函數與 Berns 3 中建議的函式不同，後者的函式會測量從大到大的距離的變異 \[ \] 數，因此當點與大量的點等距時，變異數就會是零，即使它們可能會分散到很多的內容也是一樣。</span><span class="sxs-lookup"><span data-stu-id="d85b4-461">Note that the preceding objective function is different from the one suggested in Berns\[3\] in that the latter function measures the variance of the distances from the center of mass, so that the variance is zero when the points are equidistant from the center of mass, even though they may spread out quite a bit about it.</span></span> <span data-ttu-id="d85b4-462">在此範例中，會使用第二分鐘直接 contolled 點散佈。</span><span class="sxs-lookup"><span data-stu-id="d85b4-462">In the example, the dispersion of points is contolled directly using the second moments.</span></span>

<span data-ttu-id="d85b4-463">如同適用于非線性最小平方問題的任何反復演算法，Levenberg-Marquardt 需要初步猜測。</span><span class="sxs-lookup"><span data-stu-id="d85b4-463">As with any iterative algorithm for the nonlinear least squares problem, Levenberg-Marquardt requires an initial guess.</span></span> <span data-ttu-id="d85b4-464">有兩個明顯的候選項目。</span><span class="sxs-lookup"><span data-stu-id="d85b4-464">There are two obvious candidates.</span></span> <span data-ttu-id="d85b4-465">其中一個是 (0、0、0) ;另一個則是測量的黑色點。</span><span class="sxs-lookup"><span data-stu-id="d85b4-465">One is (0, 0, 0); the other is the measured black point.</span></span> <span data-ttu-id="d85b4-466">針對 CTE，測量的黑色點會先做為初始猜測。</span><span class="sxs-lookup"><span data-stu-id="d85b4-466">For the CTE, the measured black point is first used as the initial guess.</span></span> <span data-ttu-id="d85b4-467">如果超過100個反覆運算的最大值，但未達到每個 (點的平均距離0.001 的平均距離，而此臨界值對應至目標函式) 的臨界值（ (0.001) 17 3 = 0.000051），則會執行另一輪次猜測 (0、0、0) 的反復專案。</span><span class="sxs-lookup"><span data-stu-id="d85b4-467">If a maximum of 100 iterations is exceeded without achieving a threshold of an average distance of 0.001 of each point from its center of mass (which corresponds to a threshold value of (0.001)    17   3 = 0.000051 for the objective function), then another round of iterations with the initial guess of (0, 0, 0) is performed.</span></span> <span data-ttu-id="d85b4-468">所產生的黑色點估計值是 XYZ，相較于上一回合反復專案的最佳估計值 (以測量的黑色點做為初始猜測) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-468">The resulting estimate of the black point is XYZ compared with the best estimate from the previous round of iterations (with the measured black point as the initial guess).</span></span> <span data-ttu-id="d85b4-469">使用可為目標函式提供最小值的估計值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-469">Use the estimate that gives the smallest value for the objective function.</span></span> <span data-ttu-id="d85b4-470">選擇的100反復專案和0.001 的誤差距離為每個選取的廣為人知且實證。</span><span class="sxs-lookup"><span data-stu-id="d85b4-470">The choice of 100 iterations and the error distance of 0.001 were each selected empirically.</span></span> <span data-ttu-id="d85b4-471">在未來的版本中，將錯誤距離參數化可能是合理的。</span><span class="sxs-lookup"><span data-stu-id="d85b4-471">In future versions, it might be reasonable to parameterize the error distance.</span></span>

<span data-ttu-id="d85b4-472">步驟1的結果是估計的黑色點 ( *X <sub>k</sub>*、*Y <sub>K</sub>*、*Z <sub>K</sub>* ) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-472">The result of step one is the estimated black point ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ).</span></span> <span data-ttu-id="d85b4-473">步驟二包含決定 tristimulus 矩陣，方法是將第一個步驟中取得之三個群集的點 chromaticity 平均。</span><span class="sxs-lookup"><span data-stu-id="d85b4-473">Step two consists of determining the tristimulus matrix by averaging the chromaticity of the points in the three clusters obtained in step one.</span></span> <span data-ttu-id="d85b4-474">針對 Crt，這是為了將測量錯誤的影響降到最低。</span><span class="sxs-lookup"><span data-stu-id="d85b4-474">For CRTs, this is done primarily to minimize the effects of measurement errors.</span></span> <span data-ttu-id="d85b4-475">用來平均 chromaticity 的點必須與步驟1中的優化所使用的點相同。</span><span class="sxs-lookup"><span data-stu-id="d85b4-475">The points used in averaging the chromaticity must be the same points used in the optimization in step one.</span></span> <span data-ttu-id="d85b4-476">換句話說，如果數位計數 15 (第一個點，則在優化步驟中會捨棄每個滑軌中) 的範例，而必須在平均值中完成相同的操作。</span><span class="sxs-lookup"><span data-stu-id="d85b4-476">In other words, if the first point (digital count 15, in the example) in each ramp is discarded in the optimization step, then the same must be done in the averaging.</span></span> <span data-ttu-id="d85b4-477">如果 ![ 顯示紅色和綠色通道中座標的平均 chromaticity 公式。](images/cdmp-formula10.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-477">If ![Shows formulas of averaged chromaticity for coordinates in the red and green channels.](images/cdmp-formula10.png)</span></span> <span data-ttu-id="d85b4-478">，並 ![ 顯示藍色通道中座標的平均 chromaticity 公式。](images/cdmp-formula11.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-478">, and ![Shows a formula of averaged chromaticity for coordinates in the blue channel.](images/cdmp-formula11.png)</span></span> <span data-ttu-id="d85b4-479">是紅色、綠色和藍色通道的平均 chromaticity 座標，而下列程式會決定 tristimulus 矩陣。</span><span class="sxs-lookup"><span data-stu-id="d85b4-479">are the averaged chromaticity coordinates of the red, green, and blue channels, then the following procedure determines the tristimulus matrix.</span></span> <span data-ttu-id="d85b4-480">首先，請解決3？3線性系統：</span><span class="sxs-lookup"><span data-stu-id="d85b4-480">First, solve the 3?3 linear system:</span></span>

![顯示解決3？3線性系統的程式第一個部分。](images/cdmp-formula12.png)

![顯示3？3線性系統的第二個部分。](images/cdmp-formula13.gif)![顯示3？3線性系統第二個部分結尾的 t 注標 b 值。](images/cdmp-formula14.gif)

<span data-ttu-id="d85b4-484">*X <sub>W</sub>*、*Y <sub>W</sub>*、*Z <sub>W</sub>*</span><span class="sxs-lookup"><span data-stu-id="d85b4-484">*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z<sub>W</sub>*</span></span>

![顯示解決3？3線性系統的程式最後部分。](images/cdmp-formula15.png)

<span data-ttu-id="d85b4-486">判斷出 tristimulus 矩陣之後，色調曲線的判斷會遵循標準的方法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-486">After the tristimulus matrix is determined, the determination of tone curves follows the standard approach.</span></span> <span data-ttu-id="d85b4-487">針對 CRT 顯示，會假設個別的通道會遵循 "GOG" 模型：</span><span class="sxs-lookup"><span data-stu-id="d85b4-487">For CRT displays, the individual channels are assumed to follow the "GOG" model:</span></span>

![顯示 ' G O G G ' 模型的公式。](images/cdmp-formula16.png)

<span data-ttu-id="d85b4-489">其中 *k <sub>g</sub>* 是「增益」，1-*k <sub>g</sub>* 是「位移」，而？</span><span class="sxs-lookup"><span data-stu-id="d85b4-489">where *k <sub>g</sub>* is the "gain",1 -*k<sub>g</sub>* is the "offset", and ?</span></span> <span data-ttu-id="d85b4-490">是 "gamma"。</span><span class="sxs-lookup"><span data-stu-id="d85b4-490">is the "gamma."</span></span> <span data-ttu-id="d85b4-491">Tristimulus 矩陣的反向矩陣會套用至 neutrals 的 XYZ 資料以取得線性 RGB 資料，然後使用 GOG 模型上的非線性回歸，與數位 RGB 值相互關聯。</span><span class="sxs-lookup"><span data-stu-id="d85b4-491">The inverse matrix of the tristimulus matrix is applied to the XYZ data of the neutrals to obtain the linear RGB data, which is then correlated with the digital RGB values using nonlinear regression on the GOG model.</span></span> <span data-ttu-id="d85b4-492">對 R、G 和 B 通道而言，這些特性不一定相同，而且通常不相同。</span><span class="sxs-lookup"><span data-stu-id="d85b4-492">These characteristics do not have to be the same for the R, G, and B channels, and generally are not the same.</span></span>

<span data-ttu-id="d85b4-493">Berns \[ 1 \] ： Berns、 *Billmeyer 和 Saltzman 的色彩技術原則，也就是* 3 <sub>rd</sub> Ed。</span><span class="sxs-lookup"><span data-stu-id="d85b4-493">Berns\[1\]: Berns, *Billmeyer and Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed.</span></span> <span data-ttu-id="d85b4-494">John Wiley & 兒子 (2000) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-494">John Wiley & Sons (2000).</span></span>

<span data-ttu-id="d85b4-495">Berns \[ 2 \] ： Berns and Katoh，適用于電腦控制之 CRT 的數位 to radiometric transfer 函式會顯示， *CIE 專家 Symposium 的97色彩標準，適用于影像處理技術*，1997年11月。</span><span class="sxs-lookup"><span data-stu-id="d85b4-495">Berns\[2\]: Berns and Katoh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97 Colour Standards for Imaging Technology*, Nov. 1997.</span></span>

<span data-ttu-id="d85b4-496">Berns \[ 3 \] ： Berns、Fernandez 和 Taplin，Black-Level Computer-Controlled 顯示器、 *色彩研究和應用程式*、28: 379-383 Wiley 期刊、inc. (2003 的排放量進行評估) </span><span class="sxs-lookup"><span data-stu-id="d85b4-496">Berns\[3\]: Berns, Fernandez and Taplin, Estimating Black-Level Emissions of Computer-Controlled Displays, *Color Research and Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)</span></span>

<span data-ttu-id="d85b4-497">Kang \[ 1 \] ： Kang， *適用于電子影像裝置的色彩技術*，SPIE (1997) </span><span class="sxs-lookup"><span data-stu-id="d85b4-497">Kang\[1\]: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)</span></span>

<span data-ttu-id="d85b4-498">Katoh \[ 1 \] ： Katoh、Deguchi 和 BERNS、CRT 監視器的精確特性 (II) 提案適用于 CIE 方法的延伸模組，以及其驗證（ *Opt* ） 8: 397-408 (2001) </span><span class="sxs-lookup"><span data-stu-id="d85b4-498">Katoh\[1\]: Katoh, Deguchi and Berns, An accurate characterization of CRT monitor (II) proposal for an extension to CIE method and its verification, *Opt. Rev.* 8: 397-408 (2001)</span></span>

### <a name="lcd-device-model-baseline"></a><span data-ttu-id="d85b4-499">LCD 裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-499">LCD Device Model Baseline</span></span>

<span data-ttu-id="d85b4-500">LCD 裝置型號基準和 CRT 裝置型號基準類似。</span><span class="sxs-lookup"><span data-stu-id="d85b4-500">The LCD Device Model Baseline is similar to the CRT Device Model Baseline.</span></span> <span data-ttu-id="d85b4-501">本節將說明 LCD 模型與 CRT 模型有何不同的方式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-501">This section will explain the ways in which LCD modeling differs from CRT modeling.</span></span>

<span data-ttu-id="d85b4-502">其中一個不同之處在于，您無法假設 LCD 顯示遵循用於 Crt 的 GOG 模型，而且會以測量資料的插補來取得語氣曲線。</span><span class="sxs-lookup"><span data-stu-id="d85b4-502">One difference is that you cannot assume that LCD displays follow the GOG model used for CRTs, and the tone curves are obtained by interpolation of measured data.</span></span> <span data-ttu-id="d85b4-503">因此，應更頻繁地取樣裝置中性軸。</span><span class="sxs-lookup"><span data-stu-id="d85b4-503">Because of that, the device neutral axis should be sampled more frequently.</span></span>

<span data-ttu-id="d85b4-504">以下是一些可為 LCD 裝置型號基準產生良好資料的典型範例值：</span><span class="sxs-lookup"><span data-stu-id="d85b4-504">Here are some typical example values that can generate good data for the LCD device model baseline:</span></span>

<span data-ttu-id="d85b4-505">Red： R = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、G = B = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="d85b4-506">綠色： G = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = B = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="d85b4-507">Blue： B = 15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255、R = G = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="d85b4-508">Neutrals： R = G = B = 0、15、30、45、60、75、90、105、120、135、150、165、180、195、210、225、240、255。</span><span class="sxs-lookup"><span data-stu-id="d85b4-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span></span>

<span data-ttu-id="d85b4-509">平均測量色彩 chromaticies 來取得裝置主要複本 chromaticities 的程式對於 Lcd 來說更重要，因為它是用於 Crt。</span><span class="sxs-lookup"><span data-stu-id="d85b4-509">The process of averaging measured color chromaticies to obtain the chromaticities for the device primaries is more critical for LCDs than it is for CRTs.</span></span> <span data-ttu-id="d85b4-510">在 chromaticity 的 *xy* 平面上繪製 XYZ 測量時，[圖 1] 中會顯示一般情況。</span><span class="sxs-lookup"><span data-stu-id="d85b4-510">When XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="d85b4-511">請注意 chromaticity 偏離到黑點的方式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-511">Notice how the chromaticity drifts toward the black point.</span></span> <span data-ttu-id="d85b4-512">這是因為所有 Lcd 都有特定數量的燈光流失。</span><span class="sxs-lookup"><span data-stu-id="d85b4-512">This is because all LCDs have a certain amount of light leakage.</span></span>

![圖表，顯示使用未經修正之原始資料的 chromaticity 圖表。](images/cdmp-lcd-dmp-figure1.png)

<span data-ttu-id="d85b4-514">**圖 1** ：使用未經修正之原始資料的 chromaticity 圖</span><span class="sxs-lookup"><span data-stu-id="d85b4-514">**Figure 1** : The chromaticity diagram using raw data with no correction</span></span>

<span data-ttu-id="d85b4-515">從原始的 XYZ 測量中減去這項功能時，會在 [圖 2] 中描述一般情況。</span><span class="sxs-lookup"><span data-stu-id="d85b4-515">When this is subtracted from the raw XYZ measurements, a typical situation is depicted in Figure 2.</span></span> <span data-ttu-id="d85b4-516">這些點現在已叢集化大約三個中心，但它們在其上並不相同。</span><span class="sxs-lookup"><span data-stu-id="d85b4-516">Tthe points are now clustered about three centers, although they don't fall identically on them.</span></span> <span data-ttu-id="d85b4-517">Crt 所述的平均進程可大幅改善 Lcd 的結果。</span><span class="sxs-lookup"><span data-stu-id="d85b4-517">The averaging process described for CRTs greatly improves the results for LCDs.</span></span>

![此圖顯示使用原始資料搭配已調整之黑色點的 chromaticity 圖表。](images/cdmp-lcd-dmp-figure2.png)

<span data-ttu-id="d85b4-519">**圖 2** ：使用已調整之黑色點的資料 chromaticity 圖</span><span class="sxs-lookup"><span data-stu-id="d85b4-519">**Figure 2** : The chromaticity diagram using data with adjusted black point</span></span>

### <a name="rgb-capture-device-model-baseline"></a><span data-ttu-id="d85b4-520">RGB 捕獲裝置模型基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-520">RGB Capture Device Model Baseline</span></span>

<span data-ttu-id="d85b4-521">基準 RGB 捕獲裝置模型是 IDeviceModel 類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="d85b4-521">The baseline RGB capture device model is a subclass of the IDeviceModel class.</span></span> <span data-ttu-id="d85b4-522">在色彩捕獲裝置（如掃描器和數位攝影機）的色度特性中，會使用下列方法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-522">In the colorimetric characterization of color capture devices, such as scanners and digital cameras, the following approach is used.</span></span> <span data-ttu-id="d85b4-523">使用 capture 裝置來捕捉含有已知 CIEXYZ 值之色彩修補程式的目標。</span><span class="sxs-lookup"><span data-stu-id="d85b4-523">A target consisting of color patches with known CIEXYZ values is captured using the capture device.</span></span> <span data-ttu-id="d85b4-524">捕捉的結果是 RGB 點陣圖影像，其中每個修補程式的色彩會以 RGB 值編碼。</span><span class="sxs-lookup"><span data-stu-id="d85b4-524">The result of the capture is an RGB bitmap image in which the color of each patch is encoded in an RGB value.</span></span> <span data-ttu-id="d85b4-525">這些裝置 RGB 值專屬於特定的捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="d85b4-525">These device RGB values are specific to a particular capture device.</span></span> <span data-ttu-id="d85b4-526">色度特性的目標是要建立裝置 RGB 值與 CIEXYZ 值之間的經驗關聯性，或從 RGB 到 XYZ 的數學轉換，讓模型盡可能精確地模型化。</span><span class="sxs-lookup"><span data-stu-id="d85b4-526">The goal of colorimetric characterization is to establish an empirical relationship between the device RGB values and CIEXYZ values, or a mathematical transformation from RGB to XYZ that models as accurately as possible the behavior of the capture device.</span></span>

<span data-ttu-id="d85b4-527">這類數學轉換可以藉由低度的 polynomials 來合理模型化。</span><span class="sxs-lookup"><span data-stu-id="d85b4-527">Such a mathematical transformation can be modeled reasonably by polynomials of low degrees.</span></span> <span data-ttu-id="d85b4-528">此程式詳述于文獻中，例如 Kang \[ 92 \] 、Kang \[ 97 \] 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-528">This procedure is detailed in the literature, for example Kang\[92\], Kang\[97\].</span></span> <span data-ttu-id="d85b4-529">在 Kang \[ 97 中 \] ，報告的方法會在 R、G 和 B 變數中使用一組3、6、8、9、11、14或20個詞彙的 polynomials，而第三個 polynomials 回歸分別放在 CIEXYZ 空間的 X、Y、Z 元件中。</span><span class="sxs-lookup"><span data-stu-id="d85b4-529">In Kang\[97\], an approach is reported that uses a set of three polynomials with 3, 6, 8, 9, 11, 14 or 20 terms in the R, G, and B variables, while the three polynomials regress respectively into the X, Y, Z components of the CIEXYZ space.</span></span> <span data-ttu-id="d85b4-530">針對20詞彙多項式，格式為：</span><span class="sxs-lookup"><span data-stu-id="d85b4-530">For the 20-term polynomial, the form is:</span></span>

![顯示20詞彙多項式。](images/cdmp-formula20.png)

<span data-ttu-id="d85b4-532">Y 和 Z 有類似的運算式。用於調整 polynomials 的數學技巧會落在「多變數線性回歸」內，並在統計資料中的任何基本文字中說明。</span><span class="sxs-lookup"><span data-stu-id="d85b4-532">There are similar expressions for Y and Z. The mathematical technique for fitting the polynomials falls within "Multivariate Linear Regression" and is described in any elementary text in Statistics.</span></span>

<span data-ttu-id="d85b4-533">這種線性回歸方法不能將「右方」目標函數最小化。</span><span class="sxs-lookup"><span data-stu-id="d85b4-533">This method of linear regression suffers from not minimizing the "right" objective function.</span></span> <span data-ttu-id="d85b4-534">根據設計，線性回歸會尋找最小平方的方案，這表示所取得的係數會將基礎空間中誤差的總總和降至最低，或等同于 Euclidean 距離的平方總和。</span><span class="sxs-lookup"><span data-stu-id="d85b4-534">By design, linear regression finds the least squares solution, which implies that the coefficients obtained will minimize the total sum of squares of errors in the underlying space, or equivalently, the sum of squares of the Euclidean distances.</span></span> <span data-ttu-id="d85b4-535">在實務上，您想要將平方的總和降至最低？Es，哪裡？E 是其中一個接受的標準，例如 CIE94。</span><span class="sxs-lookup"><span data-stu-id="d85b4-535">In practice, you want to minimize the sum of squares of ?Es, where ?E is one of the accepted standards such as CIE94.</span></span> <span data-ttu-id="d85b4-536">將此目標函數最小化是非線性回歸問題。</span><span class="sxs-lookup"><span data-stu-id="d85b4-536">Minimizing this objective function is a nonlinear regression problem.</span></span>

<span data-ttu-id="d85b4-537">在新的引擎中，實驗室到 XYZ 是回歸入的 CIE 色彩空間，而20詞彙的三次多項式則是做為捕獲裝置的模型，或係數 ls，例如 bs，讓下列 polynomials 將平方的總和降至最低？E <sub>CIE94</sub> s。</span><span class="sxs-lookup"><span data-stu-id="d85b4-537">In the new engine, Lab to XYZ is the CIE color space that is regressed into, and the 20-term cubic polynomial is used as the model for the capture device, or coefficients ls,as,bs such that the following polynomials minimize the sum of squares of ?E <sub>CIE94</sub> s.</span></span>

![顯示一組多項式公式。](images/cdmp-formula21.png)

<span data-ttu-id="d85b4-539">解決方案 ( *l <sub>i</sub>*， *<sub>i</sub>*， *b <sub>i</sub>* ) 在60維度實數的網際空間 **R** 203 中，這種情況下的總錯誤最小化：</span><span class="sxs-lookup"><span data-stu-id="d85b4-539">The solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) in the 60-dimensional real numeric space **R** 203 must be such that the following total error is minimized:</span></span>

![顯示要最小化的錯誤總數。](images/cdmp-formula22.png)

<span data-ttu-id="d85b4-541">其中的總和是透過所有資料點配對 (*R <sub>i</sub>*、*G <sub>i</sub>*、*B <sub>i</sub>*;*L <sub>i</sub>*、*u <sub>i</sub>*、*v <sub>i</sub>* ) 在取樣的資料集中，再加上其他控制點以詳述如下。</span><span class="sxs-lookup"><span data-stu-id="d85b4-541">where the summation is through all the data point pairs (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v<sub>i</sub>* ) in the sampled data set plus additional control points to be detailed in the following.</span></span> <span data-ttu-id="d85b4-542">這是非線性回歸問題，因為參數 *？<sub></sub>* i、 *<sub>i</sub>*、\* <sub>i</sub>\* 以非線性方式進入目標函式， (不會 quadratically) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-542">This is a nonlinear regression problem because the parameters *?<sub>i</sub>*, *a<sub>i</sub>*, \* <sub>i</sub>\* enter into the objective function in a nonlinear way (not quadratically).</span></span>

<span data-ttu-id="d85b4-543">因為目標函數？</span><span class="sxs-lookup"><span data-stu-id="d85b4-543">Because the objective function ?</span></span> <span data-ttu-id="d85b4-544">是否為參數的非線性 (和 nonquadratic) 函數 *？<sub></sub>我*、 *<sub>i</sub>* 和 \* <sub>i</sub>\*，您必須使用反復的技巧來解決優化問題。</span><span class="sxs-lookup"><span data-stu-id="d85b4-544">is a nonlinear (and nonquadratic) function of the parameters *?<sub>i</sub>*, *a<sub>i</sub>* and \* <sub>i</sub>\*, you must resort to iterative techniques to solve the optimization problem.</span></span> <span data-ttu-id="d85b4-545">因為目標函式的形式是平方的總和，所以會使用稱為 Levenberg-Marquardt 演算法的標準優化技術。</span><span class="sxs-lookup"><span data-stu-id="d85b4-545">Because the form of the objective function is a sum of squares, a standard optimization technique called the Levenberg-Marquardt algorithm is used.</span></span> <span data-ttu-id="d85b4-546">這是針對非線性最小平方問題所選擇的方法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-546">It is considered the method of choice for nonlinear least squares problems.</span></span> <span data-ttu-id="d85b4-547">針對 Levenberg-Marquardt 之類的反復演算法，您必須提供初始猜測。</span><span class="sxs-lookup"><span data-stu-id="d85b4-547">For iterative algorithms such as Levenberg-Marquardt, you must supply an initial guess.</span></span> <span data-ttu-id="d85b4-548">在尋找正確的最小值時，良好的初始猜測通常很重要。</span><span class="sxs-lookup"><span data-stu-id="d85b4-548">A good initial guess is usually critical in finding the correct minimum value.</span></span> <span data-ttu-id="d85b4-549">在這種情況下，初步猜測的一個絕佳候選項是線性回歸問題的解決方案。</span><span class="sxs-lookup"><span data-stu-id="d85b4-549">In this case, one good candidate for the initial guess is the solution of the linear regression problem.</span></span> <span data-ttu-id="d85b4-550">首先，藉由定義二個目標函式，將實驗室空間中 Euclidean 距離的平方總和降至最低：</span><span class="sxs-lookup"><span data-stu-id="d85b4-550">First, minimize the sum of the square of Euclidean distances in Lab space, by defining a quadratic objective function:</span></span>

![顯示定義的二次目標函數。](images/cdmp-formula23.png)

<span data-ttu-id="d85b4-552">這類「線性最小平方」問題的數學解決方案已知。</span><span class="sxs-lookup"><span data-stu-id="d85b4-552">The mathematical solution to such "linear least squares" problem is well known.</span></span> <span data-ttu-id="d85b4-553">因為 *？<sub>我</sub>* 只顯示在 *L* 模型中， *<sub>我</sub>* 只顯示在 *u* 模型中，而 \* <sub>i</sub>\* 只出現在 *v* 模型中;優化問題可以分解成三個 subproblems：一個用於 *L*、一個用於 *u* ，另一個用於 *v*。</span><span class="sxs-lookup"><span data-stu-id="d85b4-553">Because *?<sub>i</sub>* only appears in the *L* modeling, *a <sub>i</sub>* only appears in the *u* modeling, and \* <sub>i</sub>\* only appears in the *v* modeling; the optimization problem can be decomposed into three subproblems: one for *L*, one for *u* and one for *v*.</span></span> <span data-ttu-id="d85b4-554">考慮 *l* 方等。</span><span class="sxs-lookup"><span data-stu-id="d85b4-554">Consider the *L* equations.</span></span> <span data-ttu-id="d85b4-555"> (*u* 方程式和 *v* 方程式，請完全遵循相同的引數。 ) 將 *L* 中的錯誤平方總和降至最低的問題，可在最小平方的意義下陳述為解決下列矩陣方程式：</span><span class="sxs-lookup"><span data-stu-id="d85b4-555">(The *u* equations and the *v* equations follow exactly the same argument.) The problem of minimizing the sum of squares of errors in *L* can be stated as solving the following matrix equation in the least squares sense:</span></span>

![顯示 L 的矩陣方程式。](images/cdmp-formula24.png)

<span data-ttu-id="d85b4-557">其中 *N* 是 (原始取樣點的資料點總數，再加上以下面所述的方式建立的控制點) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-557">where *N* is the total number of data points (original sampled points plus control points created in a manner described below).</span></span> <span data-ttu-id="d85b4-558">一般而言， *N* 是大於20，所以前面的方程式是過度決定的，需要最少的平方解決方案。</span><span class="sxs-lookup"><span data-stu-id="d85b4-558">Typically, *N* is much larger than 20, so the preceding equation is over-determined, requiring a least squares solution.</span></span> <span data-ttu-id="d85b4-559">的關閉表單解決方案 **？**</span><span class="sxs-lookup"><span data-stu-id="d85b4-559">A closed form solution for **?**</span></span> <span data-ttu-id="d85b4-560">可供使用：</span><span class="sxs-lookup"><span data-stu-id="d85b4-560">is available:</span></span>

![顯示關閉表單解決方案。](images/cdmp-formula25.png)

<span data-ttu-id="d85b4-562">在實務上，使用封閉表單解決方案的直接評估不會使用，因為它的數值屬性不佳。</span><span class="sxs-lookup"><span data-stu-id="d85b4-562">In practice, direct evaluation using the closed form solution is not used because it has poor numerical properties.</span></span> <span data-ttu-id="d85b4-563">相反地，會將某種矩陣分解演算法套用至係數矩陣，以將方程式的系統縮減為標準格式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-563">Instead, some kind of matrix factorization algorithm is applied to the coefficient matrix which reduces the system of equations to a canonical form.</span></span> <span data-ttu-id="d85b4-564">在目前的執行中，單值分解 (SVD) 會套用至矩陣 **R** ，然後會解決產生的分解系統。</span><span class="sxs-lookup"><span data-stu-id="d85b4-564">In the current implementation, Singular Value Decomposition (SVD) is applied to the matrix **R** and then the resulting decomposed system is solved.</span></span>

<span data-ttu-id="d85b4-565">線性回歸問題的解決方案，以表示 ![ 線性回歸問題的解決方案。](images/cdmp-formula26.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-565">The solution to the linear regression problem, denoted by ![Shows the solution to the linear regression problem.](images/cdmp-formula26.png)</span></span> <span data-ttu-id="d85b4-566">，會用來做為 Levenberg-Marquardt 演算法的起點。</span><span class="sxs-lookup"><span data-stu-id="d85b4-566">, is used as the starting point of the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="d85b4-567">在此演算法中，會計算試用步驟，並將點移到更接近最佳解決方案。</span><span class="sxs-lookup"><span data-stu-id="d85b4-567">In this algorithm, a trial step is computed that should move the point closer to the optimal solution.</span></span> <span data-ttu-id="d85b4-568">試用步驟會滿足一組線性方程序，取決於目前點上衍生的功能值和值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-568">The trial step satisfies a set of linear equations dependent on the functional value and values of the derivatives at the current point.</span></span> <span data-ttu-id="d85b4-569">基於這個原因，目標函數的衍生專案？</span><span class="sxs-lookup"><span data-stu-id="d85b4-569">For this reason, the derivatives of the objective function ?</span></span> <span data-ttu-id="d85b4-570">關於參數 *嗎？<sub></sub>我，我\*\*是 Levenberg-Marquardt 演算法 <sub></sub> <sub></sub>的必要* 輸入。</span><span class="sxs-lookup"><span data-stu-id="d85b4-570">with respect to the parameters *?<sub>i</sub>*, *a<sub>i</sub> <sub>i</sub>* are required inputs to the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="d85b4-571">雖然有60個參數，但有一個快捷方式可讓您計算較少的。</span><span class="sxs-lookup"><span data-stu-id="d85b4-571">Although there are 60 parameters, there is a shortcut that allows you to compute a lot less.</span></span> <span data-ttu-id="d85b4-572">依微積分的鏈規則，</span><span class="sxs-lookup"><span data-stu-id="d85b4-572">By the Chain Rule of Calculus,</span></span>

![顯示允許使用微積分鏈規則之快捷方式的方程式。](images/cdmp-formula27.png)

<span data-ttu-id="d85b4-574">其中 *j* = 1、2、、20、 *L <sub>i</sub>*、*u <sub>i</sub>*、*v <sub>i</sub>* 是第 *i* 個取樣點的 CIELAB 值，而 *R <sub>ij</sub>* 是上面所定義之矩陣 **R** 的 (*i*，*j* ) 第一個專案。</span><span class="sxs-lookup"><span data-stu-id="d85b4-574">where *j* = 1, 2,  , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* are the CIELAB value of the *i* th sample point, and *R <sub>ij</sub>* is the (*i*,*j* )th entry of the matrix **R** defined above.</span></span> <span data-ttu-id="d85b4-575">因此，您可以使用數位向前差異來計算 *L*、*a* 和 *b* 的衍生型，而不是計算60參數的衍生。</span><span class="sxs-lookup"><span data-stu-id="d85b4-575">So instead of computing derivatives for 60 parameters, you can compute derivatives for *L*,*a*, and *b* using numerical forward differencing.</span></span>

<span data-ttu-id="d85b4-576">此外，也必須設定反復演算法的停止準則。</span><span class="sxs-lookup"><span data-stu-id="d85b4-576">It is also necessary to set up a stopping criterion for iterative algorithms.</span></span> <span data-ttu-id="d85b4-577">在目前的執行中，如果 mean 平方 DECIE94 小於1，或所執行的反覆運算次數已超過10，就會終止反覆運算。</span><span class="sxs-lookup"><span data-stu-id="d85b4-577">In the current implementation, the iterations are terminated if the mean square DECIE94 is less than 1, or the number of iterations performed has exceeded 10.</span></span> <span data-ttu-id="d85b4-578">數位10來自實際的體驗，如果前幾個反復專案沒有大幅減少錯誤，則在以 oscillatory 的方式移動點時，可能不會有進一步的反復專案，亦即演算法可能無法收斂。</span><span class="sxs-lookup"><span data-stu-id="d85b4-578">The number 10 comes from the practical experience that if the first few iterations do not reduce the error significantly, further iterations would not help much other than moving the point in an oscillatory manner, i.e., the algorithm may not converge.</span></span> <span data-ttu-id="d85b4-579">即使在演算法分歧的情況下，我們也可以確定 DECIE94 不會比我們所啟動的參數更糟，也就是使用從線性回歸取得的參數。</span><span class="sxs-lookup"><span data-stu-id="d85b4-579">Even in the case that the algorithm diverges, we can be sure that the DECIE94 is no worse than what we started, i.e. with the parameters obtained from linear regression.</span></span>

<span data-ttu-id="d85b4-580">即使使用上述的非線性回歸方法，還是有幾個問題需要調整。</span><span class="sxs-lookup"><span data-stu-id="d85b4-580">Even with the preceding method of nonlinear regression, there are several problems with the fitting.</span></span> <span data-ttu-id="d85b4-581">其中一個問題是 polynomials 傾向于在資料點以外超過或 undershoot。</span><span class="sxs-lookup"><span data-stu-id="d85b4-581">One problem is that the polynomials tend to overshoot or undershoot beyond the data points.</span></span> <span data-ttu-id="d85b4-582">在調整過程中，可能會引進人工智慧的人工 maxima 和最小值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-582">Artificial local maxima and minima may be introduced in the fitting process.</span></span> <span data-ttu-id="d85b4-583">您可以使用低度的 polynomials 來 counteracted 這一點，這是您不應使用超過三度的原因。</span><span class="sxs-lookup"><span data-stu-id="d85b4-583">This can be counteracted by using polynomials of low degree, which is the reason you should not use higher than three degrees.</span></span> <span data-ttu-id="d85b4-584">更嚴重的 overshooting 或 undershooting 層面是，雖然多項式可能會採用任何真正的價值，但它嘗試建立模型的空間通常具有實體條件約束和實際的條件約束。</span><span class="sxs-lookup"><span data-stu-id="d85b4-584">A more serious aspect of overshooting or undershooting is that, while a polynomial can take any real value theoretically, the space it tries to model typically has physical constraints and practical constraints.</span></span> <span data-ttu-id="d85b4-585">CIEXYZ 必須具有所有 X、Y、Z 非負的，這是實體條件約束。</span><span class="sxs-lookup"><span data-stu-id="d85b4-585">CIEXYZ must have all of X, Y, Z non-negative, which is a physical constraint.</span></span> <span data-ttu-id="d85b4-586">在實務上，它們只會以數百（而不是上千或更高）的量值來取得值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-586">In practice, they only take values in the magnitude of hundreds, not thousands or higher.</span></span> <span data-ttu-id="d85b4-587">同樣地，CIELAB 或 CIELUV 也有自己的實體和實際條件約束。</span><span class="sxs-lookup"><span data-stu-id="d85b4-587">Similarly, CIELAB or CIELUV has its own physical and practical constraints.</span></span> <span data-ttu-id="d85b4-588">當 RGB 空間填滿樣本點時，overshooting 或 undershooting 的問題並不嚴重。</span><span class="sxs-lookup"><span data-stu-id="d85b4-588">When the RGB space is filled sufficiently with sample points, the problem of overshooting or undershooting is not serious.</span></span> <span data-ttu-id="d85b4-589">不過，取自捕獲裝置的已捕捉 RGB 點通常不會一致地填滿 RGB 空間。</span><span class="sxs-lookup"><span data-stu-id="d85b4-589">However, the captured RGB points from the capture device do not usually fill up the RGB space uniformly.</span></span> <span data-ttu-id="d85b4-590">這些點可能只會填滿 RGB cube 的內部80% 或更糟的部分，它們可能位於較低的維度各種方式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-590">The points may fill up only inner the 80% of the RGB cube, or worse, they may reside in a lower dimensional manifold.</span></span> <span data-ttu-id="d85b4-591">發生這種情況時，回歸 polynomials 可能會在推斷資料點以外的值時執行不佳的作業，有時會傳回不實際的預測。</span><span class="sxs-lookup"><span data-stu-id="d85b4-591">When this happens, the regressed polynomials may do a poor job at extrapolating the values beyond the data points, sometimes returning unrealistic predictions.</span></span> <span data-ttu-id="d85b4-592">您需要一個一律傳回合理實際值的模型。</span><span class="sxs-lookup"><span data-stu-id="d85b4-592">You want a model that always returns reasonably realistic values.</span></span> <span data-ttu-id="d85b4-593">這需要可有效控制回歸 polynomials 界限行為的方法，方法是將額外的成本強加于 RGB cube 界限附近的 polynomials。</span><span class="sxs-lookup"><span data-stu-id="d85b4-593">This requires a method that can effectively control the boundary behavior of regression polynomials by imposing additional cost to those polynomials that behave erratically near the boundary of the RGB cube.</span></span> <span data-ttu-id="d85b4-594">進一步的量值，以確保 polynomials 一律會傳回實際值，方法是將輸出裁剪至 CIE 光譜 locus 內。</span><span class="sxs-lookup"><span data-stu-id="d85b4-594">A further measure to ensure that the polynomials always return realistic values is applied by clipping the output to within the CIE spectral locus.</span></span>

<span data-ttu-id="d85b4-595">此時掃描器模型和攝影機模型會彼此分離。</span><span class="sxs-lookup"><span data-stu-id="d85b4-595">It is at this point that the scanner modeling and camera modeling diverge from each other.</span></span> <span data-ttu-id="d85b4-596">攝影機模型預期會推斷至超出取樣點的區域，包括「高光」、掃描器模型不需要相同的外推。</span><span class="sxs-lookup"><span data-stu-id="d85b4-596">The camera model is expected to extrapolate to regions beyond the sampled points including the "specular highlights," the same extrapolation is not required for the scanner model.</span></span> <span data-ttu-id="d85b4-597">掃描器目標應涵蓋的特性與要掃描的印刷材質類似。</span><span class="sxs-lookup"><span data-stu-id="d85b4-597">The scanner target is expected to cover a characterization that is similar to the printed materials to be scanned.</span></span> <span data-ttu-id="d85b4-598">掃描器模型仍然必須健全，因為它不會傳回不實際的值，但不需要在特性目標以外的範圍外推入。</span><span class="sxs-lookup"><span data-stu-id="d85b4-598">The scanner model is still required to be robust in the sense that it should not return unrealistic values, but extrapolation far beyond the characterization target is not required.</span></span> <span data-ttu-id="d85b4-599">為了確保穩定性，上面的 L-多項式會在100裁剪，也就是說，多項式模型會強制不要在掃描器目標的 "Dmin" 之外推斷。</span><span class="sxs-lookup"><span data-stu-id="d85b4-599">To ensure robustness, the L-polynomial above is clipped at 100, that is, the polynomial model is forced not to extrapolate beyond "Dmin" of the scanner target.</span></span>

<span data-ttu-id="d85b4-600">攝影機模型預期會推斷為高光，因此不需要在100上進行裁剪。</span><span class="sxs-lookup"><span data-stu-id="d85b4-600">The camera model is expected to extrapolate to specular highlights, so clipping at 100 is undesirable.</span></span> <span data-ttu-id="d85b4-601">相反地，會使用下列演算法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-601">Instead, the following algorithm is used.</span></span>

<span data-ttu-id="d85b4-602">引入了人工智慧點，以在取樣不足的區域中控制 polynomials 的行為。</span><span class="sxs-lookup"><span data-stu-id="d85b4-602">Artificial control points are introduced to control the behavior of the polynomials in regions with insufficient sampling.</span></span> <span data-ttu-id="d85b4-603">藉由策略性地將這些控制點和適當的值放在一起，就能以所需的方向「提取」 polynomials。</span><span class="sxs-lookup"><span data-stu-id="d85b4-603">By strategically placing these control points with appropriate values, they serve to "pull" the polynomials in the required direction.</span></span> <span data-ttu-id="d85b4-604">在目前的執行中，會使用對應至 RGB cube 角落的八個控制點。</span><span class="sxs-lookup"><span data-stu-id="d85b4-604">In the current implementation, eight control points corresponding to the corners of the RGB cube are used.</span></span> <span data-ttu-id="d85b4-605">如果裝置值正規化為 unity，則這些點為：</span><span class="sxs-lookup"><span data-stu-id="d85b4-605">If the device values are normalized to unity, then these points are:</span></span>

<span data-ttu-id="d85b4-606">*R* = 0、 *G* = 0、 *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-606">*R* = 0, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="d85b4-607">*R* = 0、 *G* = 0、 *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d85b4-607">*R* = 0, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="d85b4-608">*R* = 0、 *G* = 1、 *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-608">*R* = 0, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="d85b4-609">*R* = 0。</span><span class="sxs-lookup"><span data-stu-id="d85b4-609">*R* = 0.</span></span> <span data-ttu-id="d85b4-610">*G* = 1， *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d85b4-610">*G* = 1, *B* = 1</span></span>

<span data-ttu-id="d85b4-611">*R* = 1、 *G* = 0、 *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-611">*R* = 1, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="d85b4-612">*R* = 1、 *G* = 0、 *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d85b4-612">*R* = 1, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="d85b4-613">*R* = 1、 *G* = 1、 *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d85b4-613">*R* = 1, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="d85b4-614">*R* = 1、 *G* = 1、 *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d85b4-614">*R* = 1, *G* = 1, *B* = 1</span></span>

<span data-ttu-id="d85b4-615">除了  =   = 與 *L* = 100、 *u* v = 0 CIELAB 值相關聯的白色 R G *B* = 1 之外，  = 下列的外推演算法會用來判斷要關聯的適當 CIELAB 值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-615">Except for the white *R* =*G* =*B* = 1, which is associated with a CIELAB value of *L* = 100, *u* =*v* = 0, the following extrapolation algorithm is used to determine the appropriate CIELAB value to be associated with.</span></span> <span data-ttu-id="d85b4-616">一般來說，針對指定的 (*r*、*g*、*b* ) ，權數會與取樣資料集中的每個 (*R <sub>i</sub>*、*G <sub>i</sub>*、*b <sub>)</sub>* 相關聯。</span><span class="sxs-lookup"><span data-stu-id="d85b4-616">Generally, for a given (*R*,*G*,*B* ), a weight is associated with each of the (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ) in the sampled data set.</span></span> <span data-ttu-id="d85b4-617">指派權數有兩個目標。</span><span class="sxs-lookup"><span data-stu-id="d85b4-617">There are two goals to assigning the weight.</span></span> <span data-ttu-id="d85b4-618">首先，權數與 (*r*、*g*、*b* ) 和 (*r <sub>i</sub>*、*g <sub>i</sub>*、*b <sub></sub>* ) 之間的距離成反比。</span><span class="sxs-lookup"><span data-stu-id="d85b4-618">First, the weight is inversely proportional to the distance between (*R*,*G*,*B* ) and (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ).</span></span> <span data-ttu-id="d85b4-619">第二，您想要捨棄或指派權數0至的點，這些點與指定點的色調不同 (*R*、*G*、*B* ) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-619">Second, you want to discard, or assign weight 0 to, points that have a different hue than the given point (*R*,*G*,*B* ).</span></span> <span data-ttu-id="d85b4-620">若要將色調列入考慮，請考慮位於錐形內的點，其頂點位於 (0，0，0) ，其軸與 (0、0、0)  (*R*、*G*、*B* ) 和其半垂直角度的線條相符？</span><span class="sxs-lookup"><span data-stu-id="d85b4-620">To take the hue into account, consider points that lie within a cone whose vertex is at (0, 0, 0), whose axis coincides with the line joining (0, 0, 0) to (*R*,*G*,*B* ), and whose semi-vertical angle ?</span></span> <span data-ttu-id="d85b4-621">滿足 cos？</span><span class="sxs-lookup"><span data-stu-id="d85b4-621">satisfies cos ?</span></span> <span data-ttu-id="d85b4-622">= 0.9。</span><span class="sxs-lookup"><span data-stu-id="d85b4-622">= 0.9.</span></span> <span data-ttu-id="d85b4-623">如需此錐形的圖例，請參閱圖3。</span><span class="sxs-lookup"><span data-stu-id="d85b4-623">See Figure 3 for an illustration of this cone.</span></span>

![顯示鄰近地區形狀的圖表。](images/cdmp-lcd-dmp-figure3.png)

<span data-ttu-id="d85b4-625">**圖 3** ：依角度和距離篩選範例點。</span><span class="sxs-lookup"><span data-stu-id="d85b4-625">**Figure 3** : Filtering the sample points by angle and distance.</span></span> <span data-ttu-id="d85b4-626">所描述的鄰近地區圖形僅供說明之用。</span><span class="sxs-lookup"><span data-stu-id="d85b4-626">The shape of the neighborhood depicted is for illustration purpose only.</span></span> <span data-ttu-id="d85b4-627">實際的圖形取決於所使用的距離;如果使用1個標準，則它是鑽石形的鄰近地區。</span><span class="sxs-lookup"><span data-stu-id="d85b4-627">The actual shape depends on the distance used; it is a diamond-shaped neighborhood if the 1-norm is used.</span></span>

<span data-ttu-id="d85b4-628">在此錐形中，會根據 RGB 距離執行第二個篩選，此距離會使用1個標準，定義于</span><span class="sxs-lookup"><span data-stu-id="d85b4-628">Within this cone, a second filtering is performed that is based on the RGB distance, which uses the 1-norm, defined by</span></span>

![顯示錐形中第二個篩選的公式。](images/cdmp-formula28.png)

<span data-ttu-id="d85b4-630">使用目前的錐形，初始搜尋是在0.1 距離的點（從 (*R*、*G*、*B* ) ）。</span><span class="sxs-lookup"><span data-stu-id="d85b4-630">With the current cone, the initial search is for points that are within a distance of 0.1 from (*R*,*G*,*B* ).</span></span> <span data-ttu-id="d85b4-631">如果在此半徑內找不到任何點，則會增加0.1 的半徑，並重新啟動搜尋。</span><span class="sxs-lookup"><span data-stu-id="d85b4-631">If no point is found within this radius, the radius is increased by 0.1, and the search is restarted.</span></span> <span data-ttu-id="d85b4-632">如果下一個圓形神經網路沒有任何點，則會以0.1 增加半徑。</span><span class="sxs-lookup"><span data-stu-id="d85b4-632">If the next round nets no point either, the radius is increased by 0.1.</span></span> <span data-ttu-id="d85b4-633">此程式會繼續進行，直到 radius 超過 MaxDist/5 為止，其中 MaxDist = 3，以1個標準的案例為例。</span><span class="sxs-lookup"><span data-stu-id="d85b4-633">This process continues until the radius exceeds MaxDist/5, where MaxDist = 3, in the case of 1-norm.</span></span> <span data-ttu-id="d85b4-634">如果找不到任何點，則會藉由減少 cos 來放大錐形？</span><span class="sxs-lookup"><span data-stu-id="d85b4-634">If no point is found, the cone is enlarged by decreasing the cos ?</span></span> <span data-ttu-id="d85b4-635">0.05，也就是增加角度？</span><span class="sxs-lookup"><span data-stu-id="d85b4-635">by 0.05, that is, increasing the angle ?</span></span> <span data-ttu-id="d85b4-636">然後以增加的半徑重新開機整個進程。</span><span class="sxs-lookup"><span data-stu-id="d85b4-636">and restarting the whole process with an increasing radius.</span></span> <span data-ttu-id="d85b4-637">此程式會繼續進行，直到找到非空白的點集合或 cos？</span><span class="sxs-lookup"><span data-stu-id="d85b4-637">This process continues until a non-empty set of points is found, or cos ?</span></span> <span data-ttu-id="d85b4-638">到達0，也就是錐形已開啟成為平面。</span><span class="sxs-lookup"><span data-stu-id="d85b4-638">reaches 0, that is, the cone has opened up to become a plane.</span></span> <span data-ttu-id="d85b4-639">此時，藉由增加半徑來重新開機搜尋，不同之處在于搜尋會繼續進行，直到 radius 到達 MaxDist 為止。</span><span class="sxs-lookup"><span data-stu-id="d85b4-639">At this point, the search is restarted by increasing the radius, except that the search continues until the radius reaches MaxDist.</span></span> <span data-ttu-id="d85b4-640">這可保證在最糟的情況下，將會發現非空白的點集合。</span><span class="sxs-lookup"><span data-stu-id="d85b4-640">This guarantees that in the worst-case scenario, a non-empty set of points will be found.</span></span> <span data-ttu-id="d85b4-641">此演算法會在 [圖 4] 的流程圖中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="d85b4-641">The algorithm is summarized in the flow diagram in Figure 4.</span></span>

![顯示演算法流程的圖表。](images/cdmp-lcd-dmp-figure4.png)

<span data-ttu-id="d85b4-643">**圖 4** ：用來判斷用於輸入 RGB 值之內推樣本點集合的流程圖</span><span class="sxs-lookup"><span data-stu-id="d85b4-643">**Figure 4** : Flow diagram for determining the set S of sample points used in the extrapolation for an input RGB value</span></span>

<span data-ttu-id="d85b4-644">假設先前的進程產生了非空白的點， (*R <sub>i</sub>*、*G <sub>i</sub>*、b ) 和 *對應 <sub></sub>* 的 (*L <sub>i</sub>*，*a <sub>i</sub>*，*b <sub>i</sub>* ) ，然後針對每個這 *類的點*，指定的 *權數 <sub></sub>*</span><span class="sxs-lookup"><span data-stu-id="d85b4-644">Assuming that the preceding process yields a non-empty set *S* of points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) and corresponding (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), then for each such point, a weight *w<sub>i</sub>* is assigned, given by</span></span>

![顯示每個點的權數公式。](images/cdmp-formula29.png)

<span data-ttu-id="d85b4-646">最後，extrapolant 的定義是由</span><span class="sxs-lookup"><span data-stu-id="d85b4-646">Finally, the extrapolant is defined by</span></span>

![顯示 extrapolant 的定義。](images/cdmp-formula30.png)

<span data-ttu-id="d85b4-648">上述方程式組成「反向距離加權方法」的實例，通常稱為 Shepard 方法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-648">The preceding equations constitute an instance of the "inverse-distance weighted methods," commonly called the Shepard methods.</span></span> <span data-ttu-id="d85b4-649">藉由從 eq (6) 透過演算法執行每個點，就會取得八個控制點，每個都有 *R*、*G*、*B* 和 *L*、*a*、*B* 值，並使用原始範例資料放入集區中。</span><span class="sxs-lookup"><span data-stu-id="d85b4-649">By running each of the eight points from eq (6) through the algorithm, eight control points are obtained, each with *R*,*G*,*B* and *L*,*a*,*b* values, which are put into the pool with the original sample data.</span></span>

<span data-ttu-id="d85b4-650">若要確保模型一律會產生有效的色彩值，以及整體色彩處理管線的系統完整性和穩定性，您必須對多項式模型的輸出執行最終裁剪。</span><span class="sxs-lookup"><span data-stu-id="d85b4-650">To ensure that the model always produces valid color values and for system integrity and stability down the whole color processing pipeline, you must perform a final clipping to the output of the polynomial model.</span></span> <span data-ttu-id="d85b4-651">CIE 的視覺範圍是由 achromatic 元件所描述 (*Y* 或 *L* ) 以及彩色元件 (*xy* 或 *a'b '*，其與 projective 轉換) 的 XYZ 空間相關。</span><span class="sxs-lookup"><span data-stu-id="d85b4-651">The CIE visual gamut is described by the achromatic component (*Y* or *L* ) and the chromatic component (*xy* or *a'b'*, which are related to the XYZ space by a projective transformation).</span></span> <span data-ttu-id="d85b4-652">在目前的執行中，會使用 *a'b '* chromaticity，因為它與 CIELUV 空間直接相關。</span><span class="sxs-lookup"><span data-stu-id="d85b4-652">In the current implementation, the *a'b'* chromaticity is used because it is directly related to the CIELUV space.</span></span> <span data-ttu-id="d85b4-653">針對任何 *CIELAB* 值，請先將 *L* 剪切至非負數值：</span><span class="sxs-lookup"><span data-stu-id="d85b4-653">For any *CIELAB* value, first clip *L* to a non-negative value:</span></span>

![顯示左至非負數值的剪切。](images/cdmp-formula31.png)

<span data-ttu-id="d85b4-655">若要允許內建高光，請在100（實驗室空間中的 *l* 的「傳統」上限）裁剪 *l* 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-655">To allow extrapolation for specular highlights, *L* is not clipped at 100, the "conventional" upper bound for *L* in Lab space.</span></span>

<span data-ttu-id="d85b4-656">接下來，如果 *L* = 0，則會裁剪 *a* 和 *b* ，使 a *= b =* 0。</span><span class="sxs-lookup"><span data-stu-id="d85b4-656">Next, if *L* = 0, then *a* and *b* are clipped such that a *= b =* 0.</span></span> <span data-ttu-id="d85b4-657">如果是 *L* ？</span><span class="sxs-lookup"><span data-stu-id="d85b4-657">If *L* ?</span></span> <span data-ttu-id="d85b4-658">0，計算</span><span class="sxs-lookup"><span data-stu-id="d85b4-658">0, calculate</span></span>

![如果 L = 0，則會顯示公式。](images/cdmp-formula32.png)

<span data-ttu-id="d85b4-660">這些是 *a'b* 圖中的向量元件，從白色點 (*u？ '*，*v？ '*</span><span class="sxs-lookup"><span data-stu-id="d85b4-660">These are the components of a vector in the *a'b'* diagram from the white point (*u?'*,*v?'*</span></span> <span data-ttu-id="d85b4-661">) 至有問題的色彩。</span><span class="sxs-lookup"><span data-stu-id="d85b4-661">) to the color in question.</span></span> <span data-ttu-id="d85b4-662">將 CIE 光譜 locus 定義為 (*'*，*b '* ) ，由波長參數化之所有點的凸殼？：</span><span class="sxs-lookup"><span data-stu-id="d85b4-662">Define the CIE spectral locus as the convex hull of all the points (*a'*,*b'* ), parameterized by the wavelength ?:</span></span>

![顯示波長的公式。](images/cdmp-formula33.png)

<span data-ttu-id="d85b4-664">其中 ![ 顯示 CIE 色彩比對的函式。](images/cdmp-formula34.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-664">where ![Shows the functions for CIE color-matching.](images/cdmp-formula34.png)</span></span> <span data-ttu-id="d85b4-665">這是兩度觀察者的 CIE 色彩比對函數。</span><span class="sxs-lookup"><span data-stu-id="d85b4-665">are the CIE color-matching functions for the 2-degree observer.</span></span> <span data-ttu-id="d85b4-666">如果向量位於 CIE locus 之外，則會將色彩裁剪為 CIE locus 上的點，也就是 locus 與向量所定義之線條的交集。</span><span class="sxs-lookup"><span data-stu-id="d85b4-666">If the vector lies outside the CIE locus, the color is clipped to the point on the CIE locus that is the intersection of the locus and the line defined by the vector.</span></span> <span data-ttu-id="d85b4-667">請參閱圖 5。</span><span class="sxs-lookup"><span data-stu-id="d85b4-667">See Figure 5.</span></span> <span data-ttu-id="d85b4-668">如果發生裁剪， *a* 和 *b* 值會先減去 *a？ '* 來重建</span><span class="sxs-lookup"><span data-stu-id="d85b4-668">If clipping has occurred, the *a* and *b* value is reconstructed by first subtracting *a?'*</span></span> <span data-ttu-id="d85b4-669">和 *b？* 」</span><span class="sxs-lookup"><span data-stu-id="d85b4-669">and *b?'*</span></span> <span data-ttu-id="d85b4-670">從裁剪 *的 a* 和 *b*，然後乘以 13 *L*。</span><span class="sxs-lookup"><span data-stu-id="d85b4-670">from the clipped *a'* and *b'*, and then multiplying by 13 *L*.</span></span>

![顯示剪切演算法圖形的圖表。](images/cdmp-lcd-dmp-figure5.png)

<span data-ttu-id="d85b4-672">**圖 5** ：裁剪 CIE 視覺範圍外的實驗室值演算法</span><span class="sxs-lookup"><span data-stu-id="d85b4-672">**Figure 5** : Clipping algorithm for Lab values that are outside the CIE visual gamut</span></span>

<span data-ttu-id="d85b4-673">在目前的執行中， *a'b* 」平面中的 CIE 光譜 locus 會以35區段的分段線性曲線表示， (對應到 360 nm 至 700 nm （含）) 的波長。</span><span class="sxs-lookup"><span data-stu-id="d85b4-673">In the current implementation, the CIE spectral locus in the *a'b'* plane is represented by a piecewise linear curve with 35 segments (corresponding to a wavelength from 360 nm to 700 nm inclusive).</span></span> <span data-ttu-id="d85b4-674">藉由排序線段，讓其白色點的 subtended 角度成為遞增（相當於遞減的波長），簡單的二進位搜尋就可以找到與上述向量形成的光線相交的線段。</span><span class="sxs-lookup"><span data-stu-id="d85b4-674">By ordering the line segments so that their subtended angles at the white point are ascending, which is equivalent to descending wavelengths, the line segment that intersects with the ray formed by the above vector can be found by a simple binary search.</span></span>

### <a name="rgb-printer-device-model-baseline"></a><span data-ttu-id="d85b4-675">RGB 印表機裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-675">RGB Printer Device Model Baseline</span></span>

<span data-ttu-id="d85b4-676">RGB 印表機的裝置特性包含了裝置的經驗模型，可針對任何指定的 RGB 值預測裝置獨立的 CIELUV 色彩</span><span class="sxs-lookup"><span data-stu-id="d85b4-676">A device characterization of a RGB printer consists of constructing an empirical model of the device that predicts the device-independent CIELUV color for any given RGB value</span></span>

<span data-ttu-id="d85b4-677">有兩種方式可以建立經驗模型。</span><span class="sxs-lookup"><span data-stu-id="d85b4-677">There are two ways to construct the empirical model.</span></span> <span data-ttu-id="d85b4-678">其中一種方式是使用 RGB 印表機的裝置資料，而另一種方式是流量分析參數資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-678">One way is to use the device data for a RGB printer, and the other is to use analytical parameter data.</span></span> <span data-ttu-id="d85b4-679">第一個方法是使用 RGB 印表機裝置的使用者所提供的測量資料， (LUT) 來建造3-d 查閱資料表。</span><span class="sxs-lookup"><span data-stu-id="d85b4-679">In the first one, measurement data provided by a user for a RGB printer device is used to construct 3-D lookup table (LUT).</span></span> <span data-ttu-id="d85b4-680">度量資料包含一致取樣 RGB 修補程式的 XYZ 值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-680">The measurement data consists of XYZ values for uniformly sampled RGB patches.</span></span> <span data-ttu-id="d85b4-681">每個元件的一般取樣大小為9或17。</span><span class="sxs-lookup"><span data-stu-id="d85b4-681">Typical sampling sizes are 9 or 17 for each component.</span></span> <span data-ttu-id="d85b4-682">每個修補程式都會以 CIEXYZ 空間中的 colorimeter 或 spectrophotometer 來測量。</span><span class="sxs-lookup"><span data-stu-id="d85b4-682">Each patch is measured with a colorimeter or spectrophotometer in CIEXYZ space.</span></span> <span data-ttu-id="d85b4-683">然後，修補程式的 XYZ 值會轉換成 CIELUV 值，形成 3-d LUT。</span><span class="sxs-lookup"><span data-stu-id="d85b4-683">The XYZ value for a patch is then converted into CIELUV value, forming a 3-D LUT.</span></span> <span data-ttu-id="d85b4-684">在裝置模型中，Sakamoto 的 tetrahedral 插補方法會套用至 3-d LUT，以預測給定 RGB 資料的 CIELUV 資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-684">In the device model, the Sakamoto's tetrahedral interpolation method is applied to the 3-D LUT in order to predict the CIELUV data for a given RGB data.</span></span> <span data-ttu-id="d85b4-685"> (將我們的專利 4275413 (Sakamoto et. ) ，美國專利 4511989 (Sakamoto) ，Kang \[ 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-685">(Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="d85b4-686">提及的兩項專利已過期。請 ) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-686">The two patents mentioned have expired.).</span></span> <span data-ttu-id="d85b4-687">第二個方法中傳遞的分析參數資料只是先前建立的 LUT。</span><span class="sxs-lookup"><span data-stu-id="d85b4-687">The analytical parameter data passed in the second method is simply a LUT that was built previously.</span></span> <span data-ttu-id="d85b4-688">一般而言，該 LUT 是使用第一個方法建立的，雖然它可以是手動建立的。</span><span class="sxs-lookup"><span data-stu-id="d85b4-688">Typically, that LUT was built using the first method, although it could be hand-built.</span></span>

<span data-ttu-id="d85b4-689">在目前的色彩管理中，來源對應會定義為從 RGB 空間進入與裝置無關的 CIEXYZ 色彩空間的地圖。</span><span class="sxs-lookup"><span data-stu-id="d85b4-689">In the current color management, the source map is defined as the map that goes from RGB space to a device-independent CIEXYZ color space.</span></span> <span data-ttu-id="d85b4-690">目的地圖定義為從裝置獨立的 CIEXYZ 色彩空間到 RGB 空間的地圖。</span><span class="sxs-lookup"><span data-stu-id="d85b4-690">The destination map is defined as the map that goes from the device-independent CIEXYZ color space to RGB space.</span></span> <span data-ttu-id="d85b4-691">它是來源對應的反向。</span><span class="sxs-lookup"><span data-stu-id="d85b4-691">It is the inverse of the source map.</span></span>

<span data-ttu-id="d85b4-692">經驗模型直接用於來源對應。</span><span class="sxs-lookup"><span data-stu-id="d85b4-692">The empirical model is directly used in the source map.</span></span> <span data-ttu-id="d85b4-693">它會先將指定的 RGB 資料對應至 CIELUV 資料，並轉換成 XYZ 資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-693">It first maps a given RGB data into a CIELUV data, which is converted into XYZ data.</span></span> <span data-ttu-id="d85b4-694">在目的地對應中，與裝置無關的 CIEXYZ 資料會先轉換成 CIELUV 資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-694">In the destination map, device-independent CIEXYZ data is first converted into CIELUV data.</span></span> <span data-ttu-id="d85b4-695">然後，經驗模型和傳統的 Newton-Raphson 方法會用來預測 CIELUV 資料的最佳 RGB 資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-695">Then, the empirical model and the classical Newton-Raphson method are used to predict the best RGB data for the CIELUV data.</span></span> <span data-ttu-id="d85b4-696">從 CieLUV 轉換成 RGB 資料的詳細資料如下所示：</span><span class="sxs-lookup"><span data-stu-id="d85b4-696">The details about conversion from CieLUV to RGB data are as follows:</span></span>

<span data-ttu-id="d85b4-697">從 RGB 產生 3-d LUT 至 CieLUV 之後，會使用 RGB 上的 tetrahedral 插補來建立從 RGB 到 LUV 的對應。</span><span class="sxs-lookup"><span data-stu-id="d85b4-697">After generating a 3-D LUT from RGB to CieLUV, the map from RGB to LUV is built using tetrahedral interpolation on RGB.</span></span> <span data-ttu-id="d85b4-698">此對應會以下列方程式表示：</span><span class="sxs-lookup"><span data-stu-id="d85b4-698">This map is denoted by the following equations:</span></span>

![顯示從 R G B 到 L U V 的地圖方程式。](images/cdmp-image125.png)

<span data-ttu-id="d85b4-700">地圖反轉是針對任何色彩的求解所組成</span><span class="sxs-lookup"><span data-stu-id="d85b4-700">Inversion of the map consists of solving, for any color</span></span> ![顯示 L U V。](images/cdmp-image127.png) <span data-ttu-id="d85b4-702">，下列非線性方程序系統：</span><span class="sxs-lookup"><span data-stu-id="d85b4-702">, the following system of nonlinear equations:</span></span>

![顯示 lolving 任何色彩 L U V 的非線性方程序。](images/cdmp-image129.png)

<span data-ttu-id="d85b4-704">以傳統 Newton-Raphson 方法為基礎的非線性方程序是在新的 CTE 中使用。</span><span class="sxs-lookup"><span data-stu-id="d85b4-704">A nonlinear equation that is based on the classical Newton-Raphson method is used in the new CTE.</span></span> <span data-ttu-id="d85b4-705">初始 <sub>的猜測</sub>或 *先驗* 看到 (R 0、G 0、B 0 ) 是藉由搜尋由預先計算 (RGB、Luv) 配對之統一8x8x8 方格所組成的「種子矩陣」來取得。</span><span class="sxs-lookup"><span data-stu-id="d85b4-705">An initial guess, or *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) is obtained by searching through a "seed matrix" consisting of a uniform 8x8x8 grid of pre-computed (RGB,Luv) pairs.</span></span> <span data-ttu-id="d85b4-706">選擇最接近 L u v 的 RGB 對應 Luv \* \* \* 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-706">The RGB corresponding Luv that is closest to the L\*u\*v\* is chosen.</span></span> <span data-ttu-id="d85b4-707">種子矩陣中的每個點都會對應到資料格的中心，如此一來，反覆運算就不會以 RGB cube 界限的點開始。</span><span class="sxs-lookup"><span data-stu-id="d85b4-707">Each point in the seed matrix corresponds to the center of a cell so that the iterations don't start with a point on the boundary face of the RGB cube.</span></span> <span data-ttu-id="d85b4-708">換句話說，種子的 RGB 是由下列定義：步驟 = 1/8 s <sub>ijk</sub> = (步驟/2 + (i-1) 步驟、步驟/2 + (j-1) 步驟、步驟/2 + (k-1) 步驟) *，在 newton-raphson 的第一個* 步驟中，下一個預估會 ![ 顯示下一次評估的變數。](images/cdmp-image133.png)</span><span class="sxs-lookup"><span data-stu-id="d85b4-708">In other words, the RGB of the seeds is defined by: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At the *i* th step of Newton-Raphson, the next estimate ![Shows the variables for the next estimate.](images/cdmp-image133.png)</span></span> <span data-ttu-id="d85b4-709">是由公式取得：</span><span class="sxs-lookup"><span data-stu-id="d85b4-709">is obtained by the formula:</span></span>

![顯示估計值的公式。](images/cdmp-image135.png)

<span data-ttu-id="d85b4-711">當 CIELUV) 空間中的錯誤 (距離小於 CTE) 中 (0.1 的預先設定容錯層級，或反覆運算數目超過 CTE (中允許的反覆運算次數上限時，會停止反復專案) 10。</span><span class="sxs-lookup"><span data-stu-id="d85b4-711">Iteration stops when the error (distance in the CIELUV space) is less than a pre-set tolerance level (0.1 in the CTE), or when the number of iterations has exceeded the maximum allowed number of iterations (10 in the CTE).</span></span> <span data-ttu-id="d85b4-712">容錯和反覆運算次數的值廣為人知且實證判定為有效。</span><span class="sxs-lookup"><span data-stu-id="d85b4-712">The values for the tolerance and the number of iterations were empirically determined to be effective.</span></span> <span data-ttu-id="d85b4-713">在未來的版本中，容錯值可能會變更。</span><span class="sxs-lookup"><span data-stu-id="d85b4-713">In future versions, the tolerance value may be changed.</span></span>

<span data-ttu-id="d85b4-714">Jacobian 矩陣是使用向前差異來計算，但界限點 (一或多個 R、G、B 是 1) ，而改用反向差異。</span><span class="sxs-lookup"><span data-stu-id="d85b4-714">The Jacobian matrix is calculated using forward difference, except at a boundary point (one or more of the R, G, B is 1) where backward difference is used instead.</span></span> <span data-ttu-id="d85b4-715">線性系統不會計算 Jacobian 矩陣的反向，而是會使用具有完整切換的 Gauss-Jordan 消除來直接解決線性系統。</span><span class="sxs-lookup"><span data-stu-id="d85b4-715">Instead of calculating the inverse of the Jacobian matrix, the linear system is solved directly using Gauss-Jordan elimination with full pivoting.</span></span>

<span data-ttu-id="d85b4-716">在反復專案結束時，仍可能無法進行聚合，因為 Newton-Raphson 是「本機」演算法，也就是說，只有當您從接近真正解決方案的初步猜測開始時，才會順利運作。</span><span class="sxs-lookup"><span data-stu-id="d85b4-716">At the end of the iterations, convergence still might not be achieved because Newton-Raphson is a "local" algorithm, that is, it only works well if you start with an initial guess that is close to the true solution.</span></span> <span data-ttu-id="d85b4-717">如果在 Newton-Raphson 反復專案結束時，尚未達成在預先定義的誤差容錯內的聚合，則會以一組新的種子重新開機反復專案，定義如下。</span><span class="sxs-lookup"><span data-stu-id="d85b4-717">If, at the end of the Newton-Raphson iterations, convergence within the pre-defined error tolerance has not been achieved, the iterations are restarted with a new set of seeds, defined as follows.</span></span>

<span data-ttu-id="d85b4-718">例如，目前為止取得的最佳解決方案是 (r、g、b) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-718">For example, the best solution obtained so far is (r, g, b).</span></span> <span data-ttu-id="d85b4-719">從這個解決方案中，N posteriori 種子是衍生的，其中 N = 4。</span><span class="sxs-lookup"><span data-stu-id="d85b4-719">From this solution, N a posteriori seeds are derived, where N = 4.</span></span> <span data-ttu-id="d85b4-720">在直覺的情況下，解決方案會在與 N 相依的步驟大小中「朝中心」移動。請參閱圖6。</span><span class="sxs-lookup"><span data-stu-id="d85b4-720">Intuitively, the solution is moved "toward the center" in a step size that depends on N. See Figure 6.</span></span>

![顯示解決方案更動方向的圖表。](images/cdmp-image136.png)

<span data-ttu-id="d85b4-722">**圖 6** ：解決方案的更動方向取決於它所在的 octant。</span><span class="sxs-lookup"><span data-stu-id="d85b4-722">**Figure 6** : Perturbation direction of the solution depends on which octant it is in.</span></span>

<span data-ttu-id="d85b4-723">換句話說，如果 r &gt; 0.5，r 通道上的值會減少，否則值會增加。</span><span class="sxs-lookup"><span data-stu-id="d85b4-723">In other words, if r &gt; 0.5, the value on the R channel is decreased, otherwise the value is increased.</span></span> <span data-ttu-id="d85b4-724">G 和 B 通道都有類似的邏輯。</span><span class="sxs-lookup"><span data-stu-id="d85b4-724">There is similar logic for the G and B channels.</span></span> <span data-ttu-id="d85b4-725">精確定義如下：</span><span class="sxs-lookup"><span data-stu-id="d85b4-725">The precise definitions are:</span></span>

<span data-ttu-id="d85b4-726">更動 = 0.5/ (N + 1) </span><span class="sxs-lookup"><span data-stu-id="d85b4-726">PERTURBATION = 0.5/(N+1)</span></span>

<span data-ttu-id="d85b4-727">Dir (r) =-1 如果 r &gt; 0.5; 否則為 + 1。</span><span class="sxs-lookup"><span data-stu-id="d85b4-727">Dir(r) = -1 if r &gt; 0.5; +1 otherwise.</span></span> <span data-ttu-id="d85b4-728">類似于 Dir (g) 和 Dir (b) </span><span class="sxs-lookup"><span data-stu-id="d85b4-728">Similarly for Dir(g) and Dir(b)</span></span>

<span data-ttu-id="d85b4-729">第 j 個 a posteriori 種子，s????, 是 (r + Dir (r) \* j \* 更動、g + dir (g) \* j \* 更動、b + dir (b) \* j \* 更動) </span><span class="sxs-lookup"><span data-stu-id="d85b4-729">The jth a posteriori seed, s ????, is (r + Dir(r) \*j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)</span></span>

<span data-ttu-id="d85b4-730">嘗試第一個????</span><span class="sxs-lookup"><span data-stu-id="d85b4-730">Try the first s ????</span></span> <span data-ttu-id="d85b4-731">如果它在容錯範圍內提供新的解決方案，您可以停止。</span><span class="sxs-lookup"><span data-stu-id="d85b4-731">and if it gives a new solution within error tolerance, you can stop.</span></span> <span data-ttu-id="d85b4-732">否則，請嘗試第二秒????</span><span class="sxs-lookup"><span data-stu-id="d85b4-732">Otherwise, try the second s ????</span></span> <span data-ttu-id="d85b4-733">依此類推，直到第 n 秒????。</span><span class="sxs-lookup"><span data-stu-id="d85b4-733">and so on until the Nth s ????.</span></span>

<span data-ttu-id="d85b4-734">[圖 7] 顯示整個演算法的圖解。</span><span class="sxs-lookup"><span data-stu-id="d85b4-734">The schematics of the whole algorithm is shown in Figure 7.</span></span>

![顯示將裝置模型反轉的流程的圖表。](images/cdmp-image138.png)

<span data-ttu-id="d85b4-736">**圖 7** ：反轉裝置模型的圖解</span><span class="sxs-lookup"><span data-stu-id="d85b4-736">**Figure 7** : Schematics of inverting the device model</span></span>

### <a name="rgb-virtual-device-model-baseline"></a><span data-ttu-id="d85b4-737">RGB 虛擬裝置模型基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-737">RGB Virtual Device Model Baseline</span></span>

<span data-ttu-id="d85b4-738">此裝置模型 (DM) 是簡單的矩陣/語氣複製演算法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-738">This device model(DM) is a simple matrix/tone reproduction algorithm.</span></span> <span data-ttu-id="d85b4-739">矩陣衍生自使用標準色彩科學演算法的白色點和主要複本。</span><span class="sxs-lookup"><span data-stu-id="d85b4-739">The matrix is derived from the white point and primaries using standard color science algorithms.</span></span> <span data-ttu-id="d85b4-740">色調複製品曲線是根據 CurveType 和 ParametricType (的 ICC 描述衍生的測量參數，或視需要) 反轉。</span><span class="sxs-lookup"><span data-stu-id="d85b4-740">The tone reproduction curve is derived from the measurement parameters according to the ICC descriptions of CurveType and ParametricType (or inverted as required).</span></span> <span data-ttu-id="d85b4-741">內部演算法的詳細資料將在額外驗證高動態範圍的問題之後提供。</span><span class="sxs-lookup"><span data-stu-id="d85b4-741">Details of the internal algorithms will be provided after additional validation of high dynamic range issues.</span></span>

<span data-ttu-id="d85b4-742">RGB 虛擬裝置模型是一種理想化的矩陣/語氣複製曲線 RGB，類似于 ICC 三元件矩陣設定檔的設計。</span><span class="sxs-lookup"><span data-stu-id="d85b4-742">The RGB virtual device model is an idealized matrix/tone reproduction curve RGB similar to the ICC three-component matrix-based profile design.</span></span> <span data-ttu-id="d85b4-743">DM 的「虛擬測量」參數包含一個白色點值 (絕對 CIEXYZ) 、RGB 主要值 (絕對 CIEXYZ) ，以及以與 DMP 架構一致之 XML 格式的 ParametricCurveType 和 CurveType 為基礎的音調複製品曲線。</span><span class="sxs-lookup"><span data-stu-id="d85b4-743">The "virtual measurement" parameters of the DM include a white point value (absolute CIEXYZ), RGB primary values (absolute CIEXYZ), and a tone reproduction curve that is based on the ICC ParametricCurveType and CurveType in XML formatting consistent with the DMP schemas.</span></span>

<span data-ttu-id="d85b4-744">下表顯示在 IRGBVirtualDeviceModelBase 中的 ICC parametricCurveType 函式類型編碼和對應支援。</span><span class="sxs-lookup"><span data-stu-id="d85b4-744">ICC parametricCurveType function type encoding and corresponding support in IRGBVirtualDeviceModelBase are shown in the following table.</span></span>



| <span data-ttu-id="d85b4-745">函式類型</span><span class="sxs-lookup"><span data-stu-id="d85b4-745">Function type</span></span>                                         | <span data-ttu-id="d85b4-746">參數</span><span class="sxs-lookup"><span data-stu-id="d85b4-746">Parameters</span></span>                          | <span data-ttu-id="d85b4-747">類型</span><span class="sxs-lookup"><span data-stu-id="d85b4-747">Type</span></span>                                     | <span data-ttu-id="d85b4-748">注意</span><span class="sxs-lookup"><span data-stu-id="d85b4-748">Note</span></span>                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![顯示 ' GammaType ' 函式。](images/cdmp-image154.png)<br/> | <span data-ttu-id="d85b4-750">g</span><span class="sxs-lookup"><span data-stu-id="d85b4-750">g</span></span><br/>              | <span data-ttu-id="d85b4-751">GammaType</span><span class="sxs-lookup"><span data-stu-id="d85b4-751">GammaType</span></span><br/>                 | <span data-ttu-id="d85b4-752">常見的執行</span><span class="sxs-lookup"><span data-stu-id="d85b4-752">Common implementation</span></span><br/>           |
| ![顯示 ' GammaOffsetGainType ' 函式。](images/cdmp-image156.png)<br/> | <span data-ttu-id="d85b4-754">ga b</span><span class="sxs-lookup"><span data-stu-id="d85b4-754">ga b</span></span><br/>           | <span data-ttu-id="d85b4-755">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="d85b4-755">GammaOffsetGainType</span></span><br/>       | <span data-ttu-id="d85b4-756">CIE 122-1966</span><span class="sxs-lookup"><span data-stu-id="d85b4-756">CIE 122-1966</span></span><br/>                    |
| ![顯示 ' GammaOffsetGainOffsetType ' 函式。](images/cdmp-image158.png)<br/> | <span data-ttu-id="d85b4-758">ga b c</span><span class="sxs-lookup"><span data-stu-id="d85b4-758">ga b c</span></span><br/>         | <span data-ttu-id="d85b4-759">GammaOffsetGainOffsetType</span><span class="sxs-lookup"><span data-stu-id="d85b4-759">GammaOffsetGainOffsetType</span></span><br/> | <span data-ttu-id="d85b4-760">IEC 61966-3</span><span class="sxs-lookup"><span data-stu-id="d85b4-760">IEC 61966-3</span></span><br/>                     |
| ![顯示 ' GammaOffsetGainGainType ' 函式。](images/cdmp-image160.png)<br/> | <span data-ttu-id="d85b4-762">ga b c d</span><span class="sxs-lookup"><span data-stu-id="d85b4-762">ga b c d</span></span><br/>       | <span data-ttu-id="d85b4-763">GammaOffsetGainGainType</span><span class="sxs-lookup"><span data-stu-id="d85b4-763">GammaOffsetGainGainType</span></span><br/>   | <span data-ttu-id="d85b4-764">IEC 61966-2。1</span><span class="sxs-lookup"><span data-stu-id="d85b4-764">IEC 61966-2.1</span></span><br/> <span data-ttu-id="d85b4-765"> (sRGB) </span><span class="sxs-lookup"><span data-stu-id="d85b4-765">(sRGB)</span></span><br/> |
| ![顯示 ' g a b c d e f ' 參數的函式。](images/cdmp-image162.png)<br/> | <span data-ttu-id="d85b4-767">ga b c d e f</span><span class="sxs-lookup"><span data-stu-id="d85b4-767">ga b c d e f</span></span><br/>   | <span data-ttu-id="d85b4-768">N/A</span><span class="sxs-lookup"><span data-stu-id="d85b4-768">N/A</span></span><br/>                       | <span data-ttu-id="d85b4-769">在 WCS 中不受支援</span><span class="sxs-lookup"><span data-stu-id="d85b4-769">Not supported in WCS</span></span><br/>            |



 

<span data-ttu-id="d85b4-770">RGB 虛擬裝置的色調曲線會在輸入資料、pDeviceColors 和矩陣相乘之間的 DeviceToColorimetric 中套用。</span><span class="sxs-lookup"><span data-stu-id="d85b4-770">The tone curve for RGB virtual devices is applied in DeviceToColorimetric between the input data, pDeviceColors, and the matrix multiply.</span></span> <span data-ttu-id="d85b4-771">若為 ColorimetricToDevice，則必須使用方法來將色調曲線反轉。</span><span class="sxs-lookup"><span data-stu-id="d85b4-771">For ColorimetricToDevice, a method must be used to invert the tone curve.</span></span> <span data-ttu-id="d85b4-772">在基準執行中，這是由 DeviceToColorimetric 所使用的相同色調曲線中的直接插補來完成。</span><span class="sxs-lookup"><span data-stu-id="d85b4-772">In the baseline implementation, this is done by direct interpolation in the same tone curve used for DeviceToColorimetric.</span></span>

<span data-ttu-id="d85b4-773">曲線應該在設定檔中指定為浮點數中的數位配對。</span><span class="sxs-lookup"><span data-stu-id="d85b4-773">The curves should be specified in the profiles as pairs of numbers in float space.</span></span> <span data-ttu-id="d85b4-774">第一個數位代表 pDeviceColors 中的值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-774">The first number represents values in pDeviceColors.</span></span> <span data-ttu-id="d85b4-775">第二個數字代表音訊曲線的輸出。</span><span class="sxs-lookup"><span data-stu-id="d85b4-775">The second number represents the output of the tone curve.</span></span> <span data-ttu-id="d85b4-776">色調曲線中的所有值都必須介於 minColorantUsed 和 maxColorantUsed 之間。</span><span class="sxs-lookup"><span data-stu-id="d85b4-776">All values in the tone curve must be between minColorantUsed and maxColorantUsed.</span></span> <span data-ttu-id="d85b4-777">色調曲線必須包含至少兩個專案：一個用於 minColorantUsed，一個用於 maxColorantUsed。</span><span class="sxs-lookup"><span data-stu-id="d85b4-777">Tone curves must contain at least two entries: one for minColorantUsed and one for maxColorantUsed.</span></span> <span data-ttu-id="d85b4-778">ToneCurve 中的專案數上限為2048。</span><span class="sxs-lookup"><span data-stu-id="d85b4-778">The maximum number of entries in the ToneCurve is 2048.</span></span> <span data-ttu-id="d85b4-779">一般而言，資料表中的專案越多，就越能更精確地建立曲率的模型。</span><span class="sxs-lookup"><span data-stu-id="d85b4-779">In general, the more entries in the table, the more accurately you can model curvature.</span></span> <span data-ttu-id="d85b4-780">在專案之間執行分段的線性插補。</span><span class="sxs-lookup"><span data-stu-id="d85b4-780">A piecewise linear interpolation is performed between the entries.</span></span>

<span data-ttu-id="d85b4-781">您可以考慮替代的插補方法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-781">You might consider alternative interpolation methods.</span></span> <span data-ttu-id="d85b4-782">如果您知道裝置的基礎行為，則可以使用較高順序曲線更精確地使用範例和模型。</span><span class="sxs-lookup"><span data-stu-id="d85b4-782">If you know something about the underlying behavior of the device, you can use fewer samples and model more accurately with a higher order curve.</span></span> <span data-ttu-id="d85b4-783">但是，如果您使用錯誤的曲線類型，就會很不精確。</span><span class="sxs-lookup"><span data-stu-id="d85b4-783">But if you use the wrong curve type, you will be very inaccurate.</span></span> <span data-ttu-id="d85b4-784">如果沒有詳細資訊，您就不能猜測曲線類型。</span><span class="sxs-lookup"><span data-stu-id="d85b4-784">Without more information, you cannot guess the curve type.</span></span> <span data-ttu-id="d85b4-785">因此，請使用線性插補並提供許多資料點。</span><span class="sxs-lookup"><span data-stu-id="d85b4-785">So, use linear interpolation and provide many data points.</span></span>

### <a name="cmyk-printer-device-model-baseline"></a><span data-ttu-id="d85b4-786">CMYK 印表機裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-786">CMYK Printer Device Model Baseline</span></span>

<span data-ttu-id="d85b4-787">CMYK 印表機的裝置特性包括：建立裝置的經驗模型，以預測任何指定之 CMYK 值的列印色彩。</span><span class="sxs-lookup"><span data-stu-id="d85b4-787">A device characterization of a CMYK printer consists of constructing an empirical model of the device that predicts the printed color for any given CMYK value.</span></span> <span data-ttu-id="d85b4-788">特性也包含此模型的反轉，讓您可以指定要列印的特定色彩之 CMYK 值的處方。</span><span class="sxs-lookup"><span data-stu-id="d85b4-788">The characterization also includes the inversion of this model so that a prescription of the CMYK value to us for a given color to be printed can be given.</span></span> <span data-ttu-id="d85b4-789">這通常是根據 CIEXYZ 或 CIELAB 值來定義。</span><span class="sxs-lookup"><span data-stu-id="d85b4-789">This is typically defined in terms of CIEXYZ or CIELAB value.</span></span>

<span data-ttu-id="d85b4-790">通常會使用包含 CMYK 修補程式的 IT 8.7/3 目標。</span><span class="sxs-lookup"><span data-stu-id="d85b4-790">Typically, an IT8.7/3 target containing CMYK patches is used.</span></span> <span data-ttu-id="d85b4-791">修補程式是以妥善定義的方式來取樣 CMYK 空間，如此一來，就會形成在 C、M、Y 和 K) 中具有非統一間距的矩形格線 (。</span><span class="sxs-lookup"><span data-stu-id="d85b4-791">The patches consist of sampling of the CMYK space in a well-defined manner so that a rectangular grid (with non-uniform spacing in C, M, Y and K) is formed.</span></span> <span data-ttu-id="d85b4-792">接著會使用 colorimeter 或 spectrophotometer 來測量每個修補程式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-792">Each patch is then measured with a colorimeter or spectrophotometer.</span></span> <span data-ttu-id="d85b4-793">CIEXYZ 值中的量值接著會形成一個查閱資料表 (LUT) ，其中會使用 Sakamoto 的插補方法來建立印表機的經驗模型。</span><span class="sxs-lookup"><span data-stu-id="d85b4-793">The measurements in CIEXYZ values then form a lookup table (LUT), from which an empirical model of the printer is built using Sakamoto's interpolation method.</span></span> <span data-ttu-id="d85b4-794">美國專利 4275413 (Sakamoto et ) 、US 專利 4511989 (Sakamoto) 、Kang \[ 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="d85b4-795">提及的兩項專利已過期。</span><span class="sxs-lookup"><span data-stu-id="d85b4-795">The two patents mentioned have expired.</span></span>

<span data-ttu-id="d85b4-796">由 CMYK 印表機基準裝置模型接受之裝置模型設定檔所需的 CMYK 測量範例特定需求如下所示。</span><span class="sxs-lookup"><span data-stu-id="d85b4-796">Specific requirements for the CMYK measurement samples necessary for a device model profile to be accepted as valid by the CMYK printer baseline device model are as follows.</span></span> <span data-ttu-id="d85b4-797"> (範例組最清楚地描述為一組 CMY 範例 cube，每個 cube 都與特定的 K 層級相關聯。 ) </span><span class="sxs-lookup"><span data-stu-id="d85b4-797">(The sample set is most clearly described as a set of CMY sample cubes, each associated with a specific K level.)</span></span>

-   <span data-ttu-id="d85b4-798">至少必須為 K = 0 和 K = 100 層級提供有效的 CMY cube。</span><span class="sxs-lookup"><span data-stu-id="d85b4-798">At minimum, valid CMY cubes must be provided for the K = 0 and K = 100 levels.</span></span>
-   <span data-ttu-id="d85b4-799">中繼 K 層級的間距可能不一致。</span><span class="sxs-lookup"><span data-stu-id="d85b4-799">Intermediate K levels may be non-uniformly spaced.</span></span>
-   <span data-ttu-id="d85b4-800">不含有效 CMY cube 的任何中繼 K 層級都將被忽略。</span><span class="sxs-lookup"><span data-stu-id="d85b4-800">Any intermediate K level without a valid CMY cube will be ignored.</span></span>
-   <span data-ttu-id="d85b4-801">CMY cube 可能會使用非統一的取樣間隔 (方格間距) ，但相同的取樣間隔集合必須用於指定 K 層級之 CMY cube 中的所有 C、M 和 Y 維度。</span><span class="sxs-lookup"><span data-stu-id="d85b4-801">The CMY cubes may use non-uniform sample intervals (grid spacing), but the same set of sample intervals must be used in all of the C,M, and Y dimensions in the CMY cube for a given K level.</span></span>
-   <span data-ttu-id="d85b4-802">每個 K 層級 CMY cube 都可以使用不同的取樣間隔數目和間距。</span><span class="sxs-lookup"><span data-stu-id="d85b4-802">Each K level CMY cube can use a different number and spacing of sample intervals.</span></span>
-   <span data-ttu-id="d85b4-803">所有 CMY cube 都必須包含 CMY cube 的「角落」，也就是 CMY 範例位於 \[ 0、0、0 \] 、 \[ 0、0100 \] 、 \[ 0100、0 \] 、 \[ 100、0、0 \] 、 \[ 0100100 \] 、 \[ 100、0100 \] 、 \[ 100100、0 \] 、 \[ 100100100 \] 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-803">All CMY cubes must contain the "corners" of the CMY cube, that is, CMY samples at \[0,0,0\], \[0,0,100\], \[0,100,0\], \[100,0,0\], \[0,100,100\], \[100,0,100\], \[100,100, 0\], \[100,100,100\].</span></span>
-   <span data-ttu-id="d85b4-804">任何中繼 CMY 格線層級都必須在每個通道中進行完整取樣。</span><span class="sxs-lookup"><span data-stu-id="d85b4-804">Any intermediate CMY grid levels must be fully sampled in each channel.</span></span> <span data-ttu-id="d85b4-805">換句話說，CMY cube 內的每個立體方格交集都必須有一個樣本。</span><span class="sxs-lookup"><span data-stu-id="d85b4-805">In other words, a sample must exist at each 3-D grid intersection within the CMY cube.</span></span>
-   <span data-ttu-id="d85b4-806">針對 K = 0 和 K = 100 CMY cube，2x2x2 「僅限角落」的 cube 是接受為有效的最小值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-806">For the K = 0 and K = 100 CMY cubes, 2x2x2 "corners-only" cubes are the minimum accepted as valid.</span></span>

    <span data-ttu-id="d85b4-807">\[注意：在 K = 0 和 K = 100 層級中，3x3x3 CMY cube 將會處理為2x2x2 「僅限角落」的 cube;中繼範例層級會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d85b4-807">\[NOTE: for K=0 and K=100 levels, a 3x3x3 CMY cube will be processed as a 2x2x2 "corners-only" cube; the intermediate sample level is ignored.</span></span> <span data-ttu-id="d85b4-808">4x4x4 和大型 cube 將會使用所有的格線範例。\]</span><span class="sxs-lookup"><span data-stu-id="d85b4-808">4x4x4 and larger cubes will have all on-grid samples used.\]</span></span>

-   <span data-ttu-id="d85b4-809">針對中繼 K 層級，4x4x4 CMY cube 是接受為有效的最小值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-809">For intermediate K levels, 4x4x4 CMY cubes are the minimum accepted as valid.</span></span>

<span data-ttu-id="d85b4-810">高品質的設定檔將會使用更精細的取樣方格，而不是有效性的最小需求，通常是9x9x9x9 或更高的版本。</span><span class="sxs-lookup"><span data-stu-id="d85b4-810">A high-quality profile will use finer sampling grids than the minimum required for validity, usually 9x9x9x9 or higher.</span></span> <span data-ttu-id="d85b4-811">IT 8.7/3、IT 8.7/4 和 ECI 目標的範例會產生有效的裝置模型設定檔 (DMPs) 用於 CMYK 印表機基準裝置模型。</span><span class="sxs-lookup"><span data-stu-id="d85b4-811">The samples from the IT8.7/3, IT8.7/4, and ECI targets produce valid device model profiles (DMPs)for the CMYK printer baseline device model.</span></span> <span data-ttu-id="d85b4-812">雖然此裝置模型可以略過這些目標中不相關的 (外網格) 範例，但並不保證可以針對其他目標執行此動作，因此建議您從會進入此裝置模型設定檔的度量集合中移除無關的樣本。</span><span class="sxs-lookup"><span data-stu-id="d85b4-812">While this device model is able to ignore the extraneous (off-grid) samples in these targets, it is not guaranteed to be able to do so for other targets, and so, it is recommended that extraneous samples be removed from measurement sets going into profiles for this device model.</span></span>

<span data-ttu-id="d85b4-813">印表機模型的反轉會帶來更多的問題。</span><span class="sxs-lookup"><span data-stu-id="d85b4-813">The inversion of the printer model presents more difficulties.</span></span> <span data-ttu-id="d85b4-814">由於 CIECAM 中有輸入色彩，因此有問題指出此色彩是否在印表機範圍內。</span><span class="sxs-lookup"><span data-stu-id="d85b4-814">Given an input color in CIECAM, there is a question of whether this color is within the printer gamut.</span></span> <span data-ttu-id="d85b4-815">另外還有關于色彩外觀空間中點相片順序的問題。</span><span class="sxs-lookup"><span data-stu-id="d85b4-815">There is also the issue regarding the arrangement of points in the color appearance space.</span></span> <span data-ttu-id="d85b4-816">雖然我們可以將 CMYK 值排列成落在矩形方格上（如同在 IT 8.7/3 目標中所做的），但也不能將產生的印刷色彩視為色彩外觀空間中的色彩。</span><span class="sxs-lookup"><span data-stu-id="d85b4-816">While we can arrange the CMYK values to fall on a rectangular grid, as is done in the IT8.7/3 target, the same cannot be said of the resulting printed colors as they are situated in the color appearance space.</span></span> <span data-ttu-id="d85b4-817">一般情況下，它們會散佈在沒有特定模式的色彩外觀空間中。</span><span class="sxs-lookup"><span data-stu-id="d85b4-817">In general, they are scattered in the color appearance space with no particular pattern.</span></span>

<span data-ttu-id="d85b4-818">散佈點的反轉問題通常有兩種方法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-818">There are generally two approaches to the inversion problem of scattered points.</span></span> <span data-ttu-id="d85b4-819">其中一個方法是使用基本三維實體（例如 tetrahedra）的印表機範圍幾何。</span><span class="sxs-lookup"><span data-stu-id="d85b4-819">One approach is to use a geometric subdivision of the printer gamut using elementary 3-dimensional solids, such as tetrahedra.</span></span> <span data-ttu-id="d85b4-820">色彩外觀空間中的印表機色域可能會從 CMY (K) 空間的對應子格引發，請參閱「無回應 \[ 93 \] ，Kang 97」 \[ \] 。這種方法的優點是計算簡易性。</span><span class="sxs-lookup"><span data-stu-id="d85b4-820">A subdivision of the printer gamut in the color appearance space can be induced from the corresponding subdivision of the CMY(K) space, see Hung\[93\], Kang\[97\].This approach has the advantage of computational simplicity.</span></span> <span data-ttu-id="d85b4-821">在四面體的案例中，只會在插補中使用四個點。</span><span class="sxs-lookup"><span data-stu-id="d85b4-821">In the case of a tetrahedron, only four points are used in an interpolation.</span></span> <span data-ttu-id="d85b4-822">另一方面，結果主要取決於幾個點，這表示測量誤差會對結果產生顯著的影響。</span><span class="sxs-lookup"><span data-stu-id="d85b4-822">On the other hand, the result depends heavily on a few points, which means that a measurement error will have a significant effect on the result.</span></span> <span data-ttu-id="d85b4-823">Interpolant 也可能不會太平滑。</span><span class="sxs-lookup"><span data-stu-id="d85b4-823">The interpolant also tends to be not as smooth.</span></span> <span data-ttu-id="d85b4-824">第二種方法不會假設任何細分，而且是以散佈資料插補的技術為基礎。</span><span class="sxs-lookup"><span data-stu-id="d85b4-824">The second approach does not assume any subdivision, and is based on the technique of scattered data interpolation.</span></span> <span data-ttu-id="d85b4-825">傳統的範例是 Shepard 插補的技巧，或反向加權方法 (參閱 Shepard \[ 68 \]) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-825">A classical example is the technique of Shepard interpolation, or inverse weighted method (See Shepard \[68\]).</span></span> <span data-ttu-id="d85b4-826">在這裡，輸入點周圍有幾個點是以某種方式來選擇，每個都指派權數，通常與距離成正比，而 interpolant 則視為相鄰點的加權平均值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-826">Here, several points surrounding the input point are chosen in some manner, each assigned a weight, usually inversely proportional to the distance, and the interpolant is taken as the weighted average of the neighboring points.</span></span> <span data-ttu-id="d85b4-827">在此方法中，相鄰點的選擇是效能的最重要。</span><span class="sxs-lookup"><span data-stu-id="d85b4-827">In this approach, the choice of neighboring points is paramount to performance.</span></span> <span data-ttu-id="d85b4-828">雖然很少的點可能會導致 interpolant 不准確且不平滑，但太多點會造成高的計算成本，因為權數通常是非線性函式，而計算成本高昂。</span><span class="sxs-lookup"><span data-stu-id="d85b4-828">While too few points can render the interpolant inaccurate and non-smooth, too many points impose a high computational cost, as the weights are typically non-linear functions and costly to compute.</span></span>

<span data-ttu-id="d85b4-829">以上所述的兩種方法都有問題。</span><span class="sxs-lookup"><span data-stu-id="d85b4-829">The two approaches described above both have problems.</span></span> <span data-ttu-id="d85b4-830">細分方法的本質取決於合理的雜訊，而 interpolant 通常不會很流暢。</span><span class="sxs-lookup"><span data-stu-id="d85b4-830">The subdivision approach depends critically on the data being reasonably void of noise, and generally the interpolant is not very smooth.</span></span> <span data-ttu-id="d85b4-831">散佈的資料插補更能容忍資料雜訊，通常會提供更流暢的 interpolant，但其計算成本更高。</span><span class="sxs-lookup"><span data-stu-id="d85b4-831">The scattered data interpolation is more tolerant to data noise, and generally gives a smoother interpolant, but it is computationally more expensive.</span></span>

<span data-ttu-id="d85b4-832">新的 CTE 會採用替代方法。</span><span class="sxs-lookup"><span data-stu-id="d85b4-832">The new CTE takes an alternative approach.</span></span> <span data-ttu-id="d85b4-833">將 CMYK 裝置視為數個 CMY 裝置的集合，其中每個裝置都有特定的黑色 (K) 值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-833">The CMYK device is treated as a collection of several CMY devices, each of which has a specific value of black (K).</span></span> <span data-ttu-id="d85b4-834">使用採用做為參數亮度和色度的選取演算法，即會選擇黑色層級。</span><span class="sxs-lookup"><span data-stu-id="d85b4-834">Using a selection algorithm that takes as parameters lightness and chroma, a level of black is chosen.</span></span> <span data-ttu-id="d85b4-835">CMY 值的取得方式是使用 RGB 印表機演算法在其他地方使用的牛頓方法，將對應的 CMY 反轉為 Luv 資料表。</span><span class="sxs-lookup"><span data-stu-id="d85b4-835">The CMY values are obtained by inversion of the corresponding CMY to Luv table using the Newton methods employed elsewhere by the RGB printer algorithm.</span></span>

<span data-ttu-id="d85b4-836">使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="d85b4-836">Use the following steps.</span></span>

1.  <span data-ttu-id="d85b4-837">列印特性目標，也就是 IT 8.7/3 目標，也就是包含每個定期或不規則間距間隔之 CMYK 空間取樣的目標。</span><span class="sxs-lookup"><span data-stu-id="d85b4-837">Print the characterization target, which is either the IT8.7/3 target, or a target containing sampling of the CMYK space at regularly or irregularly spaced intervals.</span></span>
2.  <span data-ttu-id="d85b4-838">使用 spectrophotometer 測量目標，並將度量轉換為 CIELUV 空間。</span><span class="sxs-lookup"><span data-stu-id="d85b4-838">Measure the target using a spectrophotometer, and convert the measurements to CIELUV space.</span></span>
3.  <span data-ttu-id="d85b4-839">將從 CMYK 到 Luv 的向前地圖進行結構。</span><span class="sxs-lookup"><span data-stu-id="d85b4-839">Construct the forward map from CMYK to Luv.</span></span>
4.  <span data-ttu-id="d85b4-840">使用正向對應，以針對 K 值範圍的 Luv 對應來建立一組 CMY。</span><span class="sxs-lookup"><span data-stu-id="d85b4-840">Use the forward map to construct a set of CMY to Luv maps for a range of K values.</span></span>
5.  <span data-ttu-id="d85b4-841">針對任何輸入 Luv 值，您可以選取上述步驟4中所述的其中一個對應來取得對應的 CMYK 值，並使用牛頓的方法進行反轉，以取得選取的 K 值伴隨的 CMY colorant。</span><span class="sxs-lookup"><span data-stu-id="d85b4-841">For any input Luv value, the corresponding CMYK value is obtained by selecting one of the maps constructed in step 4 above and inverting using Newton's method to obtain a CMY colorant set to accompany the K value selected.</span></span>

<span data-ttu-id="d85b4-842">步驟1和2（標準程式）是由不屬於新 CTE 的程式碼剖析程式所執行。</span><span class="sxs-lookup"><span data-stu-id="d85b4-842">Steps 1 and 2, which are standard procedures, are performed by a profiling program that is not part of the new CTE.</span></span> <span data-ttu-id="d85b4-843">IT 8.7/3 目標包含在 C、M、Y 和 K 各層級的所有 CMYK 值都有相當詳細的取樣。或者，您可以使用 C、M、Y 和 K 通道的統一取樣的自訂目標。</span><span class="sxs-lookup"><span data-stu-id="d85b4-843">The IT8.7/3 target contains a reasonably detailed sampling of all the CMYK values at various levels of C, M, Y, and K. Alternatively, a custom target with uniform sampling of the C, M, Y, and K channels can be used.</span></span> <span data-ttu-id="d85b4-844">列印目標之後，就可以使用 spectrophotometer 或 colorimeter 來測量每個修補程式的 XYZ 值，而且可以使用 CIELUV 模型將 XYZ 值轉換成 Luv 值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-844">After the target is printed, a spectrophotometer or colorimeter can be used to measure the XYZ value of each patch, and the XYZ value can be converted to the Luv value using the CIELUV model.</span></span>

<span data-ttu-id="d85b4-845">步驟3：在 CMYK 空間的矩形方格上套用任何已知的插補技術（例如 tetrahedral 或 multilinear 方法），即可達成將從 CMYK 到 Luv 的向前地圖結構。</span><span class="sxs-lookup"><span data-stu-id="d85b4-845">Step 3, construction of the forward map from CMYK to Luv, can be achieved by applying any known interpolation technique, such as tetrahedral or multilinear method, on the rectangular grid in CMYK space.</span></span> <span data-ttu-id="d85b4-846">在新的 CTE 中，會使用4維度的 tetrahedral 插補。</span><span class="sxs-lookup"><span data-stu-id="d85b4-846">In the new CTE, a 4-dimensional tetrahedral interpolation is used.</span></span> <span data-ttu-id="d85b4-847">因為 CMY 取樣方格在每個層級上通常都不同，所以我們會使用超取樣的技術，如下所述。</span><span class="sxs-lookup"><span data-stu-id="d85b4-847">Because the CMY sampling grids are generally different on each level of K, however, we use a technique of super-sampling, as detailed below.</span></span> <span data-ttu-id="d85b4-848">針對指定的 CMYK 點，將 K 層級會先根據 K 值來決定。</span><span class="sxs-lookup"><span data-stu-id="d85b4-848">For a given CMYK point, the sandwiching K levels are first determined based on the K value.</span></span> <span data-ttu-id="d85b4-849">然後，在每個 k 層級上引進「超級格線」，這是兩個 K 層級上 CMY 格線的聯集。</span><span class="sxs-lookup"><span data-stu-id="d85b4-849">Then introduce a "super-grid" on each K level that is a union of the CMY grids on each of the two K levels.</span></span> <span data-ttu-id="d85b4-850">在每個 K 層級上，任何新引進之格線點的 Luv 值都是由該 K 層級內的3維度 tetrahedral 插補所取得。</span><span class="sxs-lookup"><span data-stu-id="d85b4-850">On each K level, the Luv value of any newly introduced grid point is obtained by a 3-dimensional tetrahedral interpolation within that K level.</span></span> <span data-ttu-id="d85b4-851">最後，會在這個新方格上執行特定 CMYK 點的4維 tetrahedral 插補。</span><span class="sxs-lookup"><span data-stu-id="d85b4-851">Finally, a 4-dimensional tetrahedral interpolation for the specific CMYK point is performed on this new grid.</span></span>

![顯示 supersampling 的圖表。](images/cdmp-image163.png)

<span data-ttu-id="d85b4-853">**圖 8** ： Supersampling</span><span class="sxs-lookup"><span data-stu-id="d85b4-853">**Figure 8** : Supersampling</span></span>

<span data-ttu-id="d85b4-854">步驟4會將一組 CMY 對 Luv 的查閱資料表 (LUTs) 。</span><span class="sxs-lookup"><span data-stu-id="d85b4-854">Step 4 constructs a set of CMY-to-Luv lookup tables (LUTs).</span></span> <span data-ttu-id="d85b4-855">在步驟3中所建立的向前地圖會重複呼叫，以重新取樣 CMYK 空間。</span><span class="sxs-lookup"><span data-stu-id="d85b4-855">The forward map constructed in Step 3 is called repeatedly to resample the CMYK space.</span></span> <span data-ttu-id="d85b4-856">CMYK 色彩空間的取樣是使用 K 的偶數間距以及不同但仍平均間距的 CMY 取樣。</span><span class="sxs-lookup"><span data-stu-id="d85b4-856">The CMYK color space is sampled using an even spacing of K and a different, but still evenly spaced, sampling of CMY.</span></span>

<span data-ttu-id="d85b4-857">步驟5是使用任何輸入 Luv 點的步驟4中所建立的 LUTs 來取得 CMYK 值的程式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-857">Step 5 is a procedure to obtain the CMYK value using the LUTs constructed in Step 4 for any input Luv point.</span></span> <span data-ttu-id="d85b4-858">您可以藉由分析亮度以及所要求 Luv 中的色彩程度，來選擇 K 的適當值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-858">The appropriate value of K is chosen by analyzing the lightness as well as the degree of color in the Luv requested.</span></span> <span data-ttu-id="d85b4-859">選取資料表之後，就會使用牛頓的方法 (從資料表取得 CMY 值，如先前) 的 RGB 印表機裝置型號所述。</span><span class="sxs-lookup"><span data-stu-id="d85b4-859">After the table is selected, the CMY values are obtained from the table by using Newton's method (as documented under the RGB printer device model earlier).</span></span>

<span data-ttu-id="d85b4-860">CIELUV 空間會在印表機模型中使用，而不是 CIEJab，因為裝置型號應該僅以 DMP 提供的色度資料為基礎。</span><span class="sxs-lookup"><span data-stu-id="d85b4-860">CIELUV space is used in the printer model instead of CIEJab because the device model should be based solely on colorimetric data available in the DMP.</span></span> <span data-ttu-id="d85b4-861">DMP 包含每個已測量修補程式的色度資料（包括媒體的白色點），因此可以將 CIEXYZ 資料轉換成 CIELUV 資料。</span><span class="sxs-lookup"><span data-stu-id="d85b4-861">The DMP contains colorimetric data for each measured patch, including the media white point, so it is possible to convert CIEXYZ data into CIELUV data.</span></span> <span data-ttu-id="d85b4-862">但是，無法轉換成 CIECAM02 JCh 或 Jab，因為無法存取 DMP 中的狀況資訊。</span><span class="sxs-lookup"><span data-stu-id="d85b4-862">However, it is not possible to convert to CIECAM02 JCh or Jab, because there is no access to the viewing condition information in the DMP.</span></span>

### <a name="rgb-projector-device-model-baseline"></a><span data-ttu-id="d85b4-863">RGB 投影機裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-863">RGB Projector Device Model Baseline</span></span>

<span data-ttu-id="d85b4-864">注意：許多 RGB 投影機都有一個以上的操作模式。</span><span class="sxs-lookup"><span data-stu-id="d85b4-864">Note: Many RGB projectors have more than one operating mode.</span></span> <span data-ttu-id="d85b4-865">在一種模式中（通常是預設值，而且可能稱為「簡報」），投影機的色彩回應最適合最大亮度。</span><span class="sxs-lookup"><span data-stu-id="d85b4-865">In one mode, which is often the default and might be called something like "presentation," the color response of the projector is optimized for maximum brightness.</span></span> <span data-ttu-id="d85b4-866">不過，在此模式中，投影機無法重現輕量、稍微彩色的色彩，例如淺黃色和一些充實聲。</span><span class="sxs-lookup"><span data-stu-id="d85b4-866">However, in this mode, the projector loses the ability to reproduce light, slightly chromatic colors such as pale yellows and some flesh tones.</span></span> <span data-ttu-id="d85b4-867">在另一個模式中（通常稱為「電影」、「影片」或「sRGB」），投影機最適合用來重現實際影像和自然場景。</span><span class="sxs-lookup"><span data-stu-id="d85b4-867">In another mode, often called "film," "video," or "sRGB," the projector is optimized for reproduction of realistic images and natural scenes.</span></span> <span data-ttu-id="d85b4-868">在此模式中，最大亮度會進行取捨，以改善色彩重現的整體品質。</span><span class="sxs-lookup"><span data-stu-id="d85b4-868">In this mode, maximum brightness is traded off to improve the overall quality of the color reproduction.</span></span> <span data-ttu-id="d85b4-869">若要使用 RGB 投影機取得滿意的色彩複製品，必須將投影機放置在可重現平滑色彩的模式中。</span><span class="sxs-lookup"><span data-stu-id="d85b4-869">To obtain satisfactory color reproduction with RGB projectors, it is necessary to place the projector in a mode where a smooth gamut of colors can be reproduced.</span></span>

![顯示 D L P 裝置模型的圖表。](images/cdmp-image167.png)

<span data-ttu-id="d85b4-871">**圖 9** ： DLP 裝置模型</span><span class="sxs-lookup"><span data-stu-id="d85b4-871">**Figure 9** : DLP device model</span></span>

<span data-ttu-id="d85b4-872">傳入的 RGB 值會傳遞兩個計算路徑。</span><span class="sxs-lookup"><span data-stu-id="d85b4-872">An incoming RGB value passes through two computational pathways.</span></span> <span data-ttu-id="d85b4-873">第一個是矩陣模型，它會產生 XYZ 值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-873">The first is the matrix model, which results in an XYZ value.</span></span> <span data-ttu-id="d85b4-874">這會緊接在從 XYZ 轉換成 Luv 的後面。</span><span class="sxs-lookup"><span data-stu-id="d85b4-874">This is immediately followed by the conversion from XYZ to Luv.</span></span> <span data-ttu-id="d85b4-875">第二個是使用 tetrahedral 插補的非統一 LUT 插補。</span><span class="sxs-lookup"><span data-stu-id="d85b4-875">The second is the non-uniform LUT interpolation using tetrahedral interpolation.</span></span> <span data-ttu-id="d85b4-876">插補的輸出已在 Luv 空間中（依結構）。</span><span class="sxs-lookup"><span data-stu-id="d85b4-876">The output of the interpolation is already in Luv space by construction.</span></span> <span data-ttu-id="d85b4-877">系統會新增這兩個輸出，以取得預測的 Luv 值。</span><span class="sxs-lookup"><span data-stu-id="d85b4-877">The two outputs are added to obtain the predicted Luv value.</span></span> <span data-ttu-id="d85b4-878">這最後會轉換成 XYZ，也就是 DLP 裝置的色度模型預期輸出。</span><span class="sxs-lookup"><span data-stu-id="d85b4-878">This is finally converted to XYZ, which is the expected output of the colorimetric model for the DLP device.</span></span>

<span data-ttu-id="d85b4-879">由於投影機是顯示裝置，因此也支援將模型反轉，也就是從 XYZ 轉換成 RGB。</span><span class="sxs-lookup"><span data-stu-id="d85b4-879">Since projectors are display devices, they also support the inversion of the model, that is, the transform from XYZ to RGB.</span></span> <span data-ttu-id="d85b4-880">由於裝置模型會將 RGB 空間轉換成 XYZ 空間，這兩者都是三維，因此反轉相當於在三個未知的情況下解決三個非線性方程序。</span><span class="sxs-lookup"><span data-stu-id="d85b4-880">Because the device model transforms RGB space to XYZ space, which are both three dimensional, inversion is equivalent to solving three nonlinear equations in three unknowns.</span></span> <span data-ttu-id="d85b4-881">這可以透過標準的方程式求解技術來完成，例如，牛頓 Newton-raphson。</span><span class="sxs-lookup"><span data-stu-id="d85b4-881">This can done by standard equation solving techniques, such as Newton-Raphson.</span></span> <span data-ttu-id="d85b4-882">不過，最好先將 XYZ 轉換成 Luv，然後將 Luv 反轉為 RGB 轉換，因為 Luv 空間比 XYZ 空間更 perceptually 線性。</span><span class="sxs-lookup"><span data-stu-id="d85b4-882">It is preferable, however, to first convert XYZ to Luv, and then invert the Luv To RGB transform, because Luv space is more perceptually linear than XYZ space.</span></span>

### <a name="icc-device-model-baseline"></a><span data-ttu-id="d85b4-883">ICC 裝置型號基準</span><span class="sxs-lookup"><span data-stu-id="d85b4-883">ICC Device Model Baseline</span></span>

<span data-ttu-id="d85b4-884">引用的 ICC 工作流程互通性是藉由建立特殊的 ICC 裝置基準裝置模型設定檔來啟用，此設定檔會儲存設定檔物件，並使用無作業的 XYZ 設定檔建立 ICC 轉換。</span><span class="sxs-lookup"><span data-stu-id="d85b4-884">The CITE ICC workflow interoperability is enabled by creating a special ICC device baseline device model profile that stores the profile object and creates a ICC transform using a no-op XYZ profile.</span></span> <span data-ttu-id="d85b4-885">然後，這項轉換會用來在裝置和 CIEXYZ 色彩之間轉譯。</span><span class="sxs-lookup"><span data-stu-id="d85b4-885">This transform is then used to translate between device and CIEXYZ colors.</span></span>

![顯示 C I T E I C C 工作流程互通性的圖表。](images/cdmp-image168.png)

<span data-ttu-id="d85b4-887">**圖 10** ：引用 ICC 工作流程互通性</span><span class="sxs-lookup"><span data-stu-id="d85b4-887">**Figure 10** : CITE ICC Workflow Interoperability</span></span>

## <a name="related-topics"></a><span data-ttu-id="d85b4-888">相關主題</span><span class="sxs-lookup"><span data-stu-id="d85b4-888">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d85b4-889">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="d85b4-889">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="d85b4-890">Windows 色彩系統架構和演算法</span><span class="sxs-lookup"><span data-stu-id="d85b4-890">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





