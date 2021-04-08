---
title: System-Wide 安全性的登錄值
description: System-Wide 安全性的登錄值
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932075"
---
# <a name="registry-values-for-system-wide-security"></a>System-Wide 安全性的登錄值

不建議您變更整個系統的安全性設定，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。 如果您要變更全系統安全性設定，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。 如需設定整個進程安全性的詳細資訊，請參閱 [設定 Process-Wide 安全性](setting-processwide-security.md)。

登錄中的某些值是用來判斷未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)之應用程式的安全性設定。 您可以使用 Dcomcnfg.exe 來修改電腦的這些預設安全性設定。 如需說明如何將 Dcomcnfg.exe 用於此用途的逐步程式，請參閱 [使用 DCOMCNFG 設定 System-Wide 安全性](setting-machine-wide-security-using-dcomcnfg.md)。

變更預設全系統設定的另一種方式是直接操作登錄值。 不過，只有系統管理員和系統具有登錄部分的完整存取權，其中包含預設的全系統呼叫安全性設定。 所有其他使用者都只能讀取存取權。

會影響全系統安全性預設值的命名值如下：

-   [DefaultLaunchPermission](defaultlaunchpermission.md)
-   [DefaultAccessPermission](defaultaccesspermission.md)
-   [LegacyAuthenticationLevel](legacyauthenticationlevel.md)
-   [LegacyImpersonationLevel](legacyimpersonationlevel.md)
-   [LegacySecureReferences](legacysecurereferences.md)
-   [SRPRunningObjectChecks](srprunningobjectchecks.md)
-   [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 Process-Wide 安全性](setting-processwide-security.md)
</dt> </dl>

 

 




