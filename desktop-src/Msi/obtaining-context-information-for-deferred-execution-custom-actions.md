---
description: 因為安裝腳本可以在寫入的安裝會話之外執行，所以在安裝腳本執行期間，會話可能不會再存在。
ms.assetid: 13174c5d-c810-4b5d-9d1e-60ed30b8c44d
title: 取得順延強制自訂動作的內容資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cd956509a5b8a4c92e0a53bfa455154a59bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691435"
---
# <a name="obtaining-context-information-for-deferred-execution-custom-actions"></a>取得順延強制自訂動作的內容資訊

因為安裝腳本可以在寫入的安裝會話之外執行，所以在安裝腳本執行期間，會話可能不會再存在。 在此情況下，順延強制自訂動作無法使用安裝順序期間設定的原始會話控制碼和屬性。 任何需要會話控制碼的函式僅限於一些可抓取內容資訊的方法，或是在腳本執行期間所需的屬性必須寫入安裝腳本中。 例如，延遲的自訂動作會呼叫動態連結程式庫 (Dll) 傳遞控制碼，此控制碼只能用來取得數量非常有限的資訊。 不需要會話控制碼的函式可以從延遲的自訂動作中存取。

延後執行自訂動作僅限於呼叫需要控制碼的下列函式。



| 函式                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)       | 當搭配 [延後執行自訂動作](deferred-execution-custom-actions.md)使用時，支援一組有限的屬性： CustomActionData 屬性、 [**ProductCode**](productcode.md) 屬性和 [**UserSID**](usersid.md) 屬性。[Commit 自訂動作](commit-custom-actions.md) 無法使用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) 函式來取得 [**ProductCode**](productcode.md) 屬性。 認可自訂動作可以使用 CustomActionData 屬性來取得產品代碼。<br/> |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)     | 當搭配 [順延強制自訂動作](deferred-execution-custom-actions.md)使用時，支援一組有限的屬性： CustomActionData 和 ProductCode 屬性。                                                                                                                                                                                                                                                                                                                                                      |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)               | 從延後 [執行自訂動作](deferred-execution-custom-actions.md)中呼叫、 [認可自](commit-custom-actions.md)定義動作或 [回復自訂動作](rollback-custom-actions.md)時， [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 會在要求檢查模式參數時傳回 True 或 False MSIRUNMODE \_ 排程、MSIRUNMODE \_ 認可或 MSIRUNMODE \_ 復原。 從延後、認可或復原自訂動作檢查任何其他執行模式參數的要求會傳回 False。<br/>                       |
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)       | 目前產品的數位語言識別項。[Commit 自訂動作](commit-custom-actions.md) 無法使用 [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) 函數。 認可自訂動作可以使用 CustomActionData 屬性來取得數位語言識別項。<br/>                                                                                                                                                                                                                                                           |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) | 處理來自自訂動作的錯誤或進度訊息。                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話**](session-object.md) 物件。 這是 **Session 物件** 類型，而安裝程式會將它附加至名稱為 "Session" 的腳本。 因為 **會話** 物件在安裝復原期間可能不存在，所以以腳本撰寫的延遲自訂動作必須使用 **會話** 物件的下列其中一種方法或屬性來取出其內容。



| Name                                                           | 描述                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Mode 屬性**](session-mode.md)                          | 僅針對 MSIRUNMODE 排程傳回 True \_ 。                                                                                       |
| [**Property 屬性 (Session 物件)**](session-session.md)  | 傳回 CustomActionData 屬性、 [**ProductCode**](productcode.md) 屬性或 [**UserSID**](usersid.md) 屬性。        |
| [**Language 屬性 (Session 物件)**](session-language.md) | 傳回安裝會話的數位語言識別項。                                                                           |
| [**Message 方法**](session-message.md)                      | 呼叫以處理錯誤和進度。                                                                                              |
| [**安裝程式屬性**](session-installer.md)                | 傳回父物件，此物件用於非會話的函式，例如登錄存取和安裝程式設定管理。 |



 

在將安裝連續處理成腳本時所設定的屬性值，在腳本執行時可能無法使用。 在腳本執行期間，自訂動作一律可存取下列有限的屬性集。



| 屬性名稱                      | 描述                                                                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CustomActionData                   | 在順序資料表中處理自訂動作時的值。 CustomActionData 屬性僅適用于延後執行自訂動作。 立即自訂動作沒有這個屬性的存取權。 |
| [**ProductCode**](productcode.md) | 產品的唯一程式碼，也就是 [GUID](guid.md) 字串。                                                                                                                                                         |
| [**UserSID**](usersid.md)         | 由安裝程式設定為使用者的安全識別碼 (SID) 。                                                                                                                                                   |



 

如果延後執行自訂動作需要其他屬性資料，則其值必須儲存在安裝腳本中。 您可以使用第二個自訂動作來完成此動作。

**將屬性的值寫入安裝腳本，以便在延後執行自訂動作期間使用**

1.  將小型自訂動作插入安裝順序，將感興趣的屬性設定為具有和延後執行自訂動作相同名稱的屬性。 例如，如果延後執行自訂動作的主鍵為 "MyAction"，請將名為 "MyAction" 的屬性設定為您需要取出的屬性 X。 您必須在安裝順序中，于 "MyAction" 自訂動作之前設定 "MyAction" 屬性。 雖然任何類型的自訂動作都可以設定內容資料，但是最簡單的方法是使用屬性指派自訂動作 (例如 [自訂動作類型 51](custom-action-type-51.md)) 。
2.  在處理安裝順序時，安裝程式會將屬性 X 的值寫入執行腳本，做為屬性 CustomActionData 的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於屬性](about-properties.md)
</dt> <dt>

[使用屬性](using-properties.md)
</dt> <dt>

[屬性參考](property-reference.md)
</dt> </dl>

 

 




