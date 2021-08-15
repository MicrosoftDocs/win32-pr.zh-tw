---
description: Windows 作業系統支援使用安全性封裝（以安全性支援提供者和驗證套件的形式）來進行驗證。
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: 安全性支援提供者/驗證套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62f634d0571eab43652485f8ca1313f78fd157ca202d5d78369552db648de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918337"
---
# <a name="security-support-providerauthentication-packages"></a>安全性支援提供者/驗證套件

Windows 作業系統支援使用 [*安全性封裝*](../secgloss/s-gly.md)（以 [*安全性支援提供者*](../secgloss/s-gly.md)和 [*驗證套件*](../secgloss/a-gly.md)的形式）來進行驗證。 安全性套件提供 Windows 驗證套件的登入程式支援服務，也會藉由執行一組對應至[安全性支援提供者介面](sspi.md)的函式（ (SSPI) ），為應用程式提供驗證服務。

作為驗證套件並執行 [*SSPI*](../secgloss/s-gly.md) 所需功能的安全性封裝，稱為安全性支援提供者/驗證套件 (SSP/AP) 。

如需安全性封裝的詳細資訊，請參閱 [Microsoft 提供的 SSP 套件](ssp-packages-provided-by-microsoft.md)。 如需有關開發自訂 SSP/Ap 的詳細資訊，請參閱 [自訂安全性封裝](custom-security-packages.md)。

 

 
