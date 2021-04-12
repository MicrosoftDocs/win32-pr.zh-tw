---
description: DateAcquired 屬性的相片中繼資料原則。
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: DateAcquired 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194778"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>DateAcquired 相片中繼資料原則

[DateAcquired](../properties/props-system-dateacquired.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ DateAcquired

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ FILETIME

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ FILETIME

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="precedence-of-paths-jpeg"></a> (JPEG) 的路徑優先順序

如果檔案是 JPEG 格式，則處理常式會依下列順序搜尋資料：



| 單 | 路徑                             | 磁片格式                        | 必要 |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | XMP 日期格式的 Unicode 字串。 | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>路徑 (TIFF) 的優先順序

如果檔案採用 TIFF 格式，則處理常式會依下列順序搜尋資料：



| 單 | 路徑                                 | 磁片格式                        | 必要 |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | XMP 日期格式的 Unicode 字串。 | Yes      |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System. DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
