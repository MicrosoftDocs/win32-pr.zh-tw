---
description: SpeedRef 屬性的相片中繼資料原則。
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: SpeedRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985024"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>SpeedRef 相片中繼資料原則

[SpeedRef](../properties/props-system-gps-speedref.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ SpeedRef

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      | 磁碟格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      |         |
|-------|---------------------------|---------|
| 1     | /ifd/gps/{ushort = 12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort = 12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort = 12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
