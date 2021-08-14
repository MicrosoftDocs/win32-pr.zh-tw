---
description: 延後執行自訂動作的目的是延遲系統變更執行安裝腳本的時間。
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: 延後執行自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cec06600fa2cdb447ace579ecf9d19be62e5f4824ecf2d34d77ed879a717d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379175"
---
# <a name="deferred-execution-custom-actions"></a>延後執行自訂動作

延後執行自訂動作的目的是延遲系統變更執行安裝腳本的時間。 這不同于一般自訂動作或標準動作，在此動作中，安裝程式會在序列資料表或 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)的呼叫中，立即執行動作。 延後執行自訂動作可讓封裝作者指定執行安裝腳本內特定點的系統作業。

安裝程式在處理安裝順序時，不會執行順延強制自訂動作。 相反地，安裝程式會將自訂動作寫入安裝腳本中。 唯一的模式參數是在此案例中，安裝程式所設定的 MSIRUNMODE \_ 排程。 如需執行模式參數的說明，請參閱 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 。

延後執行自訂動作必須在執行腳本產生之區段內的執行順序資料表中排程。 延後執行自訂動作必須在 [InstallInitialize](installinitialize-action.md) 之後，並且在動作順序中 [InstallFinalize](installfinalize-action.md) 之前。

設定屬性、功能狀態、元件狀態或目標目錄的自訂動作，或藉由將資料列插入至順序資料表來排程系統作業，在許多情況下都可以安全地使用立即執行。 不過，直接變更系統或呼叫另一個系統服務的自訂動作，必須延後至執行安裝腳本的時間。 如需其自訂動作和主要安裝執行緒之間可能發生衝突的詳細資訊，請參閱 [同步和非同步自訂動作](synchronous-and-asynchronous-custom-actions.md) 。

因為安裝腳本可以在寫入的安裝會話之外執行，所以在安裝腳本執行期間，會話可能不會再存在。 這表示，順延強制自訂動作無法使用安裝順序期間的原始會話控制碼和屬性資料集。 延遲的自訂動作會呼叫動態連結程式庫 (Dll) 傳遞控制碼，該控制碼只能用來取得非常有限的資訊，如 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)中所述。

請注意，延遲的自訂動作（包括 [復原自訂動作](rollback-custom-actions.md) 和 [認可自訂動作](commit-custom-actions.md)）是唯一可在使用者安全性內容外部執行的動作類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)
</dt> <dt>

[自訂動作參考](custom-action-reference.md)
</dt> </dl>

 

 



