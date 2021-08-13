---
description: Nondeferred 呼叫動態連結程式庫或腳本的自訂動作，可能會存取執行中的安裝，以查詢或修改目前安裝會話的屬性。
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: 從自訂動作內部存取目前的安裝程式會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ee3214b8f8664b57f5216b28a7f5d5269d76049fe5c4dd24f7ab8d130d89a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640187"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>從自訂動作內部存取目前的安裝程式會話

Nondeferred 呼叫 [動態連結程式庫](dynamic-link-libraries.md) 或 [腳本](scripts.md) 的自訂動作，可能會存取執行中的安裝，以查詢或修改目前安裝會話的屬性。 每個進程只能有一個 **會話** 物件，而且自訂動作腳本不能嘗試建立另一個會話。

自訂動作只能加入、修改或移除資料庫中的暫存資料列、資料行或資料表。 自訂動作無法修改資料庫中的持續性資料，例如，儲存在磁片上之資料庫的資料。

[動態連結程式庫](dynamic-link-libraries.md)

若要存取執行中的安裝，呼叫動態連結程式庫 (DLL) 的自訂動作會傳遞給目前會話的型別 MSIHANDLE 控制碼，作為 [CustomAction 資料表](customaction-table.md)的目標資料行中所指定之 DLL 進入點的唯一引數。 因為安裝程式提供此控制碼，所以自訂動作不應該關閉它，例如，若要從安裝程式接收控制碼 *hInstall* ，自訂動作函式的宣告方式如下。


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



若要取得目前資料庫的唯讀存取權，請呼叫 [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)來取得資料庫控制碼。 如需詳細資訊，請參閱 [取得資料庫控制碼](obtaining-a-database-handle.md)。

[指令碼](scripts.md)

以 VBScript 或 JScript 撰寫的自訂動作可使用 [**session 物件**](session-object.md)存取目前的安裝會話。 安裝程式會建立名為「會話」的 **會話** 物件，該物件會參考目前的安裝。 若為目前資料庫的唯讀存取權，請使用 **Session** 物件的 [**database**](session-database.md)屬性。

因為腳本是從 [**會話**](session-object.md) 物件的內容中執行，所以並不一定需要完整限定屬性和方法。 在下列範例中，使用 VBScript 時，我的參考可以取代 **會話** 物件，例如，下列三行是相等的。


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[可執行檔](executable-files.md)

您無法從呼叫以命令列啟動之可執行檔的自訂動作（例如， [自訂動作類型 2](custom-action-type-2.md) 和 [自訂動作類型 18](custom-action-type-18.md)）存取目前的安裝程式會話。

[延後執行自訂動作](deferred-execution-custom-actions.md)

您無法從順延強制自訂動作存取目前的安裝程式會話或所有屬性資料。 如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從自訂動作內部存取資料庫或會話](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



