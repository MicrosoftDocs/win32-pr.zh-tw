---
title: 評等
description: 評等
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Windows Media Player 行動外觀、評等
- 外觀、評等
- 外觀、評等的參考
- 外觀中的評等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969474"
---
# <a name="ratings"></a>評等

當您建立適用于 Windows Media Player 10.1 行動裝置的面板時，您可以顯示與目前現正播放之以 Windows Media 音訊為基礎的內容相關聯的評等。 評等會顯示為星號，其中有一個數位。 星號將會從1到5編號，表示該內容目前的評等。 如果內容未分級，星號將會以零為數字。

面板定義檔的 [評等] 區段開頭為以下這一行：


```C++
[ Ratings ]

```



然後，您必須在面板中新增包含評等圖示大小和位置相關資訊的行。


```C++
147, 3, 22, 21       ratings96S.gif

```



您可以使用下列範本作為面板定義檔的評等區段：


```C++
// <Location>           <Image>
// ---------------      --------------------
```



您也可以透過 Windows Media Player 10.1 行動裝置中的使用者介面，將分級值指派給媒體專案，並在裝置下次與電腦進行同步處理時，將新的分級值傳播至該媒體專案，如果該媒體專案位於 Windows Media Player 10 程式庫中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




