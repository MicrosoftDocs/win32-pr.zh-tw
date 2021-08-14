---
description: AreaInformation 屬性的相片中繼資料原則。
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: AreaInformation 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4eee2cf4234902049241c833d1077814f5daf88187323c43bc1cb00f6f44aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205519"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>AreaInformation 相片中繼資料原則

[AreaInformation](../properties/props-system-gps-areainformation.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AreaInformation

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



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort = 28}    |
| 2     | /xmp/exif:GPSAreaInformation |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort = 28}             |
| 2     | /ifd/xmp/exif:GPSAreaInformation |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AreaInformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
