---
description: '[System.object] 屬性的相片中繼資料原則。'
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: System. Subject 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9321e866c34027df3e932f84d532162def959cbaf365bb4020c19647d547adea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881968"
---
# <a name="systemsubject-photo-metadata-policy"></a>System. Subject 相片中繼資料原則

[ [System.object](../properties/props-system-subject.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 主旨

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

VT \_ LPWSTR 或 vt \_ LPWSTR

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                     | 磁片格式    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort = 40095} | unicode \_ 位元組 |
| 2     | /app1/ifd/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                     | 磁片格式    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort = 40095} | unicode \_ 位元組 |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort = 40095} |
| 2     | /app1/ifd/{ushort = 270}   |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                | 磁片格式    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort = 40095} | unicode \_ 位元組 |
| 2     | /ifd/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                | 磁片格式    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort = 40095} | unicode \_ 位元組 |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                |
|-------|---------------------|
| 1     | /ifd/{ushort = 40095} |
| 2     | /ifd/{ushort = 270}   |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System. Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
