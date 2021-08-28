---
title: Windows Media Player SDK) 的點陣圖 (
description: 點陣圖
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player行動外觀、點陣圖
- 外觀，點陣圖
- 外觀、點陣圖的參考
- 外觀中的點陣圖，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ff4689c052162d8addfb9a66aeb6b227916f0e22e21de3e3572ea265380664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123858"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Windows Media Player SDK) 的點陣圖 (

您必須在面板中使用一或多個映射，而且每個影像都必須定義于面板定義檔中。 如果您未在此區段中定義影像，您的面板將無法使用它。

整個參考中都會使用「點陣圖」一詞，並以 .bmp 副檔名、具有 .gif 副檔名的 GIF 影像、具有 .jpg 副檔名的 JPEG 影像，以及具有 .png 副檔名的 PNG 影像來參考點陣圖影像。

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

 

 




