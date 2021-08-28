---
title: '描述 (Windows Media Player SDK) '
description: 描述
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player行動外觀、描述區段
- 外觀，描述區段
- 外觀的參考，描述區段
- 外觀中的描述區段
- 外觀定義檔，描述區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ca5235939352ffabb924aaf38a706b436d4c1358a92b9aef4996614c53623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749955"
---
# <a name="description-windows-media-player-sdk"></a>描述 (Windows Media Player SDK) 

當您為 Windows Mobile 2003 或更新版本的 Windows Media Player 9 系列建立面板時，必須包含描述區段。 [描述] 區段可讓您指定顯示器的寬度和高度、顯示解析度，以及設計面板的顯示方向。 [描述] 區段必須出現在面板定義檔中的任何其他區段之前，以及在初始版本宣告之後。

面板定義檔的 [描述] 區段必須以下行開頭：


```C++
[ Description ]

```



然後，您必須新增面板的維度和顯示解析度的相關資訊。 下列範例顯示如何指定維度：


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



這會指定您將顯示的面板設計為240圖元寬、320圖元高，以及使用 96 DPI 顯示器解析度。 請注意，這表示直向模式的方向。

您可以選擇性地指定您在 [描述] 區段中設計面板的方向模式。 下列範例顯示如何指定方向：


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



下表列出您可能用於方向的值。



| 方向 | 描述                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| 橫向   | 外觀的寬度大於面板的高度。 顯示是以水準方式導向。   |
| 直向    | 外觀的高度大於面板的寬度。 顯示器是以垂直方式導向。 |
| Square      | 外觀的高度等於面板的寬度。 顯示器沒有方向。                    |



 

> [!Note]  
> 當面板定義檔中指定的描述區段符合裝置目前的狀態時，Windows 行動2003的 Windows Media Player 9 系列將只會顯示特定的外觀。

 

您應該小心指定您的面板所撰寫的正確維度、解析度和方向。 例如，如果您的外觀所指定的維度描述了橫向的方向，則當裝置處於直向模式時，您的面板將無法使用，即使您在方向線中指定直向。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




