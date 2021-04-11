---
description: DestBearingRef 屬性的相片中繼資料原則。
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: DestBearingRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193558"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>DestBearingRef 相片中繼資料原則

[DestBearingRef](../properties/props-system-gps-destbearingref.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestBearingRef

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-type"></a>輸入類型

字串。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                        |
|-------|-----------------------------|
| 1     | /app1/ifd/gps/{ushort = 23}   |
| 2     | /xmp/exif:gpsdestbearingref |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 順序 | path                            |
|-------|---------------------------------|
| 1     | /ifd/gps/{ushort = 23}            |
| 2     | /ifd/xmp/exif:gpsdestbearingref |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DestBearingRef](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
