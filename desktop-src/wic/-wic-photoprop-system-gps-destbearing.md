---
description: DestBearing 屬性的相片中繼資料原則。
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: DestBearing 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598ef1e759f75dfb4851f2f3f435b53db1f875421c3d21446ae3de33f688cefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205509"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>DestBearing 相片中繼資料原則

[DestBearing](../properties/props-system-gps-destbearing.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestBearing

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

您可以藉由寫入 DestBearingNumerator 和 DestBearingDenominator 來寫入這個值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      | 磁碟格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 24} |             |
| 2     | /xmp/exif:gpsdestbearing  |             |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort = 24}         |
| 2     | /ifd/xmp/exif:gpsdestbearing |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DestBearing](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
