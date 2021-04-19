---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: '[攝影] 相片中繼資料原則'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980638"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>[攝影] 相片中繼資料原則

適用于 [system.object](../properties/props-system-photo-aperture.md) 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ 口徑

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 ApertureNumerator 和 ApertureDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37378} |
| 2     | /xmp/exif:aperturevalue       |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                        |
|-------|-----------------------------|
| 1     | /ifd/exif/{ushort = 37378}    |
| 2     | /ifd/xmp/exif:aperturevalue |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System.servicemodel](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
