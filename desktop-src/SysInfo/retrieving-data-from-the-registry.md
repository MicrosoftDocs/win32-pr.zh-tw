---
description: 若要從登錄取出資料，應用程式通常會列舉金鑰的子機碼，直到它找到特定的子機碼，然後從與其相關聯的值取得資料。
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: 從登錄中取出資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bedbe0631015188a8a9fe280ba17d929c83663e995f440f4528c0913fc69cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763477"
---
# <a name="retrieving-data-from-the-registry"></a>從登錄中取出資料

若要從登錄取出資料，應用程式通常會列舉金鑰的子機碼，直到它找到特定的子機碼，然後從與其相關聯的值取得資料。 應用程式可以呼叫 [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) 函式來列舉指定機碼的子機碼。

若要取得特定子機碼的詳細資料，應用程式可以呼叫 [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) 函數。 [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)函式會捕獲保護金鑰的安全描述項複本。

應用程式可以使用 [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) 函式來列舉指定索引鍵的值，並使用 [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) 函式來取得索引鍵的特定值。 應用程式通常會呼叫 **RegEnumValue** 來判斷值名稱，然後 **RegQueryValueEx** 來取得名稱的資料。

[**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)函式會抓取與開啟登錄機碼相關聯之值名稱清單的類型和資料。 此函數對動態金鑰提供者很有用，因為它會在不可部分完成的作業中抓取多個值，以確保資料的一致性。

由於其他應用程式可以在您的應用程式可以讀取值和使用它的時間之間變更登錄值中的資料，因此您可能需要確定您的應用程式具有最新的資料。 當登錄機碼的屬性或內容有所變更，或刪除金鑰時，您可以使用 [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) 函式來通知呼叫的執行緒。 此函式會通知事件物件以通知呼叫者。 如果呼叫 **RegNotifyChangeKeyValue** 的執行緒結束，則會將事件發出信號，並停止監視登錄機碼。

您可以透過使用通知篩選或旗標來控制或指定應該報告的變更。 通常，藉由對您指定給函式的事件發出信號來回報變更。 請注意， [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) 函式無法用於遠端控制碼。

若要更詳細地監視登錄作業，請參閱 [**registry**](/windows/desktop/ETW/registry)。

 

 
