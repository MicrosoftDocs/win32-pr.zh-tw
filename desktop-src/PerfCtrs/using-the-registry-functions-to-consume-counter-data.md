---
description: 您可以使用登錄功能來收集效能資料。
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: 使用登錄函式來使用計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 69f64f6e4cb44dd98d4f5097ca791054cd04c7e07219dc0e270cbfdff4cdbdc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033118"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>使用登錄函式來使用計數器資料

使用登錄[](/windows/desktop/SysInfo/registry-functions)函式從特殊登錄機碼收集效能資料 `HKEY_PERFORMANCE_DATA` 。

效能資料實際上不會儲存在登錄中。 呼叫登錄函數會導致系統從適當的效能資料提供者收集資料。

> [!Note]
> 您通常不應該使用登錄功能來使用計數器資料。 相反地，您應該 [使用效能資料協助程式 (PDH) 函數](using-the-pdh-functions-to-consume-counter-data.md)。 PDH 函式更容易使用，並可避免因為登錄功能不當使用而發生的許多效能和可靠性問題。

> [!Note]
> 如果您要撰寫 Windows OneCore 的應用程式，則無法使用登錄功能。 相反地，請使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式。

登錄功能是用來從 **V1 提供者** 收集資料的低層級 API。 登錄函式也支援透過呼叫 [v2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式的轉譯層，從 **V2 提供者** 收集資料。

若要從本機系統取得效能資料，請呼叫 [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) 函數。 使用 `HKEY_PERFORMANCE_DATA` 作為索引鍵。 第一個呼叫會開啟金鑰。 您不需要明確地先開啟金鑰。

若要從遠端系統取得效能資料，請呼叫 [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) 函數。 使用遠端系統的電腦名稱稱，並使用 `HKEY_PERFORMANCE_DATA` 做為金鑰。 此呼叫會抓取代表遠端系統效能資料的索引鍵。 您可以使用此金鑰來取得資料，而不是使用 `HKEY_PERFORMANCE_DATA` 金鑰。

當您完成效能資料的取得時，請務必使用 [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) 函式來關閉索引鍵的控制碼。 這對本機和遠端案例而言很重要：

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` 實際上並不會關閉登錄控制碼，但會清除所有快取的資料，並釋放載入的效能 Dll。
- `RegCloseKey(hkeyRemotePerformanceData)` 關閉遠端電腦登錄的控制碼。

> [!IMPORTANT]
> 請勿 `RegCloseKey(HKEY_PERFORMANCE_DATA)` 在期間呼叫 `DLL_PROCESS_DETACH` 。

您可以使用 `lpValueName` [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) 函數的參數來指出要取出的資訊。 下表列出您可以為指定的值 `lpValueName` 。 請注意，值字串不區分大小寫。

|值|描述
|-----|-----------
|`Global`| 抓取電腦上註冊之所有效能物件的效能資料，但類別中所包含的物件除外 `Costly` 。
|`OLD_Global`| **Windows Vista 和更新版本：** 抓取電腦上註冊之所有 **V1** 效能物件的效能資料，但類別中所包含的物件除外 `Costly` 。 `Global`當您知道感興趣的資料來自 V1 提供者時，請使用此取代來避免收集不必要的 V2 提供者資料。
|`n1 n2 ...`| 抓取一或多個效能物件的效能資料。 在以空格分隔的清單中，指定與您想要取得之每個物件相關聯的十進位索引。 例如，如果您想要取出系統和記憶體物件，並判斷對應的名稱字串的索引為2和4，請指定字串 `"2 4"` 。 請注意，查詢所傳回的物件數目可能會與您所要求的數目不同。 如果指定的物件相依于另一個物件類型，或者如果提供者傳回未直接要求的資料，就會發生這種情況。 例如，執行緒相依于處理常式，因此如果您要求物件中的資料 `Thread` ，結果會包含來自物件的資料 `Process` 。
|`Counter n`| 抓取指定語言識別項的名稱字串，例如的英文 `Counter 9` 。 使用傳回的名稱字串來尋找對應到指定名稱的索引，或尋找對應至指定索引的名稱。 如需詳細資訊，請參閱取得 [計數器名稱和解說文字](retrieving-counter-names-and-help-text.md) 。 請注意，傳回的清單同時包含物件 (counterset) 名稱和計數器名稱--沒有簡單的方法可判斷名稱是否為物件名稱或計數器名稱。
|`Help n`| 針對指定的語言識別項（例如英文）抓取說明 `Help 9` 字串。 使用傳回的說明字串來尋找對應至物件 (counterset) 或計數器說明索引的描述。 如需詳細資訊，請參閱取得 [計數器名稱和解說文字](retrieving-counter-names-and-help-text.md) 。
|`Costly`| 已 **淘汰：** 取得物件類型的效能資料，而這些物件的資料在處理器時間或記憶體使用量方面都很耗費資源收集。 此集合可能需要幾分鐘的時間，才會在大量載入的機器上執行。 如果您的應用程式需要在此資料收集期間回應使用者，您應該在背景工作執行緒上執行集合。

如需登錄所傳回之效能資料格式的詳細資訊，請參閱 [效能資料格式](performance-data-format.md)。

如需取得電腦上已註冊之計數器的名稱和描述的範例，請參閱抓取 [計數器名稱和解說文字](retrieving-counter-names-and-help-text.md)。

如需存取效能資料之元件的範例，請參閱 [顯示物件、實例和計數器名稱](displaying-object-instance-and-counter-names.md)。

如需抓取、計算和列印計數器值的範例，請參閱抓取 [計數器資料](retrieving-counter-data.md) 和 [計算計數器值](calculating-counter-values.md)。
