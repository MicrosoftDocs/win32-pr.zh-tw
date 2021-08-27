---
description: '[System. Comment] 屬性的相片中繼資料原則。'
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: System. 批註相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa1a62fd5afa131a714c365ed2fda2c307bc955
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883909"
---
# <a name="systemcomment-photo-metadata-policy"></a>System. 批註相片中繼資料原則

[ [System. Comment](../properties/props-system-comment.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 批註

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

否

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ LPWSTR 或 vt \_ LPSTR

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                | 磁片格式    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort = 40092}            | unicode \_ 位元組 |
| 2     | /app1/ifd/{ushort = 37510}            | Unicode        |
| 3     | /xmp/ &lt; xmpalt &gt; Exif： UserComment | Unicode        |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort = 40092} | unicode \_ 位元組 |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                          |
|-------|-------------------------------|
| 1     | /app1/ifd/{ushort = 40092}      |
| 2     | /app1/ifd/exif/{ushort = 37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                    | 磁片格式    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort = 40092}                     | unicode \_ 位元組 |
| 2     | /ifd/{ushort = 37510}                     | Unicode        |
| 3     | /ifd/xmp/ &lt; xmpalt &gt; Exif： UserComment | Unicode        |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                | 磁片格式    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort = 40092} | unicode \_ 位元組 |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                      |
|-------|---------------------------|
| 1     | /ifd/{ushort = 40092}       |
| 2     | /ifd/{ushort = 37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
