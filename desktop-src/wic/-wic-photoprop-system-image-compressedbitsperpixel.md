---
description: CompressedBitsPerPixel 屬性的相片中繼資料原則。
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: CompressedBitsPerPixel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988834"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>CompressedBitsPerPixel 相片中繼資料原則

[CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 影像 \_ CompressedBitsPerPixel

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

這個值是從 CompressedBitsPerPixelNumerator 和 CompressedBitsPerPixelDenominator 產生的。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                 | 磁片格式 |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort = 37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
