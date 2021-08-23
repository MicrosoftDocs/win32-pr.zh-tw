---
title: 驗證通訊協定初始化
description: 在用戶端與伺服器之間，以 RAS 和無線 (802.1 X) 用戶端的相同方式初始化 EAP 安全連線。
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d53643718f747e1f39aaf68393f92a0577455041ec765ca19bea710f2c3aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984458"
---
# <a name="authentication-protocol-initialization"></a>驗證通訊協定初始化

在用戶端與伺服器之間，以 RAS 和無線 (802.1 X) 用戶端的相同方式初始化 EAP 安全連線。

## <a name="client"></a>用戶端

當用戶端嘗試建立連接時，驗證服務會取得使用者的身分 [識別資訊](obtaining-identity-information.md) 。 如果這個驗證通訊協定的登錄中有 **RAS \_ EAP \_ VALUENAME \_ INVOKE \_ NAMEDLG** 值，而且此值設定為零，則驗證服務會呼叫 [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)。 此函式通常會顯示使用者介面，讓身分識別資訊成為驗證通訊協定的特定類型;例如，憑證或數位識別碼。 如果 **RAS \_ EAP \_ VALUENAME \_ INVOKE \_** 叫用 NAMEDLG 不存在，或設定為1，則驗證服務會顯示標準系統使用者名稱對話方塊。

一旦驗證服務取得使用者的身分識別資訊，它就會呼叫 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))的驗證通訊協定的執行。 此呼叫可讓驗證通訊協定配置和初始化工作緩衝區，讓服務在後續呼叫 [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) 和 [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85))時傳遞。 工作緩衝區對服務而言是不透明的，而且永遠不會存取工作緩衝區的內容。 如果驗證通訊協定為每個 EAP 會話建立不同的工作緩衝區，則工作緩衝區會是會話和安全線程。 由於驗證通訊協定會配置工作緩衝區的記憶體，因此驗證通訊協定也應使用 [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) 函式釋放這個記憶體。

在 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))的呼叫中，服務也會傳遞 [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) 結構，其中包含連線設定資訊的指標，以及使用者的身分識別資訊。 服務一律會傳入 **PPP \_ EAP \_ 輸入** 之 **pszIdentity** 成員的值。 不過， [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)的 **pszPassword** 成員可以是 **Null**。

在 [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) 結構內， **fAuthenticator** 成員會指出是否要叫用驗證通訊協定，以在用戶端) 上進行驗證 (，或做為伺服器) 上的驗證器 (。

## <a name="server"></a>伺服器

在伺服器上， [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)的 **bInitialID** 成員會指定伺服器用於第一個 EAP 封包的識別碼。 伺服器會針對後續的封包遞增此識別碼。

此外，在伺服器上， [**PPP \_ EAP \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)中的 **pUserAttributes** 指標會指向 [**RAS \_ AUTH \_ 屬性 \_ 類型**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type)類型的屬性陣列。 這些是從用戶端取得之使用者的屬性。

如果 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) 呼叫傳回任何 **不是 \_ 錯誤** 的值，會話就會中斷連線。 傳回的錯誤會記錄在伺服器) 上 (，或顯示給用戶端) 上的使用者 (。

 

 