---
description: DestLongitude 屬性的相片中繼資料原則。
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: DestLongitude 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 917c65dbd580b00cf25603e04050386383967e3a70c1896405346652667ef5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087839"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>DestLongitude 相片中繼資料原則

[DestLongitude](../properties/props-system-gps-destlongitude.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLongitude

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ 向量 \| vt \_ R8

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ 向量 \| vt \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

這個值是從 DestLongitudeNumerator 和 DestLongitudeDenominator 產生的。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                       |
|-------|----------------------------|
| 1     | /app1/ifd/gps/{ushort = 22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                           |
|-------|--------------------------------|
| 1     | /ifd/gps/{ushort = 22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
