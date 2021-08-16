---
description: 說明如何使用自訂安全性封裝 API 建立自訂安全性套件。
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: 自訂安全性套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799edb3eb8e0551afe7d7f7bcdc54924228445d6ffb28cb4773af843b5c2d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008666"
---
# <a name="custom-security-packages"></a>自訂安全性套件

若要執行與 Windows Server 和 Windows 作業系統整合的新安全性通訊協定，請使用自訂安全性封裝 API 和 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 函式。

自訂安全性封裝 API 支援自訂 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) 的合併開發 (ssp) ，其提供 [非互動式驗證](noninteractive-authentication.md) 服務和安全訊息交換給用戶端/伺服器應用程式，並開發自訂 [*驗證套件*](/windows/desktop/SecGloss/a-gly)，以提供服務給執行 [互動式驗證](interactive-authentication.md)的應用程式。 這些服務在組合成單一套件時，稱為安全性支援提供者/驗證套件 (SSP/AP) 。

如同 Microsoft 提供的安全性套件，自訂安全性套件的使用者會使用 [LSA 登入功能](authentication-functions.md)來存取互動式驗證服務。 您可以使用 [安全性支援提供者介面](sspi.md) (SSPI) 直接存取非互動式驗證和訊息保護服務。

部署在 SSP/Ap 中的安全性套件會與 LSA 完全整合。 使用自訂安全性套件可用的 LSA 支援函式，開發人員可以執行高階安全性功能，例如建立權杖、 [*補充*](/windows/desktop/SecGloss/s-gly) 認證支援和傳遞驗證。 如需這些支援函式的清單，請參閱 [驗證套件所呼叫的 LSA 函數](authentication-functions.md)。 如需如何執行自訂安全性封裝的詳細資訊，請參閱 [建立自訂安全性封裝](creating-custom-security-packages.md)。

如需有關自訂安全性封裝的詳細資訊，請參閱下列主題。



| 主題                                                                                                                                                 | 描述                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/Ap 與 Ssp](ssp-aps-versus-ssps.md)<br/>                                                                                                | 有關如何判斷安全性封裝是否應該位於 SSP/AP 或 SSP 中的資訊。<br/> |
| [LSA 模式與使用者模式的比較](lsa-mode-versus-user-mode.md)<br/>                                                                                    | LSA 模式和使用者模式不同的詳細資料。<br/>                                      |
| [註冊和安裝安全性套件的限制](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Windows 中不支援之安全性封裝的動作。<br/>                              |



 

 

