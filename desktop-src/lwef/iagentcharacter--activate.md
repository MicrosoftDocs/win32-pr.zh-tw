---
title: IAgentCharacter 啟用
description: IAgentCharacter 啟用
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507472"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter：： Activate

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

設定用戶端是否為使用中或字元是否最上層。

-   傳回 \_ [確定] 表示作業成功。
-   傳回 \_ FALSE，表示作業不成功。

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

您可以為此參數指定下列值：



| 值 | 描述                   |
|-------|-------------------------------|
| 0     | 設定為非作用中用戶端。 |
| 1     | 設定為使用中用戶端。     |
| 2     | 將最上層的字元設為最上層。   |



 

</dd> </dl>

當有多個字元可見時，一次只能有一個字元接收語音輸入。 同樣地，當多個用戶端應用程式共用相同的字元時，只有其中一個用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 一次。 用來接收滑鼠和語音輸入的字元集是最上層的字元，而接收輸入的用戶端是字元的作用中用戶端。  (最頂端的字元視窗也會出現在字元視窗的迭置順序頂端。 ) 一般是由使用者明確選取時，判斷哪一個字元最上層。 不過，當字元顯示或隱藏 (字元變成或不再是最上層時，最上層啟用也會變更。 ) 

您也可以使用這個方法，在用戶端收到導向字元的輸入時明確管理，例如當您的應用程式本身變成作用中時。 例如，將 [ **狀態** ] 設定為 [2] 會將字元設為最上層，而您的用戶端會接收使用者與該字元互動所產生的所有滑鼠和語音輸入事件。 因此，它也會讓您的用戶端成為字元的輸入主動用戶端。 不過，您也可以將 [ **狀態** ] 設定為 [1]，為字元設定使用中用戶端，而不讓字元最上層。 這可讓您的用戶端在字元變成最上層時，接收導向該字元的輸入。 同樣地，您可以將用戶端設定為非作用中的用戶端 (不會在字元變成最上層時，藉由將 **狀態** 設為0來接收輸入) 。 您可以使用 [**IAgentCharacter：： HasOtherClients**](iagentcharacter--hasotherclients.md)來判斷某個字元是否有其他目前的用戶端。

避免直接在 [**Show**](iagentcharacter--show.md) 方法之後呼叫此方法。 **顯示** 自動設定輸入-主動用戶端。 隱藏字元時，如果在 **Show** 方法完成之前處理，**啟動** 呼叫可能會失敗。

當指定的字元隱藏時，嘗試以 **State** 參數設定為 2 () 將會失敗。 同樣地，如果您將 **狀態** 設定為0，而您的應用程式是唯一的用戶端，則此呼叫會失敗。 字元必須一律具有最上層的用戶端。

> [!Note]  
> 除非沒有載入任何其他字元，或您的應用程式已經輸入-主動，否則以將 **狀態** 設定為1的方法呼叫此方法通常不會產生 [**AgentNotifySink：： ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) 事件。

 

## <a name="see-also"></a>另請參閱

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




