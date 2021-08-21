---
title: 在安裝時註冊類別
description: 如果某個類別打算隨時供用戶端使用，則在大部分的應用程式中，您通常會透過安裝和安裝程式進行註冊。
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017e4393a4c5422157c8f9b9e9b7f366c2fafc8cfe6af5722e451a3d1b9fa069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047856"
---
# <a name="registering-a-class-at-installation"></a>在安裝時註冊類別

如果某個類別打算隨時供用戶端使用，則在大部分的應用程式中，您通常會透過安裝和安裝程式進行註冊。 這表示將應用程式的相關資訊放入登錄中，包括將應用程式的物件具現化的方式和位置。 這是所有 Clsid 都必須註冊的資訊。 其他資訊則為選擇性。 Regsvr32 之類的工具可讓您輕鬆地撰寫安裝程式，以便在安裝時註冊伺服器。

如果您不依賴系統預設值，登錄中會有兩個重要的金鑰： CLSID 和 AppID。 這些機碼底下的重要資訊片段是物件的具現化方式。 物件可以指定為同進程、跨進程的本機或跨進程的遠端。

AppID 金鑰底下有幾個值，可定義該應用程式的特定資訊。 這些都是 [RemoteServerName](remoteservername.md) 和 [ActivateAtStorage](activateatstorage.md)，這兩者都可以用來允許用戶端建立物件，而用戶端則沒有伺服器位置的內建知識。  (如需有關遠端具現化的詳細資訊，請參閱 [尋找遠端物件](locating-a-remote-object.md) 和 [實例建立](instance-creation-helper-functions.md)協助程式函數。 ) 

伺服器也可以安裝為服務，或是在特定使用者帳戶下執行。 如需詳細資訊，請參閱 [安裝為服務應用程式](installing-as-a-service-application.md)。

不是服務或在特定使用者帳戶下執行的伺服器或 ROT 物件可以稱為「啟動為啟動項」伺服器。 針對這些伺服器，安全性內容和用戶端的視窗工作站/桌面必須符合伺服器的。 嘗試連接到遠端伺服器的用戶端會被視為具有 **Null** 視窗工作站/桌上型電腦，因此在此實例中只會比較伺服器安全性內容。  (如需 Sid 的詳細資訊，請參閱 [com 中的安全性](security-in-com.md)。 ) com 會在進程第一次連接到分散式 COM 服務時，快取進程的視窗站/桌面。 因此，在呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**COINITIALIZEEX**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)之後，COM 用戶端和伺服器不應該變更進程的視窗工作站或執行緒桌面。

當類別註冊為同進程時，COM 會將 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 的呼叫自動傳遞至 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式，該函式必須實作為呼叫物件，以提供其類別物件的指標。

在可執行檔中執行的類別可指定 COM 應執行其進程，並等候進程透過呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)函式來註冊其類別物件的 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 登錄機碼](com-registry-keys.md)
</dt> <dt>

[安裝為服務應用程式](installing-as-a-service-application.md)
</dt> <dt>

[註冊正在執行的 EXE 伺服器](registering-a-running-exe-server.md)
</dt> <dt>

[註冊元件](registering-components.md)
</dt> <dt>

[在 ROT 中註冊物件](registering-objects-in-the-rot.md)
</dt> <dt>

[自我註冊](self-registration.md)
</dt> </dl>

 

 