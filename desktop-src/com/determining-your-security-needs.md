---
title: 判斷您的安全性需求
description: 您如何設定應用程式的 COM 安全性，取決於您的應用程式所需的安全性類型。 有幾種常見的情況會決定您應該做什麼。
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675823"
---
# <a name="determining-your-security-needs"></a>判斷您的安全性需求

您如何設定應用程式的 COM 安全性，取決於您的應用程式所需的安全性類型。 有幾種常見的情況會決定您應該做什麼。

如果您決定使用 COM 安全性預設值，就不需要執行 anythingâ€」 COM 全部處理。 如需這些預設設定的詳細資訊，請參閱 [COM 安全性預設值](com-security-defaults.md)。

您也可以停用遠端電腦) 之間的所有遠端電腦 (COM，以防止任何遠端呼叫您的電腦。 如需詳細資訊，請參閱 [使用 DCOMCNFG 設定 System-Wide 安全性](setting-machine-wide-security-using-dcomcnfg.md)。

針對舊版或新的應用程式，您可以在登錄中設定整個進程的安全性。 如需詳細資訊，請參閱 [透過登錄設定 Processwide 安全性](setting-processwide-security-through-the-registry.md)。

您也可以覆寫進程中特定介面呼叫的預設安全性設定，同時設定其餘進程 (的預設安全性，以允許 COM 處理一般案例) 。 如需詳細資訊，請參閱在 [介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)。

針對複雜的安全性需求，您可以透過程式設計方式來處理所有安全性，而不是讓 COM 為您處理。 若要這樣做，請呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來停用自動驗證，然後藉由設定每個介面的安全性來控制所有安全性設定。 如需詳細資訊，請參閱 [使用 CoInitializeSecurity 設定 Processwide 安全性](setting-processwide-security-with-coinitializesecurity.md) 和 [在介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)。

在某些情況下，您可能會想要完全關閉安全性。 您可能會決定您的應用程式不需要任何安全性，或者您可能想要在開發期間停用安全性，讓您可以個別啟用安全性功能。 若要瞭解如何停用 COM 安全性，請參閱 [關閉安全性](turning-off-security.md)。

COM 中的安全性依賴安全性封裝所管理的驗證服務。 NTLMSSP 適用于許多應用程式，但不提供其他封裝所提供的更健全安全性。 因此，COM 支援 Schannel 安全性封裝和 Kerberos v5 安全性通訊協定。 如需使用這些安全性封裝的詳細資訊，請參閱 [COM 和安全性封裝](com-and-security-packages.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




