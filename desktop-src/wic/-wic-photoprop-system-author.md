---
description: System. Author 屬性的相片中繼資料原則。
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: System. 作者相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b898f450fe1d370f94a9be2922eb650db47ac8c2e414c27d9eede23f0dada276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088000"
---
# <a name="systemauthor-photo-metadata-policy"></a>System. 作者相片中繼資料原則

[System. Author](../properties/props-system-author.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 作者

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ 向量 \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

偏好以 VT \_ 向量 \| VT \_ LPWSTR，但 \_ 也接受 vt LPWSTR。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                             | 磁片格式    |
|-------|----------------------------------|----------------|
| 1     | /app1/ifd/{ushort = 315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /xmp/ <xmpseq> dc： creator    | Unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /app1/ifd/{ushort = 40093}         | unicode \_ 位元組 |
| 6     | /xmp/tiff：演出者                 | Unicode        |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                             | 磁片格式    |
|-------|----------------------------------|----------------|
| 1     | /xmp/ <xmpseq> dc： creator    | Unicode        |
| 2     | /xmp/tiff：演出者                 | Unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /app1/ifd/{ushort = 315}           | ascii          |
| 5     | /app1/ifd/{ushort = 40093}         | unicode \_ 位元組 |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                             |
|-------|----------------------------------|
| 1     | /xmp/dc： creator                  |
| 2     | /xmp/tiff：演出者                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /app1/ifd/{ushort = 315}           |
| 5     | /app1/ifd/{ushort = 40093}         |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                              | 磁片格式    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/{ushort = 315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /ifd/xmp/ <xmpseq> dc： creator | Unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /ifd/{ushort = 40093}               | unicode \_ 位元組 |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /ifd/xmp/tiff：演出者              | Unicode        |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                              | 磁片格式    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ <xmpseq> dc： creator | Unicode        |
| 2     | /ifd/xmp/tiff：演出者              | Unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /ifd/{ushort = 315}                 | ascii \_ 向量  |
| 5     | /ifd/{ushort = 40093}               | unicode \_ 位元組 |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                           |
|-------|--------------------------------|
| 1     | /ifd/xmp/dc： creator            |
| 2     | /ifd/xmp/tiff：演出者           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /ifd/{ushort = 315}              |
| 6     | /ifd/{ushort = 40093}            |



 

### <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
