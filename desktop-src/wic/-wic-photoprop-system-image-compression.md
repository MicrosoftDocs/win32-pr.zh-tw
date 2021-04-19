---
description: 適用于 [壓縮] 屬性的相片中繼資料原則。
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: 系統映射。壓縮相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992467"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>系統映射。壓縮相片中繼資料原則

適用于 [ [壓縮](../properties/props-system-image-compression.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 影像 \_ 壓縮

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



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort = 259} | ushort      |
| 2     | /xmp/tiff：壓縮  | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort = 259} | ushort      |
| 2     | /xmp/tiff：壓縮  | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort = 259} |
| 2     | /xmp/tiff：壓縮  |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort = 259}         | ushort      |
| 2     | /ifd/xmp/tiff：壓縮 | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort = 259}         | ushort      |
| 2     | /ifd/xmp/tiff：壓縮 | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/{ushort = 259}         |
| 2     | /ifd/xmp/tiff：壓縮 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統映射壓縮](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
