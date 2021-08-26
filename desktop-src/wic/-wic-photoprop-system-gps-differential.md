---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: 系統 GPS. 差異相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728df47fd8e6e9748b7208b79444ba8fa257fa49c92587df199441de941f4fdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931798"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>系統 GPS. 差異相片中繼資料原則

適用于 [system.object](../properties/props-system-gps-differential.md) 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ 差異

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI2

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ UI1、vt \_ UI2 和 vt \_ UI4 全都接受。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                      | 磁片格式 |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort = 30} |
| 2     | /xmp/exif:gpsdifferential |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                          | 磁片格式 |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort = 30}          |
| 2     | /ifd/xmp/exif:gpsdifferential |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統 GPS](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
