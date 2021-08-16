---
description: DateAcquired 屬性的相片中繼資料原則。
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: DateAcquired 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95b8f68d99476db0832a321de1f61c6f3c4dc6be6f10d679735bd51fc92ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087879"
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

 

 
