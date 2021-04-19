---
description: CameraManufacturer 屬性的相片中繼資料原則。
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: CameraManufacturer 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971575"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>CameraManufacturer 相片中繼資料原則

[CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ CameraManufacturer

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



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort = 271} | ascii       |
| 2     | /xmp/tiff： Make         | Unicode     |
| 3     | /xmp/tiff： make         | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort = 271} | ascii       |
| 2     | /xmp/tiff： Make         | Unicode     |
| 3     | /xmp/tiff： make         | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort = 271} |
| 2     | /xmp/tiff： Make         |
| 3     | /xmp/tiff： make         |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑               | 磁片格式 |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort = 271}  | ascii       |
| 2     | /ifd/xmp/tiff： Make | Unicode     |
| 3     | /ifd/xmp/tiff： make | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑               | 磁片格式 |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort = 271}  | ascii       |
| 2     | /ifd/xmp/tiff： Make | Unicode     |
| 3     | /ifd/xmp/tiff： make | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑               |
|-------|--------------------|
| 1     | /ifd/{ushort = 271}  |
| 2     | /ifd/xmp/tiff： Make |
| 3     | /ifd/xmp/tiff： make |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
