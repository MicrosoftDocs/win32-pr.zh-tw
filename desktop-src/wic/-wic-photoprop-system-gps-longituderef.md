---
description: LongitudeRef 屬性的相片中繼資料原則。
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: LongitudeRef 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00908f0c76305c745e1146677f32bee7b9724c08510f273c1627ed56e139d02b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931728"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>LongitudeRef 相片中繼資料原則

[LongitudeRef](../properties/props-system-gps-longituderef.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ LongitudeRef

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

### <a name="precedence-of-paths-jpeg"></a> (JPEG) 的路徑優先順序

如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：



| 單 | 路徑                         | 磁片格式 | 必要 |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLongitudeRef    | Unicode     | Yes      |
| 2     | /app1/ifd/gps/ \\ {ushort = 3 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>路徑 (TIFF) 的優先順序

如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：



| 單 | 路徑                          | 磁片格式 | 必要 |
|-------|-------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLongitudeRef | Unicode     | Yes      |
| 2     | /ifd/gps/ \\ {ushort = 3 \\ }       | ASCII       | 否       |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[LongitudeRef](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
