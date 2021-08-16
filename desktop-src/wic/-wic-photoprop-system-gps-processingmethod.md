---
description: ProcessingMethod 屬性的相片中繼資料原則。
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: ProcessingMethod 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800515d3a7870fa2dc9b5a6ec8c19178889482fa820f66d7d98e8e3ff09870f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931738"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>ProcessingMethod 相片中繼資料原則

[ProcessingMethod](../properties/props-system-gps-processingmethod.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ProcessingMethod

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/gps/{ushort = 27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                              | 磁片格式 |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /ifd/gps/{ushort = 27}              |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                              | 磁片格式 |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /ifd/gps/{ushort = 27}              |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /ifd/gps/{ushort = 27}              |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
