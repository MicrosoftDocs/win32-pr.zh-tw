---
description: '[System.object] 屬性的相片中繼資料原則。'
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: 系統 GPS：相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194777"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>系統 GPS：相片中繼資料原則

[ [System.object](../properties/props-system-gps-date.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ 日期

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="input-type"></a>輸入類型

字串。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort = 29} |
| 2     | /xmp/exif:GPSTimeStamp    |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                       |
|-------|----------------------------|
| 1     | /ifd/gps/{ushort = 29}       |
| 2     | /ifd/xmp/exif:GPSTimeStamp |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統 GPS。 Date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
