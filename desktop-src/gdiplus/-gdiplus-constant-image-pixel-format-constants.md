---
description: 下列常數定義于 Gdipluspixelformats 中，指定點陣圖中使用的各種像素格式。
ms.assetid: 362204c5-5dd7-461a-b90b-15826c025689
title: '影像像素格式常數 (Gdipluspixelformats .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62abc8b0ed606b958764e27171f8b45e619d23b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974813"
---
# <a name="image-pixel-format-constants"></a>影像像素格式常數

下列常數定義于 Gdipluspixelformats 中，指定點陣圖中使用的各種像素格式。



| 常數                                                                                                                                                                                                                                     | 描述                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat1bppIndexed"></span><span id="pixelformat1bppindexed"></span><span id="PIXELFORMAT1BPPINDEXED"></span><dl> <dt>**PixelFormat1bppIndexed**</dt> </dl>             | 指定格式為每圖元1位，已編制索引。<br/>                                                                                                                                                         |
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>             | 指定格式為每像素 4 位元的索引色彩。<br/>                                                                                                                                                        |
| <span id="PixelFormat8bppIndexed"></span><span id="pixelformat8bppindexed"></span><span id="PIXELFORMAT8BPPINDEXED"></span><dl> <dt>**PixelFormat8bppIndexed**</dt> </dl>             | 指定格式為每像素 8 位元的索引色彩。<br/>                                                                                                                                                        |
| <span id="PixelFormat16bppARGB1555"></span><span id="pixelformat16bppargb1555"></span><span id="PIXELFORMAT16BPPARGB1555"></span><dl> <dt>**PixelFormat16bppARGB1555**</dt> </dl>     | 指定格式為每圖元16位;1位用於 Alpha 元件，而每個位用於紅色、綠色和藍色元件。<br/>                                                       |
| <span id="PixelFormat16bppGrayScale"></span><span id="pixelformat16bppgrayscale"></span><span id="PIXELFORMAT16BPPGRAYSCALE"></span><dl> <dt>**PixelFormat16bppGrayScale**</dt> </dl> | 指定格式為每圖元16位，灰階。<br/>                                                                                                                                                     |
| <span id="PixelFormat16bppRGB555"></span><span id="pixelformat16bpprgb555"></span><span id="PIXELFORMAT16BPPRGB555"></span><dl> <dt>**PixelFormat16bppRGB555**</dt> </dl>             | 指定格式為每像素 16 位元；各有 5 位元用於紅色、綠色和藍色元件。 剩餘的位元則不使用。<br/>                                                                   |
| <span id="PixelFormat16bppRGB565"></span><span id="pixelformat16bpprgb565"></span><span id="PIXELFORMAT16BPPRGB565"></span><dl> <dt>**PixelFormat16bppRGB565**</dt> </dl>             | 指定格式為每像素 16 位元，5 位元用於紅色元件、6 位元用於綠色元件，5 位元用於藍色元件。<br/>                                    |
| <span id="PixelFormat24bppRGB"></span><span id="pixelformat24bpprgb"></span><span id="PIXELFORMAT24BPPRGB"></span><dl> <dt>**PixelFormat24bppRGB**</dt> </dl>                         | 指定格式為每像素 24 位元；各有 8 位元用於紅色、綠色和藍色元件。<br/>                                                                                                  |
| <span id="PixelFormat32bppARGB"></span><span id="pixelformat32bppargb"></span><span id="PIXELFORMAT32BPPARGB"></span><dl> <dt>**PixelFormat32bppARGB**</dt> </dl>                     | 指定格式為每像素 32 位元；各有 8 位元用於 Alpha、紅色、綠色和藍色元件。<br/>                                                                                           |
| <span id="PixelFormat32bppPARGB"></span><span id="pixelformat32bpppargb"></span><span id="PIXELFORMAT32BPPPARGB"></span><dl> <dt>**PixelFormat32bppPARGB**</dt> </dl>                 | 指定格式為每像素 32 位元；各有 8 位元用於 Alpha、紅色、綠色和藍色元件。 紅色、綠色、藍色元件會根據 Alpha 元件來預先相乘。<br/>   |
| <span id="PixelFormat32bppRGB"></span><span id="pixelformat32bpprgb"></span><span id="PIXELFORMAT32BPPRGB"></span><dl> <dt>**PixelFormat32bppRGB**</dt> </dl>                         | 指定格式為每像素 32 位元；各有 8 位元用於紅色、綠色和藍色元件。 剩餘的 8 位元則不使用。<br/>                                                               |
| <span id="PixelFormat48bppRGB"></span><span id="pixelformat48bpprgb"></span><span id="PIXELFORMAT48BPPRGB"></span><dl> <dt>**PixelFormat48bppRGB**</dt> </dl>                         | 指定格式為每像素 48 位元；各有 16 位元用於紅色、綠色和藍色元件。<br/>                                                                                                 |
| <span id="PixelFormat64bppARGB"></span><span id="pixelformat64bppargb"></span><span id="PIXELFORMAT64BPPARGB"></span><dl> <dt>**PixelFormat64bppARGB**</dt> </dl>                     | 指定格式為每像素 64 位元；各有 16 位元用於 Alpha、紅色、綠色和藍色元件。<br/>                                                                                          |
| <span id="PixelFormat64bppPARGB"></span><span id="pixelformat64bpppargb"></span><span id="PIXELFORMAT64BPPPARGB"></span><dl> <dt>**PixelFormat64bppPARGB**</dt> </dl>                 | 指定格式為每像素 64 位元；各有 16 位元用於 Alpha、紅色、綠色和藍色元件。 紅色、綠色、藍色元件會根據 Alpha 元件來預先相乘。 <br/> |



## <a name="remarks"></a>備註

**PixelFormat48bppRGB**、 **PixelFormat64bppARGB** 和 **PixelFormat64bppPARGB** 會使用每個色彩元件的16個位 (通道) 。 Windows GDI + 1.0 版可以讀取16個位元組的每個通道映射，但是這類影像會轉換成每個通道的8位元組格式，以進行處理、顯示和儲存。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Gdipluspixelformats。h</dt> </dl> |



 

 




