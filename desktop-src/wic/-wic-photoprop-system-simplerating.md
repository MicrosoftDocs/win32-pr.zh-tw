---
description: SimpleRating 屬性的相片中繼資料原則。
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: SimpleRating 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c65c9e49d7e905a4cefe890b6c5aab257250baa41171470666ba38b3fb5c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709962"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>SimpleRating 相片中繼資料原則

[SimpleRating](../properties/props-system-simplerating.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ SimpleRating

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

否

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ UI4

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

可能是 VT \_ UI1、vt \_ UI2 或 vt \_ UI4。 整數值的範圍可以從0到5。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort = 18246} | ushort      |
| 2     | /xmp/xmp：評等          | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式 |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort = 18246} | ushort      |
| 2     | /xmp/xmp：評等          | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort = 18246} |
| 2     | /xmp/xmp：評等          |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                | 磁片格式 |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort = 18246} | ushort      |
| 2     | /ifd/xmp/xmp：評等 | Unicode     |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                | 磁片格式 |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort = 18246} | ushort      |
| 2     | /ifd/xmp/xmp：評等 | Unicode     |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                |
|-------|---------------------|
| 1     | /ifd/{ushort = 18246} |
| 2     | /ifd/xmp/xmp：評等 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System. SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
