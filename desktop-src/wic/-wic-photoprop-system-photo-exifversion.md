---
description: EXIFVersion 屬性的相片中繼資料原則。
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: EXIFVersion 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eee0fdac7ba8e86321d4a055cb6c37c4e9c7bad3f5bcfced548cc2485b3347c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882028"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>EXIFVersion 相片中繼資料原則

[EXIFVersion](../properties/props-system-photo-exifversion.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ EXIFVersion

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

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort = 36864} | exif \_ 版本 |
| 2     | /xmp/exif:ExifVersion         | Unicode       |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort = 36864} | exif \_ 版本 |
| 2     | /xmp/exif:ExifVersion         | Unicode       |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort = 36864}  | exif \_ 版本 |
| 2     | /ifd/xmp/exif:ExifVersion | Unicode       |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort = 36864}  | exif \_ 版本 |
| 2     | /ifd/xmp/exif:ExifVersion | Unicode       |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort = 36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
