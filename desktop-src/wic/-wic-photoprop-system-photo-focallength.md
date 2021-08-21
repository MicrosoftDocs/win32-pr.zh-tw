---
description: FocalLength 屬性的相片中繼資料原則。
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: FocalLength 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbfb1c0a5a8d88993a42ecc1d29e70f3f3d5911d3c0451cbeeaf0ace040460d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667365"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>FocalLength 相片中繼資料原則

[FocalLength](../properties/props-system-photo-focallength.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ FocalLength

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 FocalLengthNumerator 和 FocalLengthDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37386} |
| 2     | /xmp/exif:focallength         |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort = 37386}  |
| 2     | /ifd/xmp/exif:focallength |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[FocalLength](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
