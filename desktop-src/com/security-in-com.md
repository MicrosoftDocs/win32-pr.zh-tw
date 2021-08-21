---
title: COM 中的安全性
description: COM 中的安全性是根據 Windows 以及基礎 RPC 安全性機制所提供的安全性而穩定的。
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b197a632494545e5a151110ca17f1cf1ae1df7577a897284d1e5d437b74093f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918119"
---
# <a name="security-in-com"></a>COM 中的安全性

COM 中的安全性是根據 Windows 以及基礎 RPC 安全性機制所提供的安全性而穩定的。 COM 安全性依賴 *驗證* (驗證呼叫者的身分識別) 和 *授權* 的程式 (判斷呼叫端是否已獲授權可進行要求) 的處理常式。 COM 中有兩種主要的安全性類型： *啟用安全性* 和 *呼叫安全性*。 啟用安全性可判斷用戶端是否可以啟動伺服器。 啟動伺服器之後，您可以使用 [呼叫安全性] 來控制伺服器物件的存取權。

在此安全性模型中，伺服器會管理和協助保護物件、用戶端透過伺服器取得物件的存取權，而且伺服器可以在模擬用戶端時嘗試存取。

系統會執行 Kerberos v5 驗證通訊協定和 Schannel 安全性封裝。 它也包含委派層級模擬、相互驗證、在登錄中設定 AppID 的驗證層級，以及進行掩蓋等功能。 使用 COM 安全性，您可以在不危及安全性的情況下，執行可執行特殊許可權作業的物件。

因為有各式各樣的 COM 安全性功能，所以一開始就有助於判斷您的應用程式所需的安全性類型。 對於大部分的應用程式而言，設定可接受的安全性層級可能是一個簡單的程式，不過您也可以使用 COM 安全性來支援非常複雜的安全性案例。

您可以設定安全性 processwide，方法是使用 Dcomcnfg.exe 設定登錄或呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。 有兩個主要介面、 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 和 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (以及相關聯的 helper 函式) ，可讓您在程式內設定呼叫層級安全性。

若要深入瞭解 COM 安全性，請參閱下列主題：

-   [判斷您的安全性需求](determining-your-security-needs.md)
-   [COM 安全性預設值](com-security-defaults.md)
-   [啟用安全性](activation-security.md)
-   [安全性值](security-values.md)
-   [設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
-   [使用 DCOMCNFG 啟用 COM 安全性](enabling-com-security-using-dcomcnfg.md)
-   [關閉安全性](turning-off-security.md)
-   [伺服器端安全性](server-side-security.md)
-   [安全性的總協商](security-blanket-negotiation.md)
-   [COM 和安全性封裝](com-and-security-packages.md)
-   [Windows XP service pack 2 和 Windows Server 2003 Service pack 1 中的 DCOM 安全性增強功能](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [COM 的存取控制清單](access-control-lists-for-com.md)
-   [COM 提高許可權的標記](the-com-elevation-moniker.md)

 

 