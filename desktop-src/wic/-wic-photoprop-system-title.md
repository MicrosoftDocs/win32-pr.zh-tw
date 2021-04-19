---
description: System. Title 屬性的相片中繼資料原則。
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: System. 職稱相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980586"
---
# <a name="systemtitle-photo-metadata-policy"></a>System. 職稱相片中繼資料原則

[System. Title](../properties/props-system-title.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 標題

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ LPWSTR 或 vt \_ LPSTR

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                | 磁片格式    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort = 40091}            | unicode \_ 位元組 |
| 2     | /xmp/ <xmpalt> dc：標題         | Unicode        |
| 3     | /xmp/dc： title                       | Unicode        |
| 4     | /app1/ifd/exif/{ushort = 37510}       | Unicode        |
| 5     | /app1/ifd/{ushort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /xmp/ <xmpalt> dc： description   | Unicode        |
| 8     | /xmp/dc：描述                 | Unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /xmp/ <xmpalt> exif： UserComment | Unicode        |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                | 磁片格式    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort = 40091}            | unicode \_ 位元組 |
| 2     | /xmp/dc： title                       | Unicode        |
| 3     | /xmp/ <xmpalt> dc：標題         | Unicode        |
| 4     | /app1/ifd/exif/{ushort = 37510}       | Unicode        |
| 5     | /xmp/ <xmpalt> exif： UserComment | Unicode        |
| 6     | /app1/ifd/{ushort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /xmp/dc：描述                 | Unicode        |
| 9     | /xmp/ <xmpalt> dc： description   | Unicode        |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort = 40091}            |
| 2     | /xmp/dc： title                       |
| 3     | /app1/ifd/exif/{ushort = 37510}       |
| 4     | /xmp/ <xmpalt> exif： UserComment |
| 5     | /app1/ifd/{ushort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /xmp/dc：描述                 |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                    | 磁片格式    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort = 40091}                     | unicode \_ 位元組 |
| 2     | /ifd/xmp/ <xmpalt> dc：標題         | Unicode        |
| 3     | /ifd/xmp/dc： title                       | Unicode        |
| 4     | /ifd/exif/{ushort = 37510}                | Unicode        |
| 5     | /ifd/{ushort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /ifd/xmp/ <xmpalt> dc： description   | Unicode        |
| 8     | /ifd/xmp/dc：描述                 | Unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /ifd/xmp/ <xmpalt> exif： UserComment | Unicode        |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                    | 磁片格式    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort = 40091}                     | unicode \_ 位元組 |
| 2     | /ifd/xmp/dc： title                       | Unicode        |
| 3     | /ifd/xmp/ <xmpalt> dc：標題         | Unicode        |
| 4     | /ifd/exif/{ushort = 37510}                | Unicode        |
| 5     | /ifd/xmp/ <xmpalt> exif： UserComment | Unicode        |
| 6     | /ifd/{ushort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /ifd/xmp/dc：描述                 | Unicode        |
| 10    | /ifd/xmp/ <xmpalt> dc： description   | Unicode        |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                    |
|-------|-----------------------------------------|
| 1     | /ifd/{ushort = 40091}                     |
| 2     | /ifd/xmp/dc： title                       |
| 3     | /ifd/exif/{ushort = 37510}                |
| 4     | /ifd/xmp/ <xmpalt> exif： UserComment |
| 5     | /ifd/{ushort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /ifd/xmp/dc：描述                 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
