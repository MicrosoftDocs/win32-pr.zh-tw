---
description: 下表列出用來滿足範例規格的五個自訂動作： ProcessAccounts、UninstallAccounts、CreateAccounts、RemoveAccounts 和 RollbackAccounts。
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: 撰寫自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6880f95b0468a495653057a9a5802af671c55b18b025c38a3191a4792e7558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381173"
---
# <a name="authoring-the-custom-actions"></a>撰寫自訂動作

下表列出用來滿足範例規格的五個自訂動作： ProcessAccounts、UninstallAccounts、CreateAccounts、RemoveAccounts 和 RollbackAccounts。 所有這些自訂動作都位於[二進位資料表](binary-table.md)中所儲存的[動態連結程式庫](dynamic-link-libraries.md)中。 Windows Installer SDK 提供包含範例自訂動作之動態連結程式庫的 c + + 原始程式碼。 ProcessAccounts 和 UninstallAccounts 位於檔案處理常式 .cpp 中。 CreateAccount 位於 file Create .cpp 中。 RemoveAccount 和 RollbackAccount 位於檔案 Remove 中。 這些來源檔案可以用來建立檔案 Process.dll、Create.dll 和 Remove.dll。

由於建立或移除使用者帳戶需要較高的許可權，因此必須使用在系統內容中執行的 [延後執行自訂動作](deferred-execution-custom-actions.md) 來建立、移除或復原使用者帳戶。 立即執行自訂動作（ProcessAccounts 和 UninstallAccounts）會產生延遲的自訂動作，以建立、移除或復原使用者帳戶： CreateAccount、RemoveAccount 和 RollbackAccount。

由於延後自訂動作無法讀取資料庫資料表中的資訊，因此 ProcessAccounts 和 UninstallUserAccouts 必須設定 CustomActionData 屬性，將 UserAccounts 資料表中的資訊傳遞給延遲的自訂動作，如 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)中所述。 當安裝程式執行執行腳本時，延後的自訂動作會根據 CustomActionData 屬性中的資訊來處理使用者帳戶。

因為所有自訂動作都是在二進位資料表中儲存的動態連結程式庫中，所以它們全都會在其基底數數值型別中包含常數 msidbCustomActionTypeDll 和 msidbCustomActionTypeBinaryData。 ProcessAccounts 和 UninstallAccounts 是純 [自訂動作類型 1](custom-action-type-1.md)的範例。 如需其他自訂動作類型的詳細資訊，請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md)。

CreateAccount 和 RemoveAccount 是 [延後執行的自訂動作](deferred-execution-custom-actions.md) ，不允許服務模擬特定的使用者。 這些自訂動作包括常數 msidbCustomActionTypeInScript 和 msidbCustomActionTypeNoImpersonate，以指定這些 [自訂動作的腳本執行選項](custom-action-in-script-execution-options.md)。

RollbackAccount 是 [復原自訂動作](rollback-custom-actions.md) ，只會在 [復原安裝](rollback-installation.md)期間移除使用者帳戶。 RollbackAccount 包含常數 msidbCustomActionTypeInScript 和 msidbCustomActionTypeRollback，以指定這些 [自訂動作的腳本執行選項](custom-action-in-script-execution-options.md)。

這些自訂動作可能會處理敏感性資料，例如不應寫入記錄檔的使用者密碼。 因此，延遲的自訂動作應該會在自訂動作類型中包含 msidbCustomActionTypeHideTarget。 延後自訂動作的名稱也必須加入至 [屬性工作表](property-table.md)中的 [**MsiHiddenProperties**](msihiddenproperties.md)屬性清單，因為立即的自訂動作會使用 CustomActionData 屬性，將資料傳遞至延遲的自訂動作。



| 自訂動作     | DLL 進入點                       | 自訂動作類型                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProcessAccounts   | Process.dll 中的 ProcessUserAccounts。   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | Process.dll 中的 UninstallUserAccounts。 | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | Create.dll 中的 CreateUserAccount。      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265。 |
| RemoveAccount     | Remove.dll 中的 RemoveUserAccount。      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265。 |
| RollbackAccount   | Remove.dll 中的 RemoveUserAccount。      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473。       |



 

繼續 [撰寫 CustomAction 資料表](authoring-the-customaction-table.md)。

 

 



