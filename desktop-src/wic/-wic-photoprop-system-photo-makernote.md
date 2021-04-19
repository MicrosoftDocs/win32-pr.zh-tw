---
description: MakerNote 屬性的相片中繼資料原則。
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: MakerNote 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997140"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a>MakerNote 相片中繼資料原則

[MakerNote](../properties/props-system-photo-makernote.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ MakerNote

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ 向量 \| VTUI1

### <a name="input-type"></a>輸入類型

Buffer

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37500} |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 37500} |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 37500} |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37500} |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 37500} |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort = 37500} |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MakerNote](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
