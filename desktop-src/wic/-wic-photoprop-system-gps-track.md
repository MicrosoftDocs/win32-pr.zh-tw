---
description: 適用于 [追蹤] 屬性的相片中繼資料原則。
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: GPS：追蹤相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89aee05d0c55e78fe4e55d7eacd8a8d0992fcb8d9f56312164c652cbc0bd81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205529"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>GPS：追蹤相片中繼資料原則

適用于 [ [追蹤](../properties/props-system-gps-track.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ 軌

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

這個值是從 TrackNumerator 和 TrackDenominator 產生的。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort = 15} |
| 2     | /xmp/exif:gpstrack        |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                   |
|-------|------------------------|
| 1     | /ifd/gps/{ushort = 15}   |
| 2     | /ifd/xmp/exif:gpstrack |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[GPS. 追蹤](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
