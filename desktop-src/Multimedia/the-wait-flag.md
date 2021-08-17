---
title: 等候旗標
description: 等候旗標
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT 旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311e1a55e756cfc3c1038f6ab3ccb4b708bb066dde962afff31006dcf39b7c4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801432"
---
# <a name="the-wait-flag"></a>等候旗標

MCI 命令通常會立即傳回給使用者，即使需要幾分鐘的時間才能完成命令所起始的動作。 您可以使用「等待」 (MCI \_ wait) 旗標，指示裝置等待直到要求的動作完成後，再將控制權傳回給應用程式。

例如，下列 [**play**](play.md) 命令不會將控制權傳回給應用程式，直到播放完成為止：


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> 使用者可以藉由按下 break 鍵來取消等候作業。 依預設，此索引鍵是 CTRL + BREAK。 應用程式可以使用 [**break**](break.md) ([**MCI \_ break**](mci-break.md)) 命令來重新定義此機碼。  (**mci \_ break** 會使用 [**MCI \_ break \_ PARMS**](mci-break-parms.md) 結構。 ) 等候作業取消時，MCI 會嘗試將控制權傳回給應用程式，而不會中斷與「等候」旗標相關聯的命令。

 

 

 




