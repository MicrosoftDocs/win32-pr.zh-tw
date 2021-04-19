---
description: DestLatitude 屬性的相片中繼資料原則。
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: DestLatitude 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994515"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>DestLatitude 相片中繼資料原則

[DestLatitude](../properties/props-system-gps-destlatitude.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLatitude

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ 向量 \| vt \_ R8

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ 向量 \| vt \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

這個值是從 DestLatitudeNumerator 和 DestLatitudeDenominator 產生的。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort = 20} |
| 2     | /xmp/exif:gpsdestlatitude |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort = 20}          |
| 2     | /ifd/xmp/exif:gpsdestlatitude |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DestLatitude](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
