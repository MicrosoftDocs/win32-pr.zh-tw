---
description: 說明如何建立自訂安全性封裝。
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: 建立自訂安全性套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88093ba7faed1ac2287c2a54391015984e83d4ad3878a60453978a9924706f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008846"
---
# <a name="creating-custom-security-packages"></a>建立自訂安全性套件

## <a name="ssp-security-packages"></a>SSP 安全性封裝

如果自訂安全性支援提供者 (SSP) 安全性套件將專門用於用戶端/伺服器安全性支援，它可以執行 Microsoft [安全性支援提供者介面](sspi.md)。

SampSSP 範例隨附于平臺軟體發展工具組 (SDK) 包含範例 SSP 安全性封裝的執行。

## <a name="sspap-security-packages"></a>SSP/AP 安全性套件

 (ssp/ap 的自訂 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) / [*驗證套件*](/windows/desktop/SecGloss/a-gly)) 包含可作為驗證套件的安全性套件 (ap) 以及 (ssp) 的安全性支援提供者。 這些套件會執行個別的 Api 來支援每個角色。

因為它是做為 AP 的功能，所以自訂 SSP/AP [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 必須針對 [驗證封裝所執行](authentication-functions.md)的所有函式提供執行。

為了提供整合式安全性支援，自訂的 SSP/AP 安全性套件必須提供 [SSP/ap 所執行](authentication-functions.md)之函式的執行。 [由 ssp/ap 所呼叫的 LSA](authentication-functions.md) 函式描述可供 SSP/ap 開發人員使用的支援函式，這些開發人員需要與 LSA 互動。

SSP/AP 安全性封裝若要同時以 AP 和 SSP 的形式執行，則可作為作業系統的一部分執行，並做為使用者應用程式的一部分。 這兩種執行模式分別稱為 LSA 模式和使用者模式。 如需 LSA 模式的自訂安全性封裝的詳細資訊，請參閱 [Lsa 模式初始化](lsa-mode-initialization.md)。 如需使用者模式的詳細資訊，請參閱 [使用者模式初始化](user-mode-initialization.md)。

如果自訂的 SSP/AP 安全性封裝提供服務給用戶端/伺服器應用程式，它應該會提供 [使用者模式 SSP/ap 所執行](authentication-functions.md)之函式中所述函式的執行。 [使用者模式 SSP/ap 所呼叫的 LSA 函式](authentication-functions.md) 描述可供在用戶端或伺服器進程中執行的 SSP/AP 使用的支援功能。

如需註冊 SSP/AP DLL 的詳細資訊，請參閱 [註冊 ssp/ap](registering-ssp-ap-dlls.md)dll。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊和安裝安全性套件的限制](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
