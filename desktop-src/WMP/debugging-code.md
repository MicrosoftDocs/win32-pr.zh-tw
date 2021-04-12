---
title: 偵錯程式碼
description: 偵錯程式碼
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Windows Media Player 的面板，偵錯工具代碼
- 外觀，偵錯工具代碼
- 偵錯工具程式碼的程式碼
- Windows Media Player 的外觀、記錄
- 外觀，記錄
- 外觀中的記錄功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301895"
---
# <a name="debugging-code"></a>偵錯程式碼

您通常會想要查看面板中發生的情況。 您可以透過文字控制項或記錄檔來執行此動作。

您可以建立 **文字** 專案，並暫時將其放在面板的一部分上。 例如，您可以使用下列程式碼來建立您的 **TEXT** 元素：


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



比方說，如果您想要查看 Windows Media Player 中數位媒體內容的目前位置，您可以使用類似下面的程式碼，在文字方塊中顯示目前的位置。


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a>將調試資訊寫入記錄檔

若要啟用或停用偵錯工具，請變更下列登錄機碼的值：

**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer 喜好設定 \\ \\ ScriptDebugging**

當您將值設定為1時，就會啟用記錄。 當您將值設定為 0 (預設) 時，會停用記錄。

如果啟用記錄功能，檔案將會放在使用者的電腦上與面板相同的資料夾中。 檔案將命名為 "*filename* \_ 0 \_log.txt"，其中 *filename* 是面板檔案的名稱。 您面板中的程式碼可以使用 *主題* 將文字寫入這個檔案。**logString** 方法。 如果您想要在程式碼執行時判斷在程式碼中發生的狀況，這會很有用。 請注意，文字檔是以 Unicode 字元編碼。

當啟用記錄功能，而且您已安裝提供偵錯工具的開發系統 (例如 Microsoft Visual Studio) 時，不是由腳本所處理的例外狀況會導致每個例外狀況的偵錯工具警告對話方塊開啟。 這是一項實用的功能，可協助您對腳本進行程式碼的偵錯工具。 此外，當啟用記錄功能時，您可以手動將 Windows Media Player 進程附加至偵錯工具。

此 SDK 包含一個範例面板（稱為「記錄」），可示範面板中的記錄功能。 若要深入瞭解如何使用範例，請參閱 [範例](samples.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於外觀**](about-skins.md)
</dt> </dl>

 

 




