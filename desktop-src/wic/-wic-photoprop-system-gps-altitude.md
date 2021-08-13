---
description: 適用于 [海拔] 屬性的相片中繼資料原則。
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: 系統 GPS. 高度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a9209bfb0bbc1a4c6f95ce4a995d32d3f532c293dd2295c335eea61c22df89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441998"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>系統 GPS. 高度相片中繼資料原則

適用于 [ [海拔](../properties/props-system-gps-altitude.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ 高度

### <a name="description"></a>描述

高度會表示為計量中參考的絕對值。

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

是

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

您可以藉由寫入 system.string 和 system.servicemodel，來寫入這個值的值。 無法直接寫入。 下表中的寫入路徑指出值在產生時可儲存的位置，而不是直接寫入時。 當讀取此值時，會協調來自不同架構的值。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort = 6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |     |
|-------|---------------------------|-----|
| 1     | /ifd/gps/{ushort = 6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[GPS](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
