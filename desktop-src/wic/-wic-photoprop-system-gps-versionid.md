---
description: System.servicemodel 屬性的相片中繼資料原則。
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: System.servicemodel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983523"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>System.servicemodel 相片中繼資料原則

System.servicemodel 屬性的相片中繼資料[原則。](../properties/props-system-gps-versionid.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ VersionID

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ 向量 \| VT \_ UI

### <a name="input-type"></a>輸入類型

Buffer

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort = 0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                       |
|-------|----------------------------|
| 1     | /ifd/gps/{ushort = 0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System.servicemodel](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
