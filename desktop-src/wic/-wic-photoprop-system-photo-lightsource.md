---
description: LightSource 屬性的相片中繼資料原則。
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: LightSource 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513952"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>LightSource 相片中繼資料原則

[LightSource](../properties/props-system-photo-lightsource.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ LightSource

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI4

### <a name="input-type"></a>輸入類型

UShort

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37384} | ushort      |
| 2     | /xmp/exif:LightSource         | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37384} | ushort      |
| 2     | /xmp/exif:LightSource         | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37384} |
| 2     | /xmp/exif:lightsource         |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort = 37384}  |
| 2     | /ifd/xmp/exif:lightsource |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
