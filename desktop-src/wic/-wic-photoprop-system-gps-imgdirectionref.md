---
description: ImgDirectionRef 屬性的相片中繼資料原則。
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: ImgDirectionRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e735f91133d4ec473537f063e30d2d48f801a99f8f6bc80fa228b98a9bd95437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667895"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>ImgDirectionRef 相片中繼資料原則

[ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS。ImgDirectionRef

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-type"></a>輸入類型

偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort = 16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort = 16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
