---
description: 疑難排解
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: 疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972774"
---
# <a name="troubleshooting"></a>疑難排解

如果您在診斷應用程式錯誤時遇到問題，請參閱下列疑難排解秘訣：

-   確定分散式交易協調器 (DTC) 正在所有伺服器上執行。
-   先在本機電腦上測試以確認應用程式可運作，以檢查網路通訊。 如果您在網路上執行 TCP/IP，則可以使用 ping.exe 公用程式來確認電腦是否在網路上。
-   請確定 SQL 和 DTC 位於相同的電腦上，或者 DTC 用戶端設定程式指定 DTC 位於另一部電腦上。 如果沒有，SQLConnect 會在從交易元件呼叫時，從內部傳回錯誤。
-   將交易超時設定為比預設60秒更高的數位。 交易超時經過之後，COM + 會中止交易。 元件的所有後續呼叫都會立即傳回，內容 \_ E 會 \_ 中止。
-   確定您的 ODBC 驅動程式是安全線程，而且沒有線程親和性。
-   如果您無法讓應用程式在數部伺服器上運作，請重新開機用戶端，然後確認您的網域控制站已正確設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錯誤隔離和 Failfast 原則](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[找出錯誤的來源](finding-the-source-of-an-error.md)
</dt> <dt>

[COM + 如何修改傳回值](how-com--modifies-return-values.md)
</dt> <dt>

[解讀錯誤碼](interpreting-error-codes.md)
</dt> <dt>

[在 COM + 中處理錯誤的策略](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



