---
description: PeopleNames 屬性的相片中繼資料原則。
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: PeopleNames 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4118cc8242d6dfe8a91d0bcd2b6039095fdf180037f51205d3541b9aefa2cc0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087047"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>PeopleNames 相片中繼資料原則

[PeopleNames](../properties/props-system-photo-peoplenames.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ PeopleNames

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ 向量 \| VT \_ LPWSTR

### <a name="input-type"></a>輸入類型

StringMulti

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                                           | 磁片格式 |
|-------|----------------------------------------------------------------|-------------|
| 1     | /xmp/ <xmpstruct> MP： RegionInfo/ <xmpbag> MPRI：區域 | ushort      |



 

### <a name="write-paths"></a>寫入路徑

無法使用中繼資料原則來寫入這個屬性。

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                |
|-------|-------------------------------------|
| 1     | /xmp/ <xmpstruct> MP： RegionInfo |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                                               | 磁片格式 |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ifd/xmp/ <xmpstruct> MP： RegionInfo/ <xmpbag> MPRI：區域 | ushort      |



 

### <a name="write-paths"></a>寫入路徑

無法使用中繼資料原則來寫入這個屬性。

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                    |
|-------|-----------------------------------------|
| 1     | /ifd/xmp/ <xmpstruct> MP： RegionInfo |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
