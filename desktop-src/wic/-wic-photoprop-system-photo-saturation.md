---
description: '[Photo] 屬性的相片中繼資料原則。'
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: 照相相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be1c5be7a0663d5f57823dcb704b843f56e6076713de3682e4b12d6b533ff48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087011"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>照相相片中繼資料原則

[[Photo] 屬性的](../properties/props-system-photo-saturation.md)相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ 飽和度

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI4

### <a name="input-type"></a>輸入類型

UShort

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41993} | ushort      |
| 2     | /xmp/exif：飽和度          | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41993} | ushort      |
| 2     | /xmp/exif：飽和度          | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 41993} |
| 2     | /xmp/exif：飽和度          |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41993} | ushort      |
| 2     | /ifd/xmp/exif：飽和度 | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41993} | ushort      |
| 2     | /ifd/xmp/exif：飽和度 | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort = 41993} |
| 2     | /ifd/xmp/exif：飽和度 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[照相](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
