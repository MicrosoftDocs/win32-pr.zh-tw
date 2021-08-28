---
description: '[系統評分] 屬性的相片中繼資料原則。'
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: System. 評分相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25278ad7d881a0acadc5199fd07227bb650aaae4da2b6342070a64d69fd75240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086981"
---
# <a name="systemrating-photo-metadata-policy"></a>System. 評分相片中繼資料原則

[ [系統評分](../properties/props-system-rating.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 評等

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI4

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

可能是 VT \_ UI1、vt \_ UI2 或 vt \_ UI4。 值的範圍可以從0到99。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto：評等 | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                       | 磁片格式 |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto：評等 | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                       |
|-------|----------------------------|
| 1     | /app1/ifd/{ushort = 18249}   |
| 2     | /xmp/microsoftphoto：評等 |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto：評等 | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                           | 磁片格式 |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto：評等 | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                           |
|-------|--------------------------------|
| 1     | /ifd/{ushort = 18249}            |
| 2     | /ifd/xmp/microsoftphoto：評等 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統評分](../properties/props-system-rating.md)
</dt> </dl>

 

 
