---
title: WCS 校正架構
description: 本主題說明可展開 WCS 色彩裝置模型設定檔的 WCS 校正架構。
ms.assetid: 99f3e9e3-15b7-4bca-87cc-a3bf3b6d0112
keywords:
- Windows Color System (WCS) ，校正
- WCS (Windows 色彩系統) ，校正
- 影像色彩管理，校正
- 色彩管理，校正
- 色彩，校正
- 架構，校正
- WCS 校正
- 校準
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e859ab9d2b47355db063961004f17a8cc1537694
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106985997"
---
# <a name="wcs-calibration-schema"></a>WCS 校正架構

本主題說明可展開 [wcs 色彩裝置模型設定檔](wcs-color-device-model-profile-schema-and-algorithms.md)的 wcs 校正架構。

## <a name="the-wcs-calibration-schema"></a>WCS 校正架構

下列架構定義可用來指定支援 [WCS 色彩裝置模型設定檔](wcs-color-device-model-profile-schema-and-algorithms.md) 校正的新 Windows 7 定義。


```C++
<?xml version="1.0" encoding="UTF-8"?>
<!--
  Copyright (C) Microsoft. All rights reserved. The Windows Color System
  color profile schemas may be used according to the terms of the license agreement
  available at https://www.microsoft.com/whdc/device/display/color/wcs_license.mspx.
  -->
<xs:schema
  xmlns:cal="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model Calibration profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="AdapterGammaConfiguration">
    <xs:choice>
      <xs:element name="ParameterizedCurves" type="wcs:ParameterizedCurvesType"/>
      <xs:element name="HDRToneResponseCurves" type="wcs:HDRToneResponseCurvesType"/>
    </xs:choice>
  </xs:complexType>

  <xs:complexType name="Calibration">
    <xs:sequence>
      <xs:element name="AdapterGammaConfiguration" type="cal:AdapterGammaConfiguration" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>

</xs:schema>
```



為了與 Windows Vista 相容，包含校正標記的設定檔應該包含屬性 `mc:Ignoreable="cdm_calibration"` 。

 

 




