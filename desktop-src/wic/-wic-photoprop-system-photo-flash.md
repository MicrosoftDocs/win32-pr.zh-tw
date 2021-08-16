---
description: '[攝影] 屬性的相片中繼資料原則。'
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: '[攝影相片中繼資料] 原則'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba32a7b4dfcde564f6b0c0c9e175aa56786e1324080264c7c928398fe97e6a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811728"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>[攝影相片中繼資料] 原則

[[攝影] 屬性的](../properties/props-system-photo-exposuretime.md)相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ Flash

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

\_如果來源架構) 為) ，則 vt UI1 (（ \_ 如果來源架構為 UI2，則為 vt (）

\\lang1036

### <a name="input-type"></a>輸入類型

VT \_ UI1、VTUI2、VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37385}    | ushort      |
| 2     | /xmp/ <xmpstruct> exif： Flash |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                             | 磁片格式 |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37385}    | ushort      |
| 2     | /xmp/ <xmpstruct> exif： Flash |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37385}    |
| 2     | /xmp/ <xmpstruct> exif： flash |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                 | 磁片格式 |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37385}             | ushort      |
| 2     | /ifd/xmp/ <xmpstruct> exif： Flash |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                 | 磁片格式 |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37385}             | ushort      |
| 2     | /ifd/xmp/ <xmpstruct> exif： Flash |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort = 37385}             |
| 2     | /ifd/xmp/ <xmpstruct> exif： flash |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[： Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
