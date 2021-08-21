---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f9f888fcea9069ff31ccef6b2c1ef5a0148fbb34ba21d03ee881c52056f10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105536"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

抓取支援語音輸入所需的條件狀態。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

變數的位址，此變數會接收狀態設定的下列其中一個值：



| 值                                                                               | 描述                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const 不帶正負號的 long** **接聽 \_ 狀態 \_ CANLISTEN = 0;**<br/>               | 條件支援語音輸入。                                                                                                                                                                                                          |
| **const 不帶正負號的 long** **接聽 \_ 狀態 \_ NOAUDIO = 1;**<br/>                 | 此系統上沒有可用的音訊輸入裝置。  (請注意，這不會偵測是否已安裝麥克風;它只能偵測使用者是否已安裝具有正常運作驅動程式的已啟用輸入的音效卡。 )  |
| **const 不帶正負號的 long** **接聽 \_ 狀態 \_ NOTTOPMOST = 2;**<br/>              | 另一個用戶端是此字元的作用中用戶端，或目前的字元不是最上層。                                                                                                                                           |
| **const 不帶正負號的 long** **接聽 \_ 狀態 \_ CANTOPENAUDIO = 3;**<br/>           | 音訊輸入或輸出通道目前忙碌中，其他應用程式正在使用音訊。                                                                                                                                               |
| **const 不帶正負號的 long** **接聽 \_ 狀態 \_ COULDNTINITIALIZESPEECH = 4;**<br/> | 初始化語音辨識子系統的過程中發生未指定的錯誤。 這包括沒有任何語音引擎可符合字元語言設定的可能性。                          |
| **const 不帶正負號的 long** **接聽 \_ 狀態 \_ SPEECHDISABLED = 5;**<br/>          | 使用者已在 [先進字元選項] 視窗中停用語音輸入。                                                                                                                                                              |
| **const 不帶正負號的 long** **接聽 \_ 狀態 \_ 錯誤 = 6;**<br/>                   | 檢查音訊狀態時發生錯誤，但系統不會傳回錯誤的原因。                                                                                                                                |



 

</dd> </dl>

此函數可讓您查詢目前的條件是否支援語音辨識輸入，包括音訊裝置的狀態。 如果您的應用程式使用 [**IAgentCharacterEx：：接聽**](iagentcharacterex--listen.md) 方法，您可以使用此函式，以確保呼叫會成功。 呼叫這個方法也會載入語音引擎（如果尚未載入）。 但是，它不會開啟接聽模式。

在 [代理程式] 屬性工作表中啟用語音輸入時 ([Advanced Character Options]) ，查詢狀態將會載入相關聯的引擎 (如果尚未載入) ，然後啟動 [語音服務]。 亦即，接聽鍵可供使用，而且可以顯示接聽提示。  (接聽鍵和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。

此函數只會傳回用戶端應用程式使用字元的設定;此設定不會反映用戶端應用程式中其他字元或其他字元的用戶端。

 

 





