---
title: Windows Media Player SDK) 的點陣圖 (
description: 點陣圖
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player 行動外觀、點陣圖
- 外觀，點陣圖
- 外觀、點陣圖的參考
- 外觀中的點陣圖，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464005"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Windows Media Player SDK) 的點陣圖 (

您必須在面板中使用一或多個映射，而且每個影像都必須定義于面板定義檔中。 如果您未在此區段中定義影像，您的面板將無法使用它。

整個參考中都會使用「點陣圖」一詞，並使用 .bmp 副檔名、GIF 影像（副檔名為 .jpg）、JPEG 影像（副檔名為 .jpg）和 PNG 影像（副檔名為 .png）來參考點陣圖影像。

面板定義檔的點陣圖區段開頭為以下這一行：


```C++
[ Bitmaps ]

```



然後，您必須新增一或多行，其中包含面板中每個影像的相關資訊。

一般的行可能是：


```C++
    Background  Background.bmp  0,0

```



您可以使用下列範本作為面板定義檔的點陣圖區段：


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



點陣圖區段中每一行的點陣圖資訊都必須使用下列順序。 這一行的每個部分都是必要的。

1.  [點陣圖類型](bitmap-type.md)
2.  [檔案名稱](file-name.md)
3.  [座標](coordinates.md)

如需點陣圖程式碼的範例，請參閱 [範例點陣圖一節](sample-bitmap-section.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




