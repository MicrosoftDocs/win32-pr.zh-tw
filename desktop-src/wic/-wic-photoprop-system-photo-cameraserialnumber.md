---
description: CameraSerialNumber 屬性的相片中繼資料原則。
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: CameraSerialNumber 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980005"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a>CameraSerialNumber 相片中繼資料原則

[CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md)屬性的相片中繼資料原則。

### <a name="pkey"></a>PKEY

PKEY \_ 相片 \_ CameraSerialNumber

### <a name="containers"></a>容器

JPEG、TIFF

### <a name="read-only"></a>唯讀

No

### <a name="output-propvariant-type"></a>輸出 PROPVARIANT 類型

VT \_ LPWSTR

### <a name="input-type"></a>輸入類型

字串。

### <a name="conflict-resolution-policy"></a>衝突解決原則

不同架構的值會進行協調。

### <a name="precedence-of-paths-jpeg"></a> (JPEG) 的路徑優先順序

如果檔案是 JPEG 格式，處理常式將會讀取、寫入和移除下列路徑中的資料：



| 單 | 路徑                                   | 磁片格式 | 必要 |
|-------|----------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>路徑 (TIFF) 的優先順序

如果檔案採用 TIFF 格式，處理常式將會讀取、寫入和移除下列路徑中的資料



| 單 | 路徑                                       | 磁片格式 | 必要 |
|-------|--------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Yes      |



 

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
