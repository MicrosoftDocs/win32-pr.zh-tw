---
title: 新增影片
description: 新增影片
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- 建立外觀、影片
- Windows Media Player 的外觀、影片
- 外觀、影片
- 外觀中的影片，新增
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099778395146cb0bf0f27b483d55dd75c0fb8a0b28b879cc2d388f8e8cb7ba75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055406"
---
# <a name="adding-video"></a>新增影片

只要使用 **video** 元素，並定義要放置影片視窗的位置，您就可以將影片新增到檔案中。

使用與 [選擇檔案] 區段中相同的程式碼;您只需要新增具有頂端、左方、寬度和高度屬性的 **影片** 元素即可。


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



然後當您播放影片時，它就會顯示在視窗中。 影片範例的藝術已修改成稍微放大一個外觀。 由於圖層是在 Photoshop 中使用，因此這些按鈕很容易四處移動，而且會非常快速地建立新的集合。 只有背景影像已變更。 空白圖層中使用填滿，且已新增斜面和浮凸效果。

您可以在 SDK 的 [範例] 區段中看到類似的工作影片外觀。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀建立指南**](skin-creation-guide.md)
</dt> </dl>

 

 




