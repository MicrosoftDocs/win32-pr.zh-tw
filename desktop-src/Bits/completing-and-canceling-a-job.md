---
title: 完成和取消作業
description: 若要完成傳送作業，請呼叫 IBackgroundCopyJob Complete 方法。
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- 傳送工作 BITS，取消
- 取消作業位
- 傳送工作 BITS，完成
- 完成作業位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 348ee7c4ad4b9a38350e6a1f25d8d05d206b299518cf25197b643dbcb15cb4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835053"
---
# <a name="completing-and-canceling-a-job"></a>完成和取消作業

若要完成傳送作業，請呼叫 [**IBackgroundCopyJob：： complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法。 若為下載工作，您可以在作業狀態為 [已 \_ \_) 傳輸的 BG 工作狀態] 之前，先呼叫 Complete 方法 (，然後再將作業的狀態傳送給工作狀態 \_ 。 只有位在您呼叫 **Complete** 方法之前成功傳送至用戶端的檔案，才可供使用者使用。

針對上傳作業，只有在作業的狀態為 [BG 作業狀態已傳送] 時，才會呼叫 [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法 \_ \_ \_ 。 若要判斷作業的狀態是否為 BG \_ 作業 \_ 狀態 \_ 傳輸，請 [輪詢](polling-for-the-status-of-the-job.md) 作業的狀態屬性或註冊，以接收 bg \_ 通知作業已 \_ \_ 傳送 [事件通知](registering-a-com-callback.md)。

若要取消傳送作業，請呼叫 [**IBackgroundCopyJob：： cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法。 **Cancel** 方法會從傳送佇列中移除工作，並從用戶端移除暫存檔案。 一般來說，如果您無法解決與作業相關聯的錯誤，您就會呼叫這個方法。

如果上傳未完成， [**取消**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法會取消上傳。 如果上傳已完成，且作業的類型為 BG \_ 作業 \_ 類型 \_ 上傳 \_ 回復，則方法會取消回復。

如果您未在90天內呼叫 [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法或 [**IBackgroundCopyJob：： Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法 (預設 [JobInactivityTimeout](group-policies.md) 群組原則) ，服務就會取消作業。 如果服務取消此作業，則不會將下載的檔案和回復檔案提供給用戶端;作業取消不會影響已成功上傳的檔案。 您應該一律呼叫 **Complete** 或 **Cancel** 方法，而不是依賴 JobInactivityTimeout 原則來清除您的工作。 如果達到 MaxJobsPerUser 或 MaxJobsPerMachine 原則限制，佇列中剩餘的作業可能會讓使用者無法建立其他作業。

 

 




