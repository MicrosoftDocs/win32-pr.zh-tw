---
description: 執行緒考量
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: 執行緒考量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026010"
---
# <a name="threading-considerations"></a>執行緒考量

COM + 佇列元件錄製器能夠在進程的多執行緒單元 (MTA) 或單一執行緒的單元 (STA) 中執行。 當記錄器在 STA 中執行時，COM + 會要求每個包含物件的單元都必須有「 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 」佇列，以處理來自相同進程中其他進程和單元的呼叫。 這表示執行緒的工作函式必須有訊息迴圈。 當已排入佇列的元件具現化時，傳回的介面指標一律為 proxy 介面指標，而不是直接介面指標。 指標實際上是對記錄器實例的參考。 如果將此錄製器介面參考傳遞至另一個執行緒，原始執行緒仍必須執行 Windows 訊息迴圈，才能讓接收端執行緒 unmarshal 介面。 如果不是這種情況，接收端執行緒會在呼叫 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)時停止回應。

如果您使用基本專案來同步處理執行緒，請考慮使用 [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ，而不是其他同步處理函數。 這會檢查佇列中的訊息，以及同步處理物件的狀態。

 

 
