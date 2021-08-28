---
description: '[系統著作權] 屬性的相片中繼資料原則。'
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: System. 著作權相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3e17190205b3df5c2ede9b1a7db231d0fdbbe21
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882699"
---
# <a name="systemcopyright-photo-metadata-policy"></a>System. 著作權相片中繼資料原則

[ [系統著作權](../properties/props-system-copyright.md) ] 屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 著作權

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

否

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>輸入 PROPVARIANT 類型

String

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                      | 磁片格式 |
|-------|-------------------------------------------|-------------|
|       | /app1/ifd/{ushort = 33432}                  | ascii       |
|       | /app13/irb/8bimiptc/iptc/copyright 通知 |             |
|       | /xmp/ &lt; xmpalt &gt; dc：許可權              | Unicode     |
|       | /xmp/dc：許可權                            | Unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright 通知 |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                      | 磁片格式 |
|-------|-------------------------------------------|-------------|
|       | /xmp/dc：許可權                            | Unicode     |
|       | /xmp/ &lt; xmpalt &gt; dc：許可權              | Unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright 通知 |             |
|       | /app1/ifd/{ushort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                      |
|-------|-------------------------------------------|
|       | /xmp/dc：許可權                            |
|       | /app13/irb/8bimiptc/iptc/copyright 通知 |
|       | /app1/ifd/{ushort = 33432}                  |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                    | 磁片格式 |
|-------|-----------------------------------------|-------------|
|       | /ifd/{ushort = 33432}                     | ascii       |
|       | /ifd/iptc/copyright 通知              |             |
|       | /ifd/xmp/ &lt; xmpalt &gt; dc：許可權        | Unicode     |
|       | /ifd/xmp/dc：許可權                      | Unicode     |
|       | /ifd/iptc/copyright 通知              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright 通知 |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                    | 磁片格式 |
|-------|-----------------------------------------|-------------|
|       | /ifd/xmp/dc：許可權                      | Unicode     |
|       | /ifd/xmp/ &lt; xmpalt &gt; dc：許可權        | Unicode     |
|       | /ifd/iptc/copyright 通知              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright 通知 |             |
|       | /ifd/{ushort = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                    |
|-------|-----------------------------------------|
|       | /ifd/xmp/dc：許可權                      |
|       | /ifd/iptc/copyright 通知              |
|       | /ifd/irb/8bimiptc/iptc/copyright 通知 |
|       | /ifd/{ushort = 33432}                     |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統著作權](../properties/props-system-copyright.md)
</dt> </dl>

 

 
