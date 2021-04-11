---
description: ISOSpeed 屬性的相片中繼資料原則。
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: ISOSpeed 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319616"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>ISOSpeed 相片中繼資料原則

[ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ ISOSpeed

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



| 單 | 路徑                                    | 磁片格式 |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 34855}           | ushort      |
| 2     | /xmp/ <xmpseq> exif： ISOSpeedRatings | Unicode     |
| 3     | /xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                    | 磁片格式 |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 34855}           | ushort      |
| 2     | /xmp/ <xmpseq> exif： ISOSpeedRatings | Unicode     |
| 3     | /xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                    |
|-------|-----------------------------------------|
| 1     | /app1/ifd/exif/{ushort = 34855}           |
| 2     | /xmp/ <xmpseq> exif： isospeedratings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                        | 磁片格式 |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 34855}                    | ushort      |
| 2     | /ifd/xmp/ <xmpseq> exif： ISOSpeedRatings | Unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                        | 磁片格式 |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 34855}                    | ushort      |
| 2     | /ifd/xmp/ <xmpseq> exif： ISOSpeedRatings | Unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                        |
|-------|---------------------------------------------|
| 1     | /ifd/exif/{ushort = 34855}                    |
| 2     | /ifd/xmp/ <xmpseq> exif： isospeedratings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
