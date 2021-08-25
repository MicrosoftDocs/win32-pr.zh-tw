---
title: 警示功能
description: 網路管理警示功能會通知網路服務程式和網路事件的應用程式。
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411a9bab5f8b74b5dc6e83d9a3c09cdcaeebf66d34c265ad27639e7aab8d7c00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912458"
---
# <a name="alert-functions"></a>警示功能

\[由於不支援「警報器」和「messenger」服務，因此不支援 Windows Vista 的警示功能。\]

網路管理警示功能會通知網路服務程式和網路事件的應用程式。 *事件* 是由應用程式所定義的進程、出現或硬體狀態的特定實例。 警示函數可讓應用程式指出預先定義的事件發生的時間。

**Windows Server 2003：** 預設會停用 Windows Server 2003 上的「警報器」和「messenger」服務。 您必須重新啟用服務，才能呼叫網路管理警示功能或網路管理 [訊息功能](message-functions.md)。

警示功能如下所示。



| 函式                                   | 描述                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | 通知所有已註冊的用戶端發生特定事件。                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | 簡化通知已註冊的用戶端發生特定事件，因為不同于 **NetAlertRaise**， **NetAlertRaiseEx** 不需要 [**STD \_ 警示**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) 結構。 |



 

當您呼叫 **NetAlertRaise** 函數或 **NetAlertRaiseEx** 函式時，必須在用戶端電腦上執行警報器服務。 如果服務未執行，則函式會失敗並 **\_ \_ \_ 找不到錯誤** 檔案。 用戶端上的警報器服務會呼叫 [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) 函數，以將資訊傳送給收件者。

應用程式、網路服務和內部網路元件會使用網路管理警示功能來引發警示，並在發生特定類型的事件時通知各種應用程式或使用者。 警示類別目錄函數、資料類型、結構和常數都定義于 LMCONS 中。H、LMERR。H 和 LMALERT。H 標頭檔。 若要存取這些定義，請定義 \_ 包含 NETERRORS 和 include NETALERT 的常數， \_ 並包含標頭檔的 LM. H。

LMALERT。H file 預先定義下列警示類別 () 傳送警示的網路事件種類：

-   需要系統管理協助的網路事件
-   將專案新增至錯誤記錄檔
-   由使用者或應用程式接收廣播訊息
-   完成列印工作
-   使用者使用特定應用程式或資源

您可以視需要定義網路應用程式的其他警示類別。 例如，如果伺服器上的應用程式會定期將大量資料寫入磁片磁碟機，應用程式就會執行填滿磁片的風險。 在此情況下，您可能會想要新增事件「沒有可用磁碟空間」來觸發警示，通知應用程式暫停或終止正在填滿磁片的處理常式。 警示的事件名稱可以是任何文字字串。

當您在呼叫 [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) 函式時引發警示時，訊息資料應該包含一個 [**標準 \_ 警示**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) 標頭結構，後面接著另一個系統 [**管理員 \_ 其他 \_ 資訊**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info)中警示特定的固定長度資料， [**Cbenginecurr.errlog \_ 其他 \_ 資訊**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info)、 [**列印 \_ 其他 \_**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)資訊或 [**使用者 \_ 其他 \_ 資訊**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) 結構。 其他可變長度的資料可以遵循警示特定結構。 [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex)函數的 (呼叫不需要 **STD \_ 警示** 結構。 ) 呼叫端應用程式必須配置所有結構和可變長度資料的記憶體，並且在呼叫傳回之後釋放記憶體。

下列宏可用於警示資料緩衝區。



| 巨集                                          | 描述                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**警示 \_ 其他 \_ 資訊**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | 傳回在警示訊息中遵循 **STD \_ 警示** 結構的固定長度資料指標。 |
| [**警示 \_ VAR \_ 資料**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | 傳回變數長度資料的指標，此資料會遵循警示訊息中的警示特定資料。   |



 

您可以使用 Windows Management Instrumentation (WMI) SDK 進行事件通知，而不是使用網路管理警示功能。 如需有關支援 WMI 事件模型之平臺的詳細資訊，請參閱 wmi 檔中的 [Wmi 基礎結構](/windows/desktop/WmiSdk/wmi-infrastructure) 和 [監視事件](/windows/desktop/WmiSdk/monitoring-events) 。

 

 