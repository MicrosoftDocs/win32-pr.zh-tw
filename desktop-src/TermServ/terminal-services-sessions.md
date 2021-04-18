---
title: 遠端桌面會話
description: 因為每次登入遠端桌面連線 (RDC) 用戶端會收到個別的會話識別碼，所以使用者體驗類似于同時登入多部電腦;例如，辦公室電腦和家用電腦。
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb99f9745e382bdff1099eabae9a8e8ef0b8333
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966250"
---
# <a name="remote-desktop-sessions"></a>遠端桌面會話

當使用者登入已啟用遠端桌面服務的電腦時，就會啟動使用者的會話。 每個會話都是由唯一的會話識別碼所識別。 因為每次登入遠端桌面連線 (RDC) 用戶端會收到個別的會話識別碼，所以使用者體驗類似于同時登入多部電腦;例如，辦公室電腦和家用電腦。

每個遠端桌面會話都與互動式視窗工作站相關聯。 互動式視窗工作站唯一支援的 windows 工作站名稱為 "WinSta0";因此，每個會話都會與它自己的「WinSta0」視窗站產生關聯。 每個視窗工作站都有三個標準桌面： Winlogon desktop、螢幕保護裝置桌面和互動式桌面。

與會話的互動式視窗工作站相關聯的使用者，就是所謂的 *互動式使用者*。 在遠端桌面連線 (RDC) 用戶端上，除了遠端桌面服務主控台的互動式使用者之外，也可以有多個互動式使用者。 若要取得目前附加至主控台之會話的識別碼，請使用 [**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) 函式。

當使用者登出遠端桌面連線 (RDC) 用戶端時，系統會刪除用戶端在遠端桌面工作階段主機 (RD 工作階段主機)  (伺服器上的會話，) 先前稱為終端機伺服器，並移除與該會話相關聯的視窗和桌面。 不過，由於不會刪除遠端桌面服務主控台會話，因此不會刪除與主控台會話相關聯的視窗工作站。 這會影響當應用程式設定為在互動式使用者的安全性內容（也稱為「RunAs 互動式使用者」物件啟用模式）中執行時，在遠端桌面服務環境中的行為。

如需有關在指定的會話上啟動本機伺服器進程的詳細資訊，請參閱 [使用會話標記的會話對會話啟用](session-to-session-activation-with-a-session-moniker.md) 和 [使用會話的標記](using-a-session-moniker.md)。 如需安全性環境的詳細資訊，請參閱 [用戶端的安全性內容](/windows/desktop/SecAuthZ/the-client-security-context)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[子會話](child-sessions.md)
</dt> </dl>

 

 