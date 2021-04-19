---
description: ResolutionUnit 屬性的相片中繼資料原則。
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: ResolutionUnit 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974301"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a>ResolutionUnit 相片中繼資料原則

[ResolutionUnit](../properties/props-system-image-resolutionunit.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 影像 \_ ResolutionUnit

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

是。

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ I2

### <a name="input-type"></a>輸入類型

UShort

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort = 296}   |
| 2     | /xmp/tiff:resolutionunit |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /ifd/{ushort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                         | 磁片格式 |
|-------|------------------------------|-------------|
| 1     | /ifd/{ushort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                         |
|-------|------------------------------|
| 1     | /ifd/{ushort = 296}            |
| 2     | /ifd/xmp/tiff:resolutionunit |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ResolutionUnit](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
