---
title: 非同步作業
description: 當 RasDial 被叫用為非同步作業時，函數會立即傳回。
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db03b1d9d3c98e84bc9a2f4fd80ec7206d9a4524608cdbc96cca83f89d0ea00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030558"
---
# <a name="asynchronous-operations"></a>非同步作業

當 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 被叫用為非同步作業時，函數會立即傳回。 在非同步模式中， **RasDial** 呼叫必須指定當連接作業變更狀態或發生錯誤時，遠端存取連線管理員用來通知用戶端的 [通知處理常式](notification-handlers.md) 。

通知處理常式可以是接收訊息的視窗，也可以是 [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)、 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)或 [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) 回呼函數。 遠端存取連線管理員會在進行 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫的執行緒內容中，進行非同步通知。 基於這個理由，呼叫的執行緒必須等到成功建立連接作業或發生錯誤時才會結束。 在同步模式中，用戶端應用程式可以在建立連線之後安全地終止，而且如果發生錯誤，則必須 [關閉連接](disconnecting.md) 作業。

 

 




