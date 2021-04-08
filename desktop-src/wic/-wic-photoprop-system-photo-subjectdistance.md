---
description: SubjectDistance 屬性的相片中繼資料原則。
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: SubjectDistance 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851212"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a>SubjectDistance 相片中繼資料原則

[SubjectDistance](../properties/props-system-photo-subjectdistance.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ SubjectDistance

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

系統會從 SubjectDistanceNumerator 和 SubjectDistanceDenominator 產生此值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37382} |
| 2     | /xmp/exif:subjectdistance     |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort = 37382}      |
| 2     | /ifd/xmp/exif:subjectdistance |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SubjectDistance](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
