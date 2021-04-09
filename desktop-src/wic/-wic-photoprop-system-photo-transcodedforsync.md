---
description: TranscodedForSync 屬性的相片中繼資料原則。
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: TranscodedForSync 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851211"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>TranscodedForSync 相片中繼資料原則

[TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ TranscodedForSync

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ BOOL

### <a name="input-type"></a>輸入類型

布林值。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="jpeg-policy"></a>JPEG 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                  | 磁片格式  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort = 18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                  | 磁片格式  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort = 18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/{ushort = 18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>TIFF 原則

### <a name="read-paths"></a>讀取路徑



| 單 | 路徑                                      | 磁片格式  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort = 18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>寫入路徑



| 單 | 路徑                                      | 磁片格式  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort = 18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>移除路徑



| 單 | 路徑                                      |
|-------|-------------------------------------------|
| 1     | /ifd/{ushort = 18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
