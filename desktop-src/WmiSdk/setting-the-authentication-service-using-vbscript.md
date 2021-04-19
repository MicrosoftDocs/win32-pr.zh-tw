---
description: 使用腳本存取 Windows Management Instrumentation (WMI) server 時，您可以選擇 NT LAN Manager (NTLM) 或 Kerberos 驗證通訊協定。
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: 使用 VBScript 設定驗證服務
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975933"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>使用 VBScript 設定驗證服務

使用腳本存取 Windows Management Instrumentation (WMI) server 時，您可以選擇 NT LAN Manager (NTLM) 或 Kerberos 驗證通訊協定。 除非使用委派，否則不需要指定 Kerberos。 如需詳細資訊，請參閱 [連接到第3部電腦委派](connecting-to-a-3rd-computer-delegation.md)。

因為作業系統版本的不同之處在于其使用的驗證服務，所以建議您不要在連接到遠端系統時指定 [授權單位] 欄位的值。 相反地，請允許作業系統和分散式版本的元件物件模型 (DCOM) 來選取 NTLM 或 Kerberos。 如果指定了驗證服務，則語法需要伺服器主體名稱，也就是目的電腦的名稱，而不是網域控制站。

您只能將授權參數用於遠端 WMI 伺服器的連接。 如果您嘗試將授權層級設定為標記的一部分，或呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 以進行本機連接，連接嘗試就會失敗。

請執行下列程式，以指定您要在 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)方法的 *strAuthority* 參數中使用的驗證服務，或使用 [標記](constructing-a-moniker-string.md)字串連接。

**使用適用于 WMI 的腳本 API 來指定 NTLM 或 Kerberos 驗證**

1.  如果 *strAuthority* 參數的開頭是 "kerberos：" 字串，WMI 會假設字串參考 kerberos 主體名稱，並使用 kerberos 驗證。 如果 *strAuthority* 參數的開頭為 "ntlmdomain：" 字串，WMI 會改為使用 NTLM 驗證。
2.  或者，您可以使用 [部分] 的 [授權單位] 來指定用來連線到 WMI 的驗證類型。 若要在使用標記時使用 Kerberos 驗證，請包含字串 "核證 = Kerberos："，後面接著主體名稱。 若要使用 NTLM 驗證，請包含字串 "核證 = ntlmdomain："，後面接著 NTLM 功能變數名稱。

    下列範例會顯示使用主體 "mydomain server" 要求 Kerberos 驗證的標記 \\ 。

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    相反地，下列範例會顯示使用「mydomain」網域要求 NTLM 驗證的標記。

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



