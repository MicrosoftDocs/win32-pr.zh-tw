---
description: 以非同步方式完成的作業會在應用程式所進行的函式呼叫中執行部分處理，並在 TAPI 2.x 從函式呼叫傳回之後，在獨立的執行執行緒中執行它的其餘部分。
ms.assetid: 37b544e4-6413-4741-b8b6-ec676ce4ca97
title: 非同步函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e792a4b1d6a25a4f49fbb2abe2c19ce3071ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983726"
---
# <a name="asynchronous-functions"></a>非同步函式

以非同步方式完成的作業會在應用程式所進行的函式呼叫中執行部分處理，並在 TAPI 2.x 從函式呼叫傳回之後，在獨立的執行執行緒中執行它的其餘部分。 為了確保呼叫的處理完成，服務提供者會將要求向量化至系統中的另一個作用中實體，例如 LAN 伺服器、增益集硬體、交換器或網路，然後返回應用程式。 目前，負的錯誤結果或正面的要求識別碼會傳回給應用程式。

在非同步完成時 (服務提供者已從硬體收到插斷，表示訊息必須傳遞) ，服務提供者會呼叫 TAPISRV 和「事件 *X* 剛剛發生的報告」。 傳遞適當的訊息給所有相關的應用程式。」 當 TAPISRV 接收到此訊息時，它會將訊息轉送至 TAPI 動態連結程式庫，在應用程式的進程中，接著會根據 [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) 或 [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)中的應用程式所選取的訊息通知配置，張貼視窗訊息、通知事件控制碼或張貼至 i/o 完成埠。

當作業的非同步部分完成時，會將 [**行 \_ 回復**](./line-reply.md) (或 [**電話 \_ 回復**](./phone-reply.md)) 訊息傳送至應用程式。 此訊息包含了函式呼叫所傳回的要求識別碼，做為它的其中一個參數。 此要求識別碼可讓應用程式判斷已完成的原始要求。  (的應用程式應該記得所有進行中要求的要求識別碼，以便能夠正確處理回復訊息。 ) 第二個參數換行 \_ 回復 (或電話 \_ 回復) 訊息是非同步傳回值。 這是錯誤 (的負數值) 如果作業順利完成，則為零。 若為非同步作業，任何傳回值可能會傳回做為函式傳回的一部分，或做為行 \_ 回復或電話回復訊息中的 dwParam2 參數 \_ 。 值0表示成功，只會傳回在行 \_ 回復訊息中，而絕不會傳回給函數的傳回值。

Initialize 函數 ( [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) 和 [**PHONEINITIALIZEEX**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)) 告知 TAPI 如何將這些訊息傳送至應用程式。

> [!Note]  
> 在某些情況下，如果多執行緒應用程式從應用程式初始化線路或電話裝置的執行緒以外的執行緒呼叫非同步函式，則應用程式可能會在非同步函式傳回之前，收到 [**行 \_ 回復**](./line-reply.md) 或 [**電話 \_ 回復**](./phone-reply.md) 訊息。 在這種情況下，應用程式應該儲存訊息參數並等候非同步函式傳回，而且在處理訊息之前，要求識別碼是已知的。

 

 

 
