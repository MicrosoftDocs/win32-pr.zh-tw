---
description: PhotometricInterpretation 屬性的相片中繼資料原則。
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: PhotometricInterpretation 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5479c747e2a1cc60a1867a7dc5906e5c4710abf9da33b5328980e0188403ecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204682"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a>PhotometricInterpretation 相片中繼資料原則

[PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ PhotometricInterpretation

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI2

### <a name="input-type"></a>輸入類型

UShort

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                | 磁片格式 |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort = 262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                | 磁片格式 |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort = 262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort = 262}              |
| 2     | /xmp/tiff:photometricinterpretation |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                    | 磁片格式 |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort = 262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                    | 磁片格式 |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort = 262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                    |
|-------|-----------------------------------------|
| 1     | /ifd/{ushort = 262}                       |
| 2     | /ifd/xmp/tiff:photometricinterpretation |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
