---
title: 已停用之跟蹤的影像來源
description: 已停用之跟蹤的影像來源
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player 行動外觀 trackbars
- 外觀，trackbars
- 外觀的參考，trackbars
- 外觀中的 trackbars、影像來源
- 外觀的影像來源，trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967201"
---
# <a name="image-source-for-disabled-trackbar"></a>已停用之跟蹤的影像來源

您必須使用您想要用來繪製影像的點陣圖類型，來定義要在停用程式時顯示的影像來源。 您所顯示的影像通常會在超級檔案內，或者，如果您要建立 Windows Media Player 10 行動裝置版的面板，則影像會在 SeekThumb 檔案內。 您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。 然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的點陣圖類型內使用之影像的左上座標 (（以圖元為單位）) 。

例如，若要使用 SeekThumb 點陣圖中的影像，其左上角的位置為50、60圖元，請輸入：


```C++
Disabled @ 50,60

```



您必須為已停用的 [查看] 影像定義影像位置。 如果您不想要顯示新的影像，您可以將背景影像定義為已停用的影像，其位移為0、0：


```C++
Disabled @ 50,60

```



在上述範例中，50，60代表您在 SeekThumb 檔中使用的按鈕位置 (在此案例中，與背景點陣圖上的按鈕相同的位置) 。 不過，強烈建議您針對所有 trackbars 顯示已停用的影像，以提供使用者視覺指示，因為在某些情況下，trackbars 將無法使用。 例如，當目前的播放清單空白時，[搜尋 trackbars] 可能會停用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




