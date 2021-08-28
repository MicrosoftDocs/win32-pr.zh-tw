---
description: '[System.object] 屬性的相片中繼資料原則。'
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: System. 關鍵字相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa5387bfb8cca7fffe83f7615a979d8e23ae890
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886647"
---
# <a name="systemkeywords-photo-metadata-policy"></a>System. 關鍵字相片中繼資料原則

[ [System.object](../properties/props-system-keywords.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 關鍵字

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

否

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ 向量 \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

\_ \| 慣用的 vt 向量 vt \_ LPWSTR 是慣用的。 \_也接受包含分號分隔字串的 VT LPWSTR。

### <a name="conflict-resolution-policy"></a>衝突解決原則

會合並來自不同架構的值。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                              | 磁片格式    |
|-------|-----------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc： subject     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /app1/ifd/{ushort = 18247}          | unicode \_ 位元組 |
| 4     | /app1/ifd/{ushort = 40094}          | unicode \_ 位元組 |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                              | 磁片格式    |
|-------|---------------------------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc： subject                     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /app1/ifd/{ushort = 18247}                          | unicode \_ 位元組 |
| 4     | /app1/ifd/{ushort = 40094}                          | unicode \_ 位元組 |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordXMP  | Unicode        |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordIPTC | Unicode        |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                              |
|-------|---------------------------------------------------|
| 1     | /xmp/dc： subject                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /app1/ifd/{ushort = 18247}                          |
| 4     | /app1/ifd/{ushort = 40094}                          |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordXMP  |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordIPTC |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                              | 磁片格式    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc： subject | Unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /ifd/{ushort = 18247}               | unicode \_ 位元組 |
| 4     | /ifd/{ushort = 40094}               | unicode \_ 位元組 |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                                             | 磁片格式    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc： subject                                | Unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /ifd/{ushort = 18247}                                              | unicode \_ 位元組 |
| 5     | /ifd/{ushort = 40094}                                              | unicode \_ 位元組 |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordXMP             | Unicode        |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordIPTC            | Unicode        |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordIPTC \_ TIFF \_ IRB | Unicode        |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                                             |
|-------|------------------------------------------------------------------|
| 1     | /ifd/xmp/dc： subject                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /ifd/{ushort = 18247}                                              |
| 5     | /ifd/{ushort = 40094}                                              |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordXMP             |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordIPTC            |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto： LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
