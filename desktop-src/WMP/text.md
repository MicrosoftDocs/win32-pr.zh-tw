---
title: " (Windows Media Player SDK) 的文字"
description: Text
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player 行動外觀、文字
- 外觀，文字
- 外觀的參考、文字
- 外觀中的文字，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843012"
---
# <a name="text-windows-media-player-sdk"></a> (Windows Media Player SDK) 的文字

您可能會想要在面板中使用一或多個文字顯示方塊。 您使用的每個文字顯示方塊都必須定義在外觀定義檔中。 如果您未在此區段中定義文字顯示框，您的面板將無法使用它。

面板定義檔的文字區段開頭為以下這一行：


```C++
[ Text ]

```



然後，您必須新增一或多行，其中包含面板中每個文字顯示方塊的相關資訊


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



您可以使用下列範本作為面板定義檔的文字區段：


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



您必須使用上述範本中所示的順序，來顯示文字區段中每一行的文字顯示框資訊。 這一行的每個部分都是必要的。 下列各節將詳細說明每個專案。

1.  [文字類型](text-type.md)
2.  [文字位置](text-location.md)
3.  [文字對齊](text-alignment.md)
4.  [文字字型](text-font.md)
5.  [文字色彩](text-color.md)

如需文字程式碼的範例，請參閱 [範例文字一節](sample-text-section.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




