---
title: 自動撥號連線作業
description: 當嘗試連線到網路位址失敗，因為無法連線到主機時，系統會在自動撥號對應資料庫中搜尋位址。
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150fa8542d1724be9d60f997db7952d6df387b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375504"
---
# <a name="autodial-connection-operations"></a>自動撥號連線作業

當嘗試連線到網路位址失敗，因為無法連線到主機時，系統會在自動撥號對應資料庫中搜尋位址。 如果位址是在資料庫中，系統就會起始與本機 TAPI 撥號位置對應的 [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85))（如果有的話）的自動撥號操作。

RAS API 提供的函式可讓您設定及查詢控制撥號連線的自動撥號參數。 您可以呼叫 [**RasSetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) 函數，以啟用或停用指定之 TAPI 撥號位置的自動撥號功能。 [**RasGetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea)函式會指出是否已針對指定的 TAPI 撥號位置啟用自動撥號功能。 如需有關 TAPI 撥號位置的詳細資訊，請參閱 TAPI 檔。 您可以呼叫 [**RasSetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) 函數來設定其他自動撥號連線參數。 例如，您可以停用目前登入會話的自動撥號連線。 呼叫 [**RasGetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) 函數來判斷自動撥號連線參數的目前值。

系統會為自動撥號作業提供預設的使用者介面。 不過，您可以建立 (DLL) 的自動撥號動態連結程式庫，以提供自訂的使用者介面，以進行與指定電話簿專案相關的自動撥號操作。 自動撥號 DLL 必須同時匯出 ANSI 和 Unicode 版本的 [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) 自動撥號處理常式。

若要為電話簿專案啟用自訂自動撥號處理常式，請呼叫 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 函式來設定該專案的屬性。 傳遞至 **RasSetEntryProperties** 的 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))結構的 **szAutodialDll** 和 **szAutodialFunc** 成員會指定自動撥號 DLL 的名稱和 [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)函式的名稱，但不包括 "A" 或 "W" 尾碼。

當系統針對具有自訂自動撥號處理常式的電話簿專案啟動自動撥號操作時，它會呼叫指定的 [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)。 **RASADFunc** 函式會接收 [**RASADPARAMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85))結構的指標，指出使用者介面視窗的位置和父視窗。 您的 **RASADFunc** 可以啟動執行緒來執行自訂撥號操作。 **RASADFunc** 函式會傳回 **TRUE** 以表示它接管撥號，或傳回 **FALSE** 以允許系統執行撥號。 您的自訂撥號操作必須使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式來執行實際的撥號。 當撥號作業完成時，自訂撥號作業會藉由設定傳遞至 [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)的 *lpdwRetCode* 參數所指向的變數來指出成功或失敗。

 

 