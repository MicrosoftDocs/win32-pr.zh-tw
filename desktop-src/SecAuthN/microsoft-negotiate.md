---
description: Microsoft Negotiate 是安全性支援提供者，可作為安全性支援提供者介面和其他 Ssp 之間的應用層。
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd223267a2e7d0e4dc23ae356a6fa2e6224c742c491e428369f15fb6d46ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786950"
---
# <a name="microsoft-negotiate"></a>Microsoft Negotiate

Microsoft Negotiate 是 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) ，可作為 [*安全性支援提供者介面*](../secgloss/s-gly.md) ([SSPI](sspi.md)) 和其他 ssp 之間的應用層。 當應用程式呼叫 SSPI 以登入網路時，它可以指定 SSP 來處理要求。 如果應用程式指定 Negotiate，Negotiate 會分析要求，並根據客戶設定的安全性原則挑選最適合的 SSP 來處理要求。

目前，協商安全性封裝會在 [Kerberos](microsoft-kerberos.md) 和 [NTLM](microsoft-ntlm.md)之間進行選取。 除非其中一個涉及驗證的系統無法使用，或呼叫的應用程式未提供足夠的資訊來使用 Kerberos，否則 Negotiate 會選取 Kerberos。

若要允許 Negotiate 選取 [Kerberos](microsoft-kerberos.md) 安全性提供者，用戶端應用程式必須提供 [*服務主體名稱*](../secgloss/s-gly.md) (SPN) 、使用者主體名稱 (UPN) 或 NetBIOS 帳戶名稱做為目標名稱。 否則，Negotiate 一律會選取 [NTLM](microsoft-ntlm.md) 安全性提供者。

使用 Negotiate 封裝的伺服器能夠回應明確選取 [Kerberos](microsoft-kerberos.md) 或 [NTLM](microsoft-ntlm.md) 安全性提供者的用戶端應用程式。 不過，用戶端應用程式必須知道伺服器支援 Negotiate 封裝，才能使用 Negotiate 要求驗證。 不支援 Negotiate 的伺服器不一定會回應指定 Negotiate 作為 SSP 之用戶端的要求。

## <a name="reasons-to-use-the-negotiate-package"></a>使用 Negotiate 套件的原因

-   允許系統使用最強的 (最安全) 可用的通訊協定。
-   確保應用程式的向前相容性。
-   確保您的應用程式表現出與客戶所設定之安全性原則一致的行為。

 

 
