---
title: HorizontalResolution 相片中繼資料原則
description: HorizontalResolution 屬性的相片中繼資料原則。
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade406e644524fea84ef6baf957aed661d2adf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693252"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>HorizontalResolution 相片中繼資料原則

[HorizontalResolution](../properties/props-system-image-horizontalresolution.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 影像 \_ HorizontalResolution

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

是。

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

這個值是由系統產生，無法直接寫入。 不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                   | 磁片格式 |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort = 282} |             |
| 2     | /xmp/tiff:XResolution  |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                        | 磁碟格式 |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort = 282} |             |
| 2     | /xmp/tiff:xresolution       |             |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 282}    |             |
| 2     | /ifd/xmp/tiff:XResolution |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      | 磁碟格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 282}    |             |
| 2     | /ifd/xmp/tiff:xresolution |             |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HorizontalResolution](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
