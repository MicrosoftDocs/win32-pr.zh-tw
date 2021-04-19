---
description: ShutterSpeed 屬性的相片中繼資料原則。
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: ShutterSpeed 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980447"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>ShutterSpeed 相片中繼資料原則

[ShutterSpeed](../properties/props-system-photo-shutterspeed.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ ShutterSpeed

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 ShutterSpeedNumerator 和 ShutterSpeedDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37377} |
| 2     | /xmp/exif:shutterspeedvalue   |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                            |
|-------|---------------------------------|
| 1     | /ifd/exif/{ushort = 37377}        |
| 2     | /ifd/xmp/exif:shutterspeedvalue |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ShutterSpeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
