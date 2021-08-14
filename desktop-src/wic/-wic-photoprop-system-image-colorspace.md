---
description: ColorSpace 屬性的相片中繼資料原則。
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: ColorSpace 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c7d7c9134a8bd93a12ba6cfb6bd8605e228cb6b745ad4401a94f91a2ba9ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710418"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>ColorSpace 相片中繼資料原則

[ColorSpace](../properties/props-system-image-colorspace.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 影像 \_ ColorSpace

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

是

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
| 1     | /app1/ifd/exif/{ushort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 40961} |
| 2     | /xmp/exif:colorspace          |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort = 40961} |
| 2     | /ifd/xmp/exif:colorspace |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
