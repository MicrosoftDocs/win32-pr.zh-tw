---
description: Winlogon 會在對話方塊顯示時，將訊息傳送至 GINA。 這些訊息全都封裝在 WLX 的 \_ WM SAS 訊息中，如下所示 \_ 。
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: 將訊息傳送至 GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976874"
---
# <a name="sending-messages-to-the-gina"></a>將訊息傳送至 GINA

[*Winlogon*](../secgloss/w-gly.md) 會在對話方塊顯示時，將訊息傳送至 [*GINA*](../secgloss/g-gly.md) 。 這些訊息全都封裝在 WLX 的 \_ WM SAS 訊息中，如下所示 \_ 。



| WParam 參數中的安全注意順序類型 | Description                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| WLX \_ SAS \_ 類型 \_ CTRL \_ ALT \_ DEL                     | 指出已收到 CTRL + ALT + DEL 鍵序列。                                                                                      |
| WLX \_ SAS \_ 類型 \_ SC \_ INSERT                         | 指出 [*智慧卡*](../secgloss/s-gly.md) 已插入相容的裝置。 |
| WLX \_ SAS \_ 類型 \_ SC \_ REMOVE                         | 表示已從相容裝置移除智慧卡。                                                                        |
| WLX \_ SAS \_ 類型 \_ 使用者 \_ 登出                       | 指出使用者已要求登出。                                                                                                       |
| WLX \_ SAS \_ 類型 \_ SCRNSVR \_ TIMEOUT                   | 指出因為缺少使用者輸入而應執行螢幕保護裝置。                                                                      |
| WLX \_ SAS \_ 類型 \_ 超時                            | 表示在指定的超時時間內未收到任何使用者輸入。                                                               |



 

針對超時和登出，Winlogon 會在傳送訊息之後關閉對話方塊。 這則訊息會傳送，因此對話方塊作業可以用實用的方式回應 (例如，如果) 發生登出，請關閉自己的操作。

針對輸入超時，此對話方塊會以程式碼 WLX \_ DLG 輸入超時的方式 \_ 關閉 \_ 。

若為螢幕保護裝置時間超時，則會關閉此對話方塊，並顯示程式碼 WLX \_ DLG \_ 螢幕 \_ 保護 \_ 超時。

若為登出，則會在程式碼 WLX 使用者登出時關閉對話方塊作業 \_ \_ \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[正在初始化 Winlogon](initializing-winlogon.md)
</dt> <dt>

[Winlogon 狀態](winlogon-states.md)
</dt> <dt>

[支援的對話方塊服務超時作業](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Winlogon 支援函式](authentication-functions.md)
</dt> </dl>

 

 
