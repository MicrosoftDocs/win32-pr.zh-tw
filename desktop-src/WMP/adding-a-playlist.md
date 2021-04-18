---
title: 新增播放清單
description: 新增播放清單
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- 建立外觀、播放清單
- Windows Media Player 的外觀、播放清單
- 外觀，播放清單
- 播放清單、外觀
- 中繼檔播放清單，外觀
- Windows Media 中繼檔播放清單，外觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968648"
---
# <a name="adding-a-playlist"></a>新增播放清單

您可以使用播放清單從音訊和影片的集合中選擇。

您可以使用第一個面板中的圖稿，對外觀定義檔進行一些變更。

第一個步驟是使用您將用於大部分外觀的 shell：


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



現在新增包含播放清單的第二個 **視圖**。 將下列程式碼放在 </VIEW> shell 程式碼的後面。


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



您將需要提供第二個 view 的識別碼，讓您稍後可以參考它。 新增 PLAYELEMENT 和 STOPELEMENT。 這些預先定義的按鈕可讓您更輕鬆地使用。


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



最後，將 onClick 事件新增至 PLAYELEMENT，以在第二個視圖中顯示播放清單：


```C++
            onClick = "JScript: theme.openView('playview');" />

```



您可以在 SDK 的 [範例] 區段中看到類似的工作播放清單面板。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀建立指南**](skin-creation-guide.md)
</dt> </dl>

 

 




