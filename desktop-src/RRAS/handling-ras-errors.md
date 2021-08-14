---
title: 處理 RAS 錯誤
description: 當發生錯誤時，遠端存取連線管理員會叫用用戶端的通知處理常式。
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- 遠端存取服務 RAS，錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b870678eb2dbe95c190bc67415b9abb5481c33918429194404893349c0d7f7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791276"
---
# <a name="handling-ras-errors"></a>處理 RAS 錯誤

當發生錯誤時，遠端存取連線管理員會叫用用戶端的通知處理常式。 通知會指出發生錯誤時的連接狀態，以及識別錯誤的程式碼。 在這些情況下，通知處理常式應該呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 來結束 RAS 連接。

識別 RAS 錯誤的錯誤碼定義于 raserror 檔案中。 RAS 用戶端可以使用 [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) 函數取得描述錯誤的顯示字串。 如需這些錯誤的說明，請參閱 [路由和遠端存取錯誤碼](routing-and-remote-access-error-codes.md) 。

 

 




