---
title: 產生錯誤資訊
description: 如果伺服器或應用程式在透過 RPC 呼叫時發生嚴重錯誤，則應該向 RPC 執行時間指出發生失敗，而且在理想情況下，應該加入失敗的相關資訊以協助進行疑難排解。
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7eb6868dfe11318e09b30217d5410a94ce32983ce64e75521c55fc5cc060ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020908"
---
# <a name="generating-error-information"></a>產生錯誤資訊

如果伺服器或應用程式在透過 RPC 呼叫時發生嚴重錯誤，則應該向 RPC 執行時間指出發生失敗，而且在理想情況下，應該加入失敗的相關資訊以協助進行疑難排解。

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>指出 RPC 執行時間發生嚴重錯誤

若要指出 RPC 執行時間失敗，請呼叫 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 函式，並在 rpc 執行緒上呼叫例外狀況，或在另一個執行緒上以非同步方式處理呼叫時呼叫 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) 。 從伺服器常式傳回錯誤碼（例如管理員常式）並不足夠-根據 RPC 規格，函式的傳回值在伺服器上沒有錯誤的語義，不論 idl/acf 檔案設定為何。

當您的元件發生嚴重錯誤時，請執行所述的任何清除，然後使用錯誤碼呼叫 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 函式。 **RpcRaiseException** 和傳回錯誤碼的唯一差異在於呼叫 **RpcRaiseException** 時，不會封送處理 out 參數。 這通常是一項優點，因為避免未初始化的參數變成不必要的。

## <a name="generating-additional-extended-error-information"></a>產生額外的延伸錯誤資訊

如同 RPC 執行時間建立一連串的錯誤記錄，您的伺服器或應用程式可以將自己的記錄新增至鏈。 這種方法通常有助於進行疑難排解程式。 例如，伺服器可能會嘗試開啟指定的檔案，並收到「找不到檔案」錯誤。 只要傳回錯誤2，就不會對判斷遺失的檔案有説明。

相反地，您的伺服器可能會呼叫 [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) 函式，並在錯誤記錄中提供字串參數（ANSI 或 Unicode），指出它所尋找之檔案的完整路徑。 當遠端電腦上的使用者畫面上出現這種資訊時，疑難排解就變得很簡單;可以完成檔案是否存在的簡單檢查，特別是因為 RPC 執行時間已經提供有問題的電腦名稱稱。

如果沒有足夠的記憶體可用， [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) 函數呼叫可能會失敗，即使它只需要幾個位元組的堆積空間也一樣。 此外， **RpcErrorAddRecord** 所加入的記錄會累積在指定的執行緒中。 執行時間通常會在呼叫您的伺服器常式之前清除這些記錄，但如果在 RPC 外部使用延伸的錯誤資訊，請呼叫 [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation)來處理線上程中累積累積的擴充錯誤。

 

 




