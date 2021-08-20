---
description: '[系統狀態] 屬性的相片中繼資料原則。'
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: 系統 GPS。狀態相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99237b9fe14d9adbc97dd5de95158a8aa714caaa4a0a8440d9f3798a2155d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710513"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>系統 GPS。狀態相片中繼資料原則

[ [系統狀態](../properties/props-system-gps-status.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ 狀態

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

偏好以 VT \_ LPWSTR，但 \_ 也接受 vt LPSTR。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policies"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort = 9} |
| 2     | /xmp/exif:gpsstatus      |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                    | 磁片格式 |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                    | 磁片格式 |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                    |
|-------|-------------------------|
| 1     | /ifd/gps/{ushort = 9}     |
| 2     | /ifd/xmp/exif:gpsstatus |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統 GPS。狀態](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
