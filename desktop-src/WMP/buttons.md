---
title: Windows Media Player SDK) 的按鈕 (
description: 按鈕
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player行動外觀，按鈕總覽
- 外觀，按鈕總覽
- 外觀、按鈕的參考
- 面板中的按鈕，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128c723c5b8bbac31c82a32060704bc892dfb7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885538"
---
# <a name="buttons-windows-media-player-sdk"></a>Windows Media Player SDK) 的按鈕 (

您會想要在面板中使用一或多個按鈕，而且每個按鈕都必須定義于面板定義檔中。 如果您未在此區段中定義按鈕，您的面板將無法使用它。

面板定義檔的 [按鈕] 區段開頭為以下這一行：


```C++
[ Buttons ]

```



然後，您必須新增一或多行，其中包含面板中每個按鈕的相關資訊。 一般的行可能是：


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



請注意，此程式碼的類型應該是以 "PlayPause" 為開頭的一行，並以 "推送 @ 160，98" 結尾。

您可以針對面板定義檔的按鈕區段使用下列範本：


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



同樣地，請注意，這些應輸入為單一行，第一個開頭為 "// &lt; Function &gt; "，結尾為 " &lt; Push 2 Image Src &gt; "。 第二行的開頭為 "//----------"，結尾為 "------------------."

按鈕區段中每一行的按鈕資訊必須以下列順序顯示。 只有行的前六個部分是必要的。 除非必要，否則不會包含次要映射。

1.  [Button 函數](button-function.md)
2.  [按鈕類型](button-type.md)
3.  [按鈕位置](button-location.md)
4.  [推送的影像來源](pushed-image-source.md)
5.  [已停用按鈕的影像來源](image-source-for-disabled-button.md)
6.  [點擊 RGB 色彩](hit-rgb-color.md)
7.  [一般次要影像來源](normal-secondary-image-source.md)
8.  [一般的三映射來源](normal-tertiary-image-source.md)
9.  [推送的次要影像來源](pushed-secondary-image-source.md)
10. [推送的第三個映射來源](pushed-tertiary-image-source.md)

如需按鈕程式碼的範例，請參閱 [範例按鈕一節](sample-button-section.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




