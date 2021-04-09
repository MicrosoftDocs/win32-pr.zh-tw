---
description: CameraModel 屬性的相片中繼資料原則。
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: CameraModel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851888"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>CameraModel 相片中繼資料原則

[CameraModel](../properties/props-system-photo-cameramodel.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ CameraModel

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
| 1     | /app1/ifd/{ushort = 272} | ascii       |
| 2     | /xmp/tiff：模型        | Unicode     |
| 3     | /xmp/tiff：模型        | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort = 272} | ascii       |
| 2     | /xmp/tiff：模型        | Unicode     |
| 3     | /xmp/tiff：模型        | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort = 272} |
| 2     | /xmp/tiff：模型        |
| 3     | /xmp/tiff：模型        |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                | 磁片格式 |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort = 272}   | ascii       |
| 2     | /ifd/xmp/tiff：模型 | Unicode     |
| 3     | /ifd/xmp/tiff：模型 | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                | 磁片格式 |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort = 272}   | ascii       |
| 2     | /ifd/xmp/tiff：模型 | Unicode     |
| 3     | /ifd/xmp/tiff：模型 | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                |
|-------|---------------------|
| 1     | /ifd/{ushort = 272}   |
| 2     | /ifd/xmp/tiff：模型 |
| 3     | /ifd/xmp/tiff：模型 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
