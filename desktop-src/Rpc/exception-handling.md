---
title: " (RPC) 的例外狀況處理"
description: RPC 使用與 Windows API 相同的例外狀況處理方式。
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b88cea6e1a2046b957baf5afe72be4cbec9f82d7da32215d2434fbf681f64d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080870"
---
# <a name="exception-handling-rpc"></a> (RPC) 的例外狀況處理

RPC 使用與 Windows API 相同的例外狀況處理方式。

[**RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))結構相當於 Windows 的 **try finally** 語句。 RPC 例外狀況結構 [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80))相當於 Windows 的 **try-except** 語句。

當您使用 RPC 例外狀況處理常式時，您的用戶端原始程式碼是可移植的。 針對每個平臺提供的不同 RPC 標頭檔會解析每個平臺的 **RpcTry** 和 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) 宏。 在 Windows 環境中，這些宏會直接對應至 Windows 的 **try-finally** 和 **try 以外** 的語句。 在其他環境中，這些宏會對應到其他平臺特定的例外狀況處理常式。

這些結構所引發的可能例外狀況包括由 RPC 函數所傳回的一組錯誤碼，其中包含前置詞 RPC \_ S \_ 和 rpc \_ X 以及 Windows 所傳回的例外狀況集。 如需詳細資訊，請參閱 [RPC 傳回值](rpc-return-values.md)。

雖然 **RpcTry** 和 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)宏提供可自訂的平臺中立方式來處理例外狀況，但在 Windows Vista 和更新版本的 Windows 中， [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)是處理例外狀況的建議方式。 不需要撰寫自訂篩選器來捕捉許多最常見的結構化例外狀況;不過，自訂例外狀況篩選準則仍然需要 **RpcExcept**。

伺服器應用程式、伺服器 stub 和伺服器執行時間程式庫中所發生的例外狀況， (傳輸層) 會傳播至用戶端。 從伺服器傳輸層級不會傳播任何例外狀況。 伺服器常式將錯誤傳回至 RPC 執行時間的建議方法是擲回例外狀況。 伺服器常式可以使用任何適當的方法來傳達伺服器常式之間的錯誤，但如果它遇到防止它執行遠端程式的錯誤，則在清除和傳回 RPC 執行時間之前，應該會引發例外狀況，而不是只將值傳回至只有伺服器常式辨識為錯誤的 RPC。

下圖顯示如何將例外狀況從伺服器傳回至用戶端。

![例外狀況是透過每個元件的各自 rpc 執行時間，從伺服器傳回至用戶端。](images/prog-a20.png)

RPC 例外狀況處理常式與開放式軟體 Foundation-Distributed 運算環境稍有不同， (憑證-DCE) 例外狀況處理宏 **TRY**、 **FINALLY** 和 **CATCH**。 各廠商提供將憑證-DCE rpc 函式對應至 Microsoft RPC 函數的 include 檔案，包括 **TRY**、 **catch**、 **catch** \_ **ALL** 和 **ENDTRY**。 這些標頭檔也會將 RPC \_ S 錯誤碼對應至 \_ \* 憑證-DCE 例外狀況對應項、rpc \_ s \_ \* ，然後將 rpc \_ x 錯誤碼對應 \_ \* 至 rpc \_ x \_ \* 。 針對憑證-DCE 可攜性，請使用這些 include 檔案。 如需 RPC 例外狀況處理常式的詳細資訊，請參閱 [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)、 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)、 [**RpcFinally**](/previous-versions/aa375699(v=vs.80))。 如需 Windows 例外狀況處理常式的詳細資訊，請參閱[結構化例外狀況處理](/windows/desktop/Debug/structured-exception-handling)。

 

 
