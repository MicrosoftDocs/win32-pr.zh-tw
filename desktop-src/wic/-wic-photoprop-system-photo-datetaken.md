---
description: DateTaken 屬性的相片中繼資料原則。
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: DateTaken 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691476c704d3fdbc4ff5e01467031f2b41884ccb16be537904484a9d01c8fa18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087074"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>DateTaken 相片中繼資料原則

[DateTaken](../properties/props-system-photo-datetaken.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ DateTaken

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ FILETIME

### <a name="input-type"></a>輸入類型

Datetime

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                  | 磁片格式 |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date 已建立 | Unicode     |
| 3     | /xmp/xmp:CreateDate                   | Unicode     |
| 4     | /app1/ifd/exif/{ushort = 36868}         | ascii       |
| 5     | /app13/irb/8bimiptc/iptc/date 已建立 | Unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                  | 磁片格式 |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date 已建立 | Unicode     |
| 3     | /xmp/xmp:CreateDate                   | Unicode     |
| 4     | /app1/ifd/exif/{ushort = 36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/exif/{ushort = 36867}         |
| 2     | /app1/ifd/exif/{ushort = 37521}         |
| 3     | /app1/ifd/exif/{ushort = 36868}         |
| 4     | /app1/ifd/exif/{ushort = 37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /xmp/xmp:CreateDate                   |
| 7     | /app13/irb/8bimiptc/iptc/date 已建立 |
| 8     | /app13/irb/8bimiptc/iptc/time 已建立 |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                | 磁片格式 |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 36867}            | ascii       |
| 2     | /ifd/iptc/date 已建立              | Unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | Unicode     |
| 4     | /ifd/exif/{ushort = 36868}            | ascii       |
| 5     | /ifd/iptc/date 已建立              | Unicode     |
| 6     | /ifd/irb/8bimiptc/iptc/date 已建立 | Unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                | 磁片格式 |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 36867}            | ascii       |
| 2     | /ifd/iptc/date 已建立              | Unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | Unicode     |
| 4     | /ifd/exif/{ushort = 36868}            | ascii       |
| 5     | /ifd/irb/8bimiptc/iptc/date 已建立 | Unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                |
|-------|-------------------------------------|
| 1     | /ifd/exif/{ushort = 36867}            |
| 2     | /ifd/exif/{ushort = 37521}            |
| 3     | /ifd/exif/{ushort = 36868}            |
| 4     | /ifd/exif/{ushort = 37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /ifd/xmp/xmp:CreateDate             |
| 7     | /ifd/iptc/date 已建立              |
| 8     | /ifd/iptc/time 已建立              |
| 9     | /ifd/irb/8bimiptc/iptc/date 已建立 |
| 10    | /ifd/irb/8bimiptc/iptc/time 已建立 |



 

### <a name="png-policy"></a>PNG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /\[\*\]文字/建立時間 | ascii       |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 2     | /\[\*\]文字/建立時間 | ascii       |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 3     | /\[\*\]文字/建立時間 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
