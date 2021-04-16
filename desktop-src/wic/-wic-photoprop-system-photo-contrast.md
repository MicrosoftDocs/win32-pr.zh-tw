---
description: '[對比] 屬性的相片中繼資料原則。'
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: 系統相片對比相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514169"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>系統相片對比相片中繼資料原則

[ [對比](../properties/props-system-photo-contrast.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ 對比

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
| 1     | /app1/ifd/exif/{ushort = 41992} | ushort      |
| 2     | /xmp/exif：對比            | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 41992} | ushort      |
| 2     | /xmp/exif：對比            | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort = 41992} |
| 2     | /xmp/exif：對比            |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41992} | ushort      |
| 2     | /ifd/xmp/exif：對比   | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort = 41992} | ushort      |
| 2     | /ifd/xmp/exif：對比   | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort = 41992} |
| 2     | /ifd/xmp/exif：對比   |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[對比](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
