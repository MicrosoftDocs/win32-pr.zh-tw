---
description: MaxAperture 屬性的相片中繼資料原則。
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: MaxAperture 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987611"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>MaxAperture 相片中繼資料原則

[MaxAperture](../properties/props-system-photo-maxaperture.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ MaxAperture

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="input-type"></a>輸入類型

Double

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 MaxApertureNumerator 和 MaxApertureDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37381} |
| 2     | /xmp/exif:maxaperturevalue    |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort = 37381}       |
| 2     | /ifd/xmp/exif:maxaperturevalue |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MaxAperture](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
