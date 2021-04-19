---
description: System.servicemodel 屬性的相片中繼資料原則。
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: System.servicemodel. 速度相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988344"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>System.servicemodel. 速度相片中繼資料原則

System.servicemodel 屬性的相片中繼資料[原則。](../properties/props-system-gps-speed.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ 速度

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

這個值是從 SpeedNumerator 和 SpeedDenominator 產生的。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort = 13} |
| 2     | /xmp/exif:gpsspeed        |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                   |
|-------|------------------------|
| 1     | /ifd/gps/{ushort = 13}   |
| 2     | /ifd/xmp/exif:gpsspeed |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[GPS. 速度](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
