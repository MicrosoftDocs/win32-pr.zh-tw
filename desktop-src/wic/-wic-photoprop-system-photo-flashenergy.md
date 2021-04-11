---
description: FlashEnergy 屬性的相片中繼資料原則。
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: FlashEnergy 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027406"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>FlashEnergy 相片中繼資料原則

[FlashEnergy](../properties/props-system-photo-flashenergy.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ FlashEnergy

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="input-type"></a>輸入類型

Double

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 41483} |
| 2     | /xmp/exif:flashenergy         |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort = 41483}  |
| 2     | /ifd/xmp/exif:flashenergy |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[FlashEnergy](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
