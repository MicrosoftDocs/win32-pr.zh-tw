---
description: DestDistanceRef 屬性的相片中繼資料原則。
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: DestDistanceRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978146"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>DestDistanceRef 相片中繼資料原則

[DestDistanceRef](../properties/props-system-gps-destdistanceref.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ DestDistanceRef

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-type"></a>輸入類型

\_接受 vt LPWSTR 或 vt \_ LPSTR。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort = 25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort = 25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
