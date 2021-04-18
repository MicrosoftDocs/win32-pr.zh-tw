---
title: 修改電腦的安全性預設值
description: 修改電腦的安全性預設值
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371831"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>修改電腦的安全性預設值

不建議您變更整個系統的安全性設定，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。 如果您要變更全系統安全性設定，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。 如需設定整個進程安全性的詳細資訊，請參閱 [設定 Process-Wide 安全性](setting-processwide-security.md)。

登錄中的某些值會決定未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)之應用程式的安全性設定。 您可以使用 Dcomcnfg.exe 來修改這些設定。

如需詳細資訊，請參閱下列主題：

-   [System-Wide 安全性的登錄值](registry-values-for-machine-wide-security.md)
-   [使用 DCOMCNFG 設定 System-Wide 安全性](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定整個進程的安全性](setting-processwide-security.md)
</dt> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




