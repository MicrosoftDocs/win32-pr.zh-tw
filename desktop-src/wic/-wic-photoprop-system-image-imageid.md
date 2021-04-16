---
description: ImageID 屬性的相片中繼資料原則。
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: ImageID 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513508"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>ImageID 相片中繼資料原則

[ImageID](../properties/props-system-image-imageid.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 影像 \_ ImageID

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



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 42016} | ascii       |
| 2     | /xmp/exif:ImageUniqueID       | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 42016} | ascii       |
| 2     | /xmp/exif:ImageUniqueID       | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 42016} |
| 2     | /xmp/exif:ImageUniqueID       |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
|       | /ifd/exif/{ushort = 42016}    | ascii       |
|       | /ifd/xmp/exif:ImageUniqueID | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
|       | /ifd/exif/{ushort = 42016}    | ascii       |
|       | /ifd/xmp/exif:ImageUniqueID | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                        |
|-------|-----------------------------|
|       | /ifd/exif/{ushort = 42016}    |
|       | /ifd/xmp/exif:ImageUniqueID |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ImageID](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
