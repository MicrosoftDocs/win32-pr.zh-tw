---
description: DigitalZoom 屬性的相片中繼資料原則。
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: DigitalZoom 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19dfaf2838c8f321b1406d951fcc335076bcdfc00e3a17de0954f1a62022570e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205374"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>DigitalZoom 相片中繼資料原則

[DigitalZoom](../properties/props-system-photo-digitalzoom.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ DigitalZoom

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 DigitalZoomNumerator 和 DigitalZoomDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 41988} |
| 2     | /xmp/exif:digitalzoomratio    |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort = 41988}       |
| 2     | /ifd/xmp/exif:digitalzoomratio |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DigitalZoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
