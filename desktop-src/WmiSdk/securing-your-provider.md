---
description: 撰寫安全的提供者需要考慮提供者的裝載方式、提供者如何處理模擬，以及確保檢查使用者是否有資料的存取權限。
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: 保護您的提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dec112c7e207a23d36700d8fb5de3b3964590b514f9cf5a6aa5fbc03243cf40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732838"
---
# <a name="securing-your-provider"></a>保護您的提供者

撰寫安全的提供者需要考慮提供者的裝載方式、提供者如何處理模擬，以及確保檢查使用者是否有資料的存取權限。 您可以藉由要求資料先經過加密驗證，再透過網路傳送，來保護提供者命名空間中的資料。 如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

如果使用者具有任何命名空間的 **完整 \_ 寫入** 存取權，則使用者可以針對命名空間中限制使用者的資料，建立跨命名空間訂閱。 因為提供者可以載入至任何命名空間，並且在任何安全性內容中執行，所以提供者應該執行它自己的存取檢查，以確保只有獲得授權的使用者可以存取資料或執行方法。 如需詳細資訊，請參閱 [執行存取檢查](performing-access-checks.md)。

下列主題討論提供者安全性：

-   [提供者裝載和安全性](provider-hosting-and-security.md)
-   [執行存取檢查](performing-access-checks.md)
-   [用來控制提供者安全性的登錄機碼](registry-keys-for-controlling-provider-security-.md)
-   [存取 WMI 命名空間](access-to-wmi-namespaces.md)
-   [模擬用戶端](impersonating-a-client.md)

下列主題將討論用戶端和腳本如何與提供者安全性互動：

-   [在 WMI 中設定驗證](setting-authentication-in-wmi.md)
-   [在不同的作業系統間連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [使用 VBScript 設定預設進程安全性等級](setting-the-default-process-security-level-using-vbscript.md)
-   [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> <dt>

[使用 WMI](using-wmi.md)
</dt> </dl>

 

 
