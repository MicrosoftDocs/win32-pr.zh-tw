---
description: RelatedSoundFile 屬性的相片中繼資料原則。
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: RelatedSoundFile 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944859"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>RelatedSoundFile 相片中繼資料原則

[RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ RelatedSoundFile

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

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 40964} |
| 2     | /xmp/exif:RelatedSoundFile    |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort = 40964}       |
| 2     | /ifd/xmp/exif:RelatedSoundFile |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
