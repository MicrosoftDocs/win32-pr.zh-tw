---
title: '狀態 (Windows Media Player SDK) '
description: 狀態
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Windows Media Player 行動外觀、狀態顯示
- 外觀，狀態顯示
- 外觀的參考、狀態顯示
- 狀態顯示在 [外觀]、[關於]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024417"
---
# <a name="status-windows-media-player-sdk"></a>狀態 (Windows Media Player SDK) 

您可能會想要在您的面板中使用狀態顯示。 如果是，則狀態專案必須定義在面板定義檔中。 或者，您也可以使用 Text 元素中的 Status 屬性來顯示這項資訊。

面板定義檔的 [狀態] 區段開頭為以下這一行：


```C++
[ Status ]

```



然後，您必須新增一或多行，其中包含有關面板中狀態顯示的資訊。


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



您可以使用下列範本作為面板定義檔的 [狀態] 區段：


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



您必須使用上述範本中顯示的順序，以取得 [狀態] 區段中每一行的狀態顯示資訊。 這一行的每個部分都是必要的。 下列各節將說明每個專案：

-   [狀態項目](status-item.md)
-   [狀態位置](status-location.md)
-   [狀態對齊](status-alignment.md)
-   [狀態字型](status-font.md)
-   [狀態色彩](status-color.md)

如需狀態碼的範例，請參閱 [範例狀態一節](sample-status-section.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




