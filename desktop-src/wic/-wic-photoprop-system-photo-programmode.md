---
description: ProgramMode 屬性的相片中繼資料原則。
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: ProgramMode 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260bf4ae5ca26fa26848765a76f5fdbc36eef48e2806909f46e5ab256f5acd7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032498"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>ProgramMode 相片中繼資料原則

[ProgramMode](../properties/props-system-photo-programmode.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ ProgramMode

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



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | Unicode     |
| 3     | /xmp/exif:ProgramMode         | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | Unicode     |
| 3     | /xmp/exif:ProgramMode         | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 34850} |
| 2     | /xmp/exif:exposureprogram     |
| 3     | /xmp/exif:programmode         |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | Unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | Unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort = 34850}      |
| 2     | /ifd/xmp/exif:exposureprogram |
| 3     | /ifd/xmp/exif:programmode     |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
