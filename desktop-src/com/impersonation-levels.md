---
title: " (COM) 的模擬層級"
description: 如果模擬成功，就表示用戶端已同意讓伺服器成為用戶端的程度。
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca691c89e7ff4a12e279ae0ecd0fd04cb31a951c8ac3f2671201fe99dd5900a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756388"
---
# <a name="impersonation-levels"></a>模擬層級

如果模擬成功，就表示用戶端已同意讓伺服器成為用戶端的程度。 不同程度的模擬稱為模擬 *層級*，而且會指出當伺服器模擬用戶端時，提供給伺服器的授權數量。

目前有四個模擬層級：*匿名*、*識別*、*模擬和**委派*。 下列清單簡要描述每個模擬等級：

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>匿名 (RPC \_ C \_ IMP \_ 層級 \_ 匿名) 
</dt> <dd>

用戶端對伺服器而言是匿名。 伺服器處理序可以模擬用戶端，但模擬語彙基元 (Token) 並不包含用戶端的任何資訊。 只有本機進程間的通訊傳輸才支援此層級。 所有其他傳輸都會以無訊息方式升級此層級來識別。

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>識別 (RPC \_ C \_ IMP \_ 等級 \_ 識別) 
</dt> <dd>

系統預設層級。 伺服器可以取得用戶端的識別 (Identity)，而且可以模擬用戶端來做 ACL 檢查。

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>模擬 (RPC \_ C \_ IMP \_ 層級模擬 \_) 
</dt> <dd>

伺服器代表用戶端動作時可以模擬用戶端的安全性內容。 伺服器可以像用戶端一樣存取本機資源。 如果伺服器在本機，則可以存取網路資源作為用戶端。 如果伺服器是遠端伺服器，則只能存取與伺服器位於同一部電腦上的資源。

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>委派 (RPC \_ C \_ IMP \_ 層級 \_ 委派) 
</dt> <dd>

功能最強大的模擬層級。 選取此層級時，伺服器 (不論本機或遠端) 代表用戶端動作時可以模擬用戶端的安全性內容。 在模擬期間， (本機和網路) 的用戶端認證可傳遞至任意數目的電腦。

若要讓模擬在委派層級運作，必須符合下列需求：

-   用戶端必須將模擬層級設定為 RPC \_ C \_ IMP \_ 層級 \_ 委派。
-   在 Active Directory 服務中，用戶端帳戶不得標示為「帳戶為機密，無法委派」。
-   伺服器帳戶必須標示 Active Directory 服務中的「受信任的委派」屬性。
-   裝載用戶端、伺服器和任何「下游」伺服器的電腦都必須在網域中執行。

</dd> </dl>

藉由選擇模擬等級，用戶端會向伺服器告知模擬用戶端的進度。 用戶端會在用來與伺服器通訊的 proxy 上設定模擬等級。

## <a name="setting-the-impersonation-level"></a>設定模擬等級

有兩種方式可以設定模擬等級：

-   用戶端可以透過呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來設定 processwide。
-   用戶端可以透過呼叫 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (或 Helper 函數 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)) ，在遠端物件的介面上設定 proxy 層級安全性。

您可以透過 DwImpLevel 參數傳遞適當的 RPC \_ C \_ IMP \_ level \_ xxx 值給 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)或 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)  ，藉以設定模擬等級。

不同的驗證服務支援委派層級的模擬至不同的範圍。 例如，NTLMSSP 支援跨執行緒和跨進程的委派層級模擬，但不支援跨電腦。 另一方面，Kerberos 通訊協定支援跨電腦界限的委派層級模擬，而 Schannel 則不支援在委派層級進行任何模擬。 如果您在模擬層級擁有 proxy，而且想要將模擬層級設定為委派，則應該使用每個參數的預設常數來呼叫 [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) ，但模擬等級除外。 COM 會在本機選擇 NTLM 和 Kerberos 通訊協定，當 Kerberos 通訊協定) 時，會從遠端 (。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[委派和模擬](delegation-and-impersonation.md)
</dt> </dl>

 

 