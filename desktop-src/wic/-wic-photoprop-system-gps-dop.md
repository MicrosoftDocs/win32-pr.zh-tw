---
description: 適用于 System.object 屬性的相片中繼資料原則。
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: GPS. DOP 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945156"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>GPS. DOP 相片中繼資料原則

適用于 [system.object](../properties/props-system-gps-dop.md) 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DOP

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

Yes

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ R8

### <a name="conflict-resolution-policy"></a>衝突解決原則

您可以藉由寫入 DOPNumerator 和 DOPDenominator 來寫入這個值。 無法直接寫入。 不同架構的值會進行協調。

### <a name="precedence-of-paths-jpeg"></a> (JPEG) 的路徑優先順序

如果檔案是 JPEG 格式，則處理常式會依下列順序讀取、寫入和移除資料：



| 單 | 路徑                          | 磁片格式   | 必要 |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | XMP 有理  | Yes      |
| 2     | /app1/ifd/gps/ \\ {ushort = 11 \\ } | EXIF 有理 | No       |



 

### <a name="precedence-of-paths-tiff"></a>路徑 (TIFF) 的優先順序

如果檔案採用 TIFF 格式，則處理常式會依下列順序讀取、寫入和移除資料：



| 單 | 路徑                     | 磁片格式   | 必要 |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | XMP 有理  | Yes      |
| 2     | /ifd/gps/ \\ {ushort = 11 \\ } | EXIF 有理 | 否       |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[GPS](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
