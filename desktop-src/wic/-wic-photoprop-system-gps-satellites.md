---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: 系統 GPS. 衛星相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65bdc244324df513b5029c682e9c2cb355da58f2c95d13910fe093ce2521c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964837"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>系統 GPS. 衛星相片中繼資料原則

適用于 [system.object](../properties/props-system-gps-satellites.md) 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ 衛星

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

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort = 8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                        | 磁片格式 |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                        |
|-------|-----------------------------|
| 1     | /ifd/gps/{ushort = 8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統 GPS](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
