---
description: 開發已排入佇列的元件
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: 開發已排入佇列的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688699"
---
# <a name="developing-queued-components"></a>開發已排入佇列的元件

COM + 佇列元件服務要求所有應用程式方法只包含 \[ in \] 參數，沒有傳回值。 由於用戶端進行呼叫時，不一定可以使用伺服器物件，因此傳送可建立另一個物件的訊息，即可傳回伺服器結果。 如此一來，雙向通訊就不會出現在每個案例中，而只會在需要時，透過一系列物件之間的單向訊息來進行。

若要使用 COM + 佇列的元件服務，您必須已安裝「 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 」服務。 訊息佇列不會自動安裝。 在作業系統安裝期間或使用 [ **新增/移除程式**] 時，必須選取 [訊息佇列]。 內部訊息佇列憑證會在登入時自動建立。

下表中描述的主題提供更多特製化情況的其他考慮。



| 主題                                                                                           | 描述                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [以參數 s 的形式傳遞物件](passing-objects-as-parameters.md)<br/>                   | 描述如何將物件以 \[ in \] 參數傳遞至已排入佇列的元件。<br/>                    |
| [工作組模式中的安全性限制](security-limitations-in-workgroup-mode.md)<br/> | 描述在工作組模式中使用訊息佇列驗證的限制。<br/>       |
| [執行緒考量](threading-considerations.md)<br/>                             | 描述與線上程之間傳遞記錄器介面指標相關的特定考慮。<br/> |
| [接收回應](receiving-a-response.md)<br/>                                     | 說明如何針對已排入佇列的元件呼叫來建立回應。<br/>                           |



 

 

 




