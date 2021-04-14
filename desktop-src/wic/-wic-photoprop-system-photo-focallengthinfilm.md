---
description: FocalLengthInFilm 屬性的相片中繼資料原則。
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: FocalLengthInFilm 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469437"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a>FocalLengthInFilm 相片中繼資料原則

[FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ FocalLengthInFilm

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI4

### <a name="input-type"></a>輸入類型

UShort

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                            |
|-------|---------------------------------|
| 1     | /app1/ifd/exif/{ushort = 41989}   |
| 2     | /xmp/exif:focallengthin35mmfilm |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                | 磁片格式 |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                | 磁片格式 |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                |
|-------|-------------------------------------|
| 1     | /ifd/exif/{ushort = 41989}            |
| 2     | /ifd/xmp/exif:focallengthin35mmfilm |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
