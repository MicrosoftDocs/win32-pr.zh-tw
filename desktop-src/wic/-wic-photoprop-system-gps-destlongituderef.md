---
description: DestLongitudeRef 屬性的相片中繼資料原則。
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: DestLongitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983852"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>DestLongitudeRef 相片中繼資料原則

[DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS。DestLongitudeRef

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

### <a name="precedence-of-paths-jpeg"></a> (JPEG) 的路徑優先順序

如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：



| 單 | 路徑                          | 磁片格式 | 必要 |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Yes      |
| 2     | /app1/ifd/gps/ \\ {ushort = 21 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>路徑 (TIFF) 的優先順序

如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：



| 單 | 路徑                              | 磁片格式 | 必要 |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Yes      |
| 2     | /ifd/gps/ \\ {ushort = 21 \\ }          | ASCII       | 否       |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
