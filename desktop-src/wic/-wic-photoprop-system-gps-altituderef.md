---
description: AltitudeRef 屬性的相片中繼資料原則。
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: AltitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980502"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>AltitudeRef 相片中繼資料原則

[AltitudeRef](../properties/props-system-gps-altituderef.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AltitudeRef

### <a name="description"></a>Description

表示用來做為參考高度的高度。 值為0表示海拔超過海平面。 值為1時，表示低於海平面的高度。

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI1

### <a name="input-type"></a>輸入類型

位元組。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort = 5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort = 5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
