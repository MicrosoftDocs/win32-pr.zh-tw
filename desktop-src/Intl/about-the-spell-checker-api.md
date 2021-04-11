---
description: 針對全球使用者，文字輸入是新式運算體驗的一部分，適用于博客、批註、tweet、立即訊息，或任何其他類型的文字類型。 在 Windows 8 中，已內建編輯控制項的拼寫檢查。
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: 關於拼寫檢查 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850259"
---
# <a name="about-the-spell-checking-api"></a>關於拼寫檢查 API

針對全球使用者，文字輸入是新式運算體驗的一部分，適用于博客、批註、tweet、立即訊息，或任何其他類型的文字類型。 在 Windows 8 中，已內建編輯控制項的拼寫檢查。

開發人員可以在其應用程式中使用拼寫檢查 API，以使用可用的拼寫檢查服務。 開發人員也可以建立可成為提供者的拼寫檢查，並整合到 Windows 拼寫檢查架構中。

拼寫檢查 API 的設計目的是要讓 Windows 元件物件模型的專業 C/c + + 開發人員使用 (COM) 應用程式。 在 Windows 或 ASP.NET 服務中不支援使用拼寫檢查 API。

## <a name="versioning"></a>版本控制

從 Windows 8 或 Windows Server 2012 開始，可以使用拼寫檢查 API。 API 的未來新增將會藉由建立新介面來處理，而這些介面可使用現有的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來決定。

## <a name="interfaces"></a>介面

所有介面都必須在不再使用時釋放。 所有傳回的 (out 參數) **LPWSTR** 字串 (和 [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) 的 **LPOLESTR** 專案都必須在不再使用 CoTaskMemFree 時，與 [](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)一起釋放。

## <a name="error-handling"></a>錯誤處理

錯誤會以 **HRESULT** s 傳回。 此 API 不支援 [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)和 [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) 。 除了不正確的引數之外，錯誤並不是特別可採取動作。

任何 API 呼叫可能會傳回標準 RPC 錯誤碼，因為它們是跨進程。 標準 RPC 超時適用。

## <a name="security"></a>安全性

拼寫檢查 API 可能會)  (的拼寫檢查提供者載入外部程式碼。 它會在進程外執行此程式碼，並在受限制的安全性內容下執行。

## <a name="dictionary-files"></a>字典檔

語言的使用者專屬詞典（包含新增、排除和自動換行清單的內容）位於% AppData% \\ Microsoft \\ 拼寫下 \\ *<language tag>* 。 檔案名是預設值。 scripting.dic (新增) ，專有 (排除) 和預設值。 acl (自動校正) 。 這些檔案是 UTF-16 LE 純文字，必須以適當的位元組順序標記 (BOM) 來開頭。 每一行都包含新增和排除的字組清單中的單字 () ，或自動校正字組（以分隔號分隔的單字） ( " \| " )  (在 [自動校正字組] 清單) 中。 目錄中的 scripting.dic、. 專有和 acl 檔案將會由拼寫檢查服務偵測，並新增至使用者字組清單。 這些檔案會被視為唯讀，且不會由拼寫檢查 API 修改。

## <a name="installing-a-spell-checking-provider"></a>安裝拼寫檢查提供者

安裝拼寫檢查提供者時，必須將它所使用的所有檔案都放在允許從 SID ([安全識別碼](../secauthz/security-identifiers.md)) 「所有應用程式封裝」中讀取權限的位置。 將它安裝在 [Program Files] 下的資料夾也可以正常運作。 此外，提供者必須在登錄中設定一些索引鍵，才能讓它出現在拼寫檢查 API 中。 它可以位於 HKEY \_ CURRENT \_ user HIVE 或 HKEY \_ 本機電腦 hive 中， \_ 取決於它是否應該僅針對目前的使用者或所有使用者進行安裝。


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



[拼寫檢查提供者範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)提供安裝提供者所需的註冊範例。

如果您要為拼寫檢查提供者建立新的拼寫檢查選項，請參閱 [**IOptionDescription：： Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) 以取得命名指引。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[拼寫檢查 API 參考](spell-checker-api-reference.md)
</dt> <dt>

[拼寫檢查用戶端範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[拼寫檢查提供者範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription：： Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
