---
description: 您可以使用 Windows 的偵錯工具，來根據動態連結程式庫來進行自訂動作的偵錯工具。 您無法使用以可執行檔或腳本為基礎的自訂動作進行動態調試。
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: 自訂動作的調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781aaa5bfc8303175e7addfee730908c581575fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887017"
---
# <a name="debugging-custom-actions"></a>自訂動作的調試

您可以使用[Windows 的調試](https://www.microsoft.com/?ref=go)程式，來根據[動態連結程式庫](dynamic-link-libraries.md)來進行自訂動作的偵錯工具。 您無法使用以 [可執行檔](executable-files.md) 或 [腳本](scripts.md)為基礎的自訂動作進行動態調試。

本節所述的技術可協助您進行 Windows Installer 自訂動作的調試。 如需有關[Windows 之調試](https://www.microsoft.com/?ref=go)程式的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 的驅動程式開發工具一節。

Windows安裝程式會使用 MsiBreak 環境變數來判斷要進行調試的自訂動作。 如果您可以存取自訂動作的原始程式碼，您可以在不 MsiBreak 的情況下使用偵錯工具。 若要在不 MsiBreak 的情況下開始進行偵錯工具，請在動作程式碼的開頭放置一個暫時的訊息方塊。 在安裝期間出現訊息方塊時，將偵錯工具附加至擁有訊息方塊的進程。 然後，您可以設定任何必要的中斷點，並關閉訊息方塊以繼續執行。 您無法使用這個方法來將自訂動作的先前部分進行 debug 錯。

若要使用 MsiBreak 環境變數來對自訂動作進行自訂，請將 MsiBreak 設定為 [CustomAction 資料表](customaction-table.md)中自訂動作的名稱。 MsiBreak 可以是系統或使用者環境變數。 如果變數設定為系統變數，則當值變更為偵測新值時，可能需要重新開機系統。

若要使用 MsiBreak 環境變數來對內嵌使用者介面進行偵錯工具，請將 MsiBreak 的值設定為 MsiEmbeddedUI。

Windows如果使用者是系統管理員，則安裝程式只會檢查 MsiBreak 環境變數。 如果使用者不是系統管理員，則安裝程式會忽略 MsiBreak 的值，即使這是 [*受控應用程式*](m-gly.md)也一樣。

如果您要對執行順序中提高 (系統) 許可權執行的自訂動作進行偵錯工具，請將偵錯工具附加至 Windows Installer 服務。 當您在執行順序中對以模擬許可權執行的自訂動作進行偵錯工具時，系統會以對話方塊提示，指出應該調試的進程。 系統會以對話方塊提示使用者，指出要進行偵錯工具的進程。 如需更高的自訂動作的詳細資訊，請參閱 [自訂動作安全性](custom-action-security.md)。

當偵錯工具附加至正確的進程之後，安裝程式就會在呼叫 DLL 的進入點之前，立即觸發偵錯工具中斷點。 在中斷點，您的 DLL 已載入至進程，並已判斷進入點位址。 如果無法載入您的自訂動作 DLL 或自訂動作輸入點不存在，則不會觸發任何中斷點。 因為中斷點會在呼叫 DLL 函式之前觸發，所以在觸發中斷點之後，您應該使用偵錯工具向前復原，直到呼叫您的自訂動作進入點為止。 或者，您可以在自訂動作的任何位置設定中斷點，然後繼續正常執行。

Windows Installer 直接從 dll 位置執行未儲存在[二進位資料表](binary-table.md)中的 dll。 安裝程式不知道二進位資料表中所儲存之 DLL 的原始名稱，而是在暫存檔案名稱下執行 DLL 自訂動作。 暫存檔案名稱的形式為 MSI?????。TMP。 在 Windows XP 上，此暫存檔案儲存在安全的位置，通常是 &lt; WindowFolder &gt; \\ 安裝程式。

請注意，針對偵錯工具所建立的許多 Dll 都包含對應之 PDB 檔的名稱和路徑，做為 DLL 本身的一部分。 在可以在 DLL 儲存的位置找到 PDB 的系統上，對此類型的 DLL 進行偵錯工具時，偵錯工具工具可能會自動載入符號。 在無法于預存位置找到 PDB 的情況下，偵錯工具不支援從預存位置載入符號，或 DLL 未以偵錯工具建立的情況下，您可能需要使用暫存 DLL 檔將符號檔案放在資料夾中。

安裝程式會將自訂動作腳本的偵錯工具新增至安裝記錄檔。

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



