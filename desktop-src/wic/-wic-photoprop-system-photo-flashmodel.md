---
description: FlashModel 屬性的相片中繼資料原則。
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: FlashModel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994379"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>FlashModel 相片中繼資料原則

[FlashModel](../properties/props-system-photo-flashmodel.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ FlashModel

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

如果檔案是 JPEG 格式，則處理常式會在讀取或寫入資料時使用下列路徑。



| 單 | 路徑                           | 磁片格式 | 資料格式 | 必要 |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>路徑 (TIFF) 的優先順序

如果檔案採用 TIFF 格式，則處理常式會在讀取或寫入資料時使用下列優先順序順序。



| 單 | 路徑                               | 磁片格式 | 資料格式 | 必要 |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Yes      |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
