---
description: 適用于 [亮度] 屬性的相片中繼資料原則。
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: 系統相片亮度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78549d86d50f9b48359932698b02c827bd454a439476f2dc82627e4aab21d25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882058"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>系統相片亮度相片中繼資料原則

適用于 [ [亮度](../properties/props-system-photo-aperture.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ 亮度

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="input-type"></a>輸入類型

Double

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 ApertureNumerator 和 ApertureDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37379} |
| 2     | /xmp/exif:brightnessvalue     |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort = 37379}      |
| 2     | /ifd/xmp/exif:brightnessvalue |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統相片。亮度](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
