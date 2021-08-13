---
description: VerticalResolution 屬性的相片中繼資料原則。
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: VerticalResolution 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9962a00be34d227756d295e992174d6e80b6d058fc32af29ad9cde58a04ed07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710281"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>VerticalResolution 相片中繼資料原則

[VerticalResolution](../properties/props-system-image-verticalresolution.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 影像 \_ VerticalResolution

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
| 1     | /app1/ifd/{ushort = 283} |             |
| 2     | /xmp/tiff:YResolution  |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                        |
|-------|-----------------------------|
| 1     | /app1/ifd/exif/{ushort = 283} |
| 2     | /xmp/tiff:yresolution       |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort = 283}    |             |
| 2     | /ifd/xmp/tiff:YResolution |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort = 283}    |
| 2     | /ifd/xmp/tiff:yresolution |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
