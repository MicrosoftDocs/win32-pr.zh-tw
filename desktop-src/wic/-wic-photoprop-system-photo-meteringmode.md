---
description: MeteringMode 屬性的相片中繼資料原則。
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: MeteringMode 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975404"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>MeteringMode 相片中繼資料原則

[MeteringMode](../properties/props-system-photo-meteringmode.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ MeteringMode

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI2

### <a name="input-type"></a>輸入類型

UShort

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                       |
|-------|----------------------------|
| 1     | /ifd/exif/{ushort = 37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
