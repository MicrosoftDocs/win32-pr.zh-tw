---
description: WriteEnvironmentStrings 動作會修改環境變數的值。
ms.assetid: a91c1ffe-1bdd-49bb-aa6a-71667a1ed812
title: WriteEnvironmentStrings 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a9d64a1140fc883d94e8d3733608d29dc2d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026982"
---
# <a name="writeenvironmentstrings-action"></a>WriteEnvironmentStrings 動作

WriteEnvironmentStrings 動作會修改環境變數的值。

執行 WriteEnvironmentStrings 動作或 [RemoveEnvironmentStrings 動作](removeenvironmentstrings-action.md) 時，不會變更環境變數以進行安裝。 在 Windows 2000、Windows Server 2003、Windows XP 和 Windows Vista 上，這項資訊會儲存在登錄中，並傳送 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) 訊息，以在安裝完成時通知系統變更。 另一個進程可以藉由處理這些訊息來接收變更的通知。 如果系統重新開機已暫止，則不會傳送任何訊息。 封裝可以使用 [**MsiSystemRebootPending**](msisystemrebootpending.md) 屬性來檢查系統重新開機是否暫止。

安裝程式只會在安裝或重新安裝元件期間執行 WriteEnvironmentStrings 動作，而且只會在移除元件期間執行 [RemoveEnvironmentStrings 動作](removeenvironmentstrings-action.md) 。

系統會根據選取的主要動作和修飾詞來寫入或移除值。 下列 ActionData 訊息章節將說明這些情況。 請注意，根據指定的動作而定，WriteEnvironmentStrings 可能會移除變數，而 RemoveEnvironmentStrings 可以根據 [環境資料表](environment-table.md)的編寫來加入這些變數。

## <a name="sequence-restrictions"></a>順序限制

[InstallValidate 動作](installvalidate-action.md)必須在 RemoveEnvironmentStrings 動作之前執行。 因為 WriteEnvironmentStrings 動作和 RemoveEnvironmentStrings 動作絕不會在安裝或移除元件期間套用，所以不會限制它們的相對順序。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                                                                                                                                                                                                  |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | 要修改的環境變數名稱。                                                                                                                                                                                 |
| \[2\] | 環境變數值。                                                                                                                                                                                             |
| \[3\] | 這是位旗標的欄位，可指定要執行的動作。 主要動作只包含一個位。 此欄位中可能包含一個以上的修飾詞位。 請參閱下列位旗標描述。 |



 



| 位值 | 主要動作的描述                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1       | 設定。 在所有情況下設定環境變數的值。<br/> 如果這個位結合了附加或前置詞修飾詞位，此動作會將值加入至變數中的任何現有值。<br/> |
| 0x2       | 設定。 如果變數不存在，則設定該值。<br/> 如果這個位結合了附加或前置詞修飾詞位，此動作會將值加入至變數中的任何現有值。<br/>                |
| 0x4       | 移除。 從變數中移除值。<br/> 如果這個位結合了附加或前置詞修飾詞，則會從現有字串中移除值（如果值存在的話）。<br/>               |



 



| 位值  | 修飾詞的描述                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x20000000 | 如果設定此位，則會將動作套用至電腦環境變數。<br/> 如果未設定此位，則會將動作套用至使用者的環境變數。<br/> |
| 0x40000000 | Append。 這位是選擇性的。 請勿同時設定 Append 和 Prefix 修飾詞。<br/>                                                                                            |
| 0x80000000 | 首碼。 這位是選擇性的。 請勿同時設定 Append 和 Prefix 修飾詞。<br/>                                                                                            |



 

 

 
