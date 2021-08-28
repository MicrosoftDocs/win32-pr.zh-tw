---
title: 專輯封面
description: 專輯封面
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player行動外觀、專輯封面
- 外觀，專輯封面
- 外觀、專輯封面的參考
- 面板的美工圖案，專輯封面
- 外觀中的專輯封面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8183c7de25c891c59ef68f5938de532a66700400d916c3fc7610a761b2024d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865118"
---
# <a name="album-art"></a>專輯封面

當您建立 Windows Media Player 10 行動裝置版或更新版本的面板時，可能會想要顯示與目前播放之媒體專案相關的專輯封面。 當您設計面板時，您會想要在背景影像中保留空間，以包含專輯封面。

面板定義檔的專輯封面區段必須以下行開頭：


```C++
[ Album Art ]

```



然後，您必須新增資訊，以指定面板中專輯封面的位置和大小。 您必須輸入四個正整數（以逗號分隔），以定義相對於背景影像的專輯封面左邊、頂端、寬度和高度（以圖元為單位）。 下列範例顯示如何指定維度：


```C++
//  <Location>
//  ----------
   5,37,230,155

```



如果您計畫在面板中包含影片區段，您可以針對專輯封面使用相同的大小和位置來節省空間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




