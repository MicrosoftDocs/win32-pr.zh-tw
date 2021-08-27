---
title: Thumb 影像來源
description: Thumb 影像來源
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player行動外觀、trackbars
- 外觀，trackbars
- 外觀的參考，trackbars
- 外觀中的 trackbars、影像來源
- 面板中的 trackbars、thumb 影像來源
- 外觀的影像來源，trackbars
- thumb、影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550569a2858ba283824f28f6793097caa140c6112bccc41b3423413e17b6d89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122768"
---
# <a name="thumb-image-source"></a>Thumb 影像來源

您必須定義包含 thumb 影像的檔案名。 這個名稱必須是副檔名為 .bmp、.gif、.jpg 或 .png 的有效檔案名。 檔案必須包含三個相同大小的並存影像。 它們必須彼此相鄰，不含空格。 左邊影像的左上角必須位在檔案的左上角。 左邊的影像是捲動方塊影像的一般影像，而中間的影像會描繪出推入的狀態，右側的影像則會描繪出已停用的狀態。


```C++
SeekThumb.bmp

```



您可能會想要讓 thumb 影像的特定區域變成透明的。 這可讓您在矩形以外的圖形中建立 thumb 影像。 您以 RGB 值255、0、255所指定色彩填滿的 thumb 影像的任何區域，在您的面板中將會顯示為透明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




