---
description: ExposureBias 屬性的相片中繼資料原則。
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: ExposureBias 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992060"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a>ExposureBias 相片中繼資料原則

[ExposureBias](../properties/props-system-photo-exposurebias.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ ExposureBias

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 ExposureBiasNumerator 和 ExposureBiasDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37380} |
| 2     | /xmp/exif:exposurebiasvalue   |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                            | 磁片格式 |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                            |
|-------|---------------------------------|
| 1     | /ifd/exif/{ushort = 37380}        |
| 2     | /ifd/xmp/exif:exposurebiasvalue |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ExposureBias](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
