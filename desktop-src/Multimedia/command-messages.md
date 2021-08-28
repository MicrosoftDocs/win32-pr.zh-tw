---
title: 命令訊息
description: 命令訊息
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- MCI 命令訊息，關於
- MCI 命令訊息，語法
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428c89f610f204cfeb75a6c23309c8f3f9846d3136ffac4dbcf0959c5bc4add3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807938"
---
# <a name="command-messages"></a>命令訊息

命令訊息介面是設計來供需要 C 語言介面來控制多媒體裝置的應用程式使用。 它會使用訊息傳遞範例來與 MCI 裝置通訊。 您可以使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式來傳送命令。

如果成功， **mciSendCommand** 函數會傳回零。 如果函式失敗，則傳回值的低序位文字會包含錯誤碼。 您可以將此錯誤碼傳遞至 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) 函式，以取得錯誤的文字描述。

## <a name="syntax-of-command-messages"></a>命令訊息的語法

MCI 命令訊息是由下列元素所組成：

-   常數訊息值
-   包含命令參數的結構
-   一組旗標，指定命令的選項以及驗證參數區塊中的欄位

下列範例會使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式，將 [**MCI \_ PLAY**](mci-play.md) 命令傳送到裝置識別碼所識別的裝置。


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



使用 [**MCI \_ OPEN**](mci-open.md) 命令開啟裝置時，會抓取第一個參數所提供的裝置識別碼。 最後一個參數是 [**MCI \_ PLAY \_ PARMS**](mci-play-parms.md) 結構的位址，其中可能包含開始及結束播放位置的相關資訊。 許多 MCI 命令訊息都使用結構來包含這種類型的參數。 當作業完成時，每個結構的第一個成員會識別接收 [**MM \_ MCINOTIFY**](mm-mcinotify.md) 訊息的視窗。

 

 