---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player 行動外觀 trackbars
- 外觀，trackbars
- 外觀的參考，trackbars
- 外觀 trackbars，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968245"
---
# <a name="trackbars"></a>Trackbars

[修訂] 會以較小的增量顯示影像。 Trackbars 用於音量控制項和播放位置控制項。 您可以使用 trackbars 顯示目前媒體專案的資訊，或允許使用者變更設定或播放位置。 例如，您可以使用 [顯示] 來讓使用者調整音量，並使用另一個可向使用者顯示目前播放位置的顯示。 Trackbars 有一個 thumb 影像，可定義目前的 [程式] 值的設定。

面板定義檔的 Trackbars 區段必須以這一行開頭：


```C++
[ Trackbars ]

```



然後，您必須新增一或多行，其中包含面板中每個 trackbars 的相關資訊。


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



您可以使用下列範本作為面板定義檔的 Trackbars 區段：


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



您必須在 Trackbars 區段中，針對每一行的資料列資訊使用下列順序， (行的每個部分都必須) ：

1.  [[類型]](trackbar-type.md)
2.  [進行中的位置](trackbar-location.md)
3.  [已停用之跟蹤的影像來源](image-source-for-disabled-trackbar.md)
4.  [Thumb 影像來源](thumb-image-source.md)
5.  [捲動方塊大小](thumb-size.md)

如需 Trackbars 程式碼的範例，請參閱 [範例 Trackbars 一節](sample-trackbars-section.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




