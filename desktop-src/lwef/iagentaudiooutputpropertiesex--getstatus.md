---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380742"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx：： GetStatus

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

捕獲音訊通道的狀態。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

音訊輸出通道的狀態，它可能是下列其中一個值：



| 值                                                                         | 描述                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **const 不帶正負號的短****音訊 \_ 狀態 \_ 可用 = 0;**<br/>         | 音訊輸出通道可用 () 不會忙碌。                                                              |
| **const 不帶正負號的短****音訊 \_ 狀態 \_ NOAUDIO = 1;**<br/>           | 不支援音訊輸出;例如，因為沒有音效卡。                             |
| **const 不帶正負號的短****音訊 \_ 狀態 \_ CANTOPENAUDIO = 2;**<br/>     | 無法開啟音訊輸出通道 (忙碌中) ;例如，因為另一個應用程式現正播放音訊。 |
| **const 不帶正負號的短****音訊 \_ 狀態 \_ USERSPEAKING = 3;**<br/>      | 音訊輸出通道忙碌中，因為伺服器正在處理使用者語音輸入                            |
| **const 不帶正負號的短****音訊 \_ 狀態 \_ CHARACTERSPEAKING = 4;**<br/> | 音訊輸出通道正在忙碌中，因為字元目前正在說話中。                                    |
| **const 不帶正負號的短****音訊 \_ 狀態 \_ SROVERRIDEABLE = 5;**<br/>    | 音訊輸出通道不在忙碌中，但正在等候使用者語音輸入。                                 |
| **const 不帶正負號的短****音訊 \_ 狀態 \_ 錯誤 = 6;**<br/>             | 嘗試存取音訊輸出通道時發生一些其他 (未知的) 問題。                       |



 

</dd> </dl>

這項設定可讓您的用戶端應用程式查詢音訊輸出通道的狀態。 您可以使用此資訊來判斷是否要使用 **IAgentCharacterEx：：接聽**) 來說出要使用的字元，或嘗試開啟接聽模式 (。

 

 





