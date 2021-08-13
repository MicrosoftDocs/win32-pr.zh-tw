---
title: 服務帳戶和 BITS
description: 您可以使用 BITS 從服務傳輸檔案。 服務必須使用 LocalSystem、LocalService 或 NetworkService 系統帳戶。 這些帳戶一律會登入;因此，使用這些帳戶的服務所提交的作業一律會執行。
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- 服務帳戶位
- 傳送作業位、擁有權、服務帳戶
- proxy 位，服務帳戶
- 傳送工作 BITS 的認證
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: a996471afefb00b0dea87b07f477f5cab2fd29352c567dc9182fcf28fa5b168a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679900"
---
# <a name="service-accounts-and-bits"></a>服務帳戶和 BITS

您可以使用 BITS 從服務傳輸檔案。 服務必須使用 LocalSystem、LocalService 或 NetworkService 系統帳戶。 這些帳戶一律會登入;因此，使用這些帳戶的服務所提交的作業一律會執行。

如果在系統帳戶下執行的服務在呼叫 BITS 之前先模擬使用者，則 BITS 會回應任何使用者帳戶 (例如，使用者必須登入電腦，才能進行傳輸) 。 在模擬使用者時，服務也應該使用動態掩蓋搭配 BITS 介面指標。 不會繼承掩蓋，因此您必須在每個從 BITS 收到的介面指標上呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 函式 (例如，呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) 方法所傳回的工作指標) ;在管理員介面指標上設定掩蓋並不夠。 您也可以呼叫進程的 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式，而不是在每個介面指標上呼叫 **CoSetProxyBlanket** 函數。

但是，如果服務未模擬使用者，則適用下列行為：

- 服務帳戶所建立的工作是由該帳戶所擁有。 由於系統帳戶一律會登入，因此 BITS 會傳輸檔案，只要電腦正在執行且有網路連線。
- 系統帳戶不應使用對應的網路磁碟機號，因為磁碟機號是會話特有的磁碟機號，而且在電腦重新開機之後，可能會遺失對應。
- 如果沒有協助程式 [權杖](helper-tokens-for-bits-transfer-jobs.md)，網路驗證會針對 LocalSystem 和 NetworkService 帳戶使用電腦認證，並針對 LocalService 帳戶使用匿名認證。 如果來源檔案 (ACL) 的存取控制清單會限制使用者帳戶的存取權，則 BITS 會傳回「拒絕存取」。
- 如需有關在有協助程式 [權杖](helper-tokens-for-bits-transfer-jobs.md)存在時驗證如何運作的詳細資訊，請參閱 [驗證](authentication.md)。
- Microsoft Internet Explorer 的 proxy 設定會依使用者儲存，而且不會針對系統帳戶進行設定。 請考慮在 BITS 工作上設定協助程式權杖，或呼叫 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 與 **BG \_ 工作 \_ proxy \_ 使用 \_** 方式覆寫來明確設定正確的 proxy 設定。 或者，您可以使用 BitsAdmin.exe 的 **/Util/SetIEProxy** 交換器來設定 LocalSystem、LocalService 或 NetworkService 系統帳戶 Internet Explorer proxy 設定。 如需詳細資訊，請參閱 [BitsAdmin 工具](bitsadmin-tool.md)。

請注意，BITS 無法辨識使用 Proxycfg.exe 檔案設定的 proxy 設定。