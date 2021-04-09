---
title: 簡單面板的完整程式碼
description: 簡單面板的完整程式碼
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- 建立外觀，程式碼範例
- Windows Media Player 的外觀，程式碼範例
- 外觀，程式碼範例
- 外觀定義檔，程式碼範例
- 建立外觀、範例
- Windows Media Player 的外觀範例
- 外觀，範例
- 外觀定義檔，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840327"
---
# <a name="complete-code-for-simple-skin"></a>簡單面板的完整程式碼

以下是第一個範例面板的完整程式碼：


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



現在您已將所有的元件放在一起。

建立副檔名為 .zip 的壓縮檔案。 此壓縮檔案包含您要包含的面板定義檔、點陣圖和任何數位媒體檔案。 將檔案重新命名，使其副檔名為 wmz。 然後按兩下您的壓縮面板將會開始播放。

您可以在 SDK 的 [範例] 區段中看到類似的工作簡單外觀。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立外觀定義檔**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




