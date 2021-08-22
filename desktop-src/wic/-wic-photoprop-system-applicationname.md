---
description: System.servicemodel 屬性的相片中繼資料原則。
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: System.servicemodel 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3084f21453a82c79925d4a164f5f847c3a24968009b7b8c4236ce3a40872dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710917"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>System.servicemodel 相片中繼資料原則

System.servicemodel 屬性的相片中繼資料[原則。](../properties/props-system-applicationname.md)

### <a name="pkey"></a>PKEY

PKEY \_ ApplicationName

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-type"></a>輸入類型

String

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                         | 磁片格式 |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort = 305}                       | ascii       |
|       | /app13/irb/8bimiptc/iptc/Originating 計畫 |             |
|       | /xmp/xmp:CreatorTool                         | Unicode     |
|       | /xmp/xmp:creatortool                         | Unicode     |
|       | /xmp/tiff：軟體                           | Unicode     |
|       | /xmp/tiff：軟體                           | Unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating 計畫 |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                         | 磁片格式 |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort = 305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | Unicode     |
|       | /xmp/xmp:creatortool                         | Unicode     |
|       | /xmp/tiff：軟體                           | Unicode     |
|       | /xmp/tiff：軟體                           | Unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating 計畫 |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                         |
|-------|----------------------------------------------|
|       | /app1/ifd/{ushort = 305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /xmp/tiff：軟體                           |
|       | /xmp/tiff：軟體                           |
|       | /app13/irb/8bimiptc/iptc/Originating 計畫 |



 

### <a name="tiff-policy"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                       | 磁片格式 |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort = 305}                          | ascii       |
|       | /ifd/iptc/Originating 計畫              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | Unicode     |
|       | /ifd/xmp/xmp:creatortool                   | Unicode     |
|       | /ifd/xmp/tiff：軟體                     | Unicode     |
|       | /ifd/xmp/tiff：軟體                     | Unicode     |
|       | /ifd/iptc/Originating 計畫              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating 計畫 |             |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                       | 磁片格式 |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort = 305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | Unicode     |
|       | /ifd/xmp/xmp:creatortool                   | Unicode     |
|       | /ifd/xmp/tiff：軟體                     | Unicode     |
|       | /ifd/xmp/tiff：軟體                     | Unicode     |
|       | /ifd/iptc/Originating 計畫              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating 計畫 |             |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                       |
|-------|--------------------------------------------|
|       | /ifd/{ushort = 305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /ifd/xmp/tiff：軟體                     |
|       | /ifd/xmp/tiff：軟體                     |
|       | /ifd/iptc/Originating 計畫              |
|       | /ifd/irb/8bimiptc/iptc/Originating 計畫 |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System.servicemodel](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
