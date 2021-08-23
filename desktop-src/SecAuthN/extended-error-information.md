---
description: 某些安全性套件支援擴充的錯誤訊息，讓通訊連結的側邊能夠傳達失敗的任何原因。
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: 延伸錯誤資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd93de1691a01802f65397abb1607612f5b7e61a311c9f801854a00c1ab4f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008216"
---
# <a name="extended-error-information"></a>延伸錯誤資訊

某些 [*安全性套件*](/windows/desktop/SecGloss/s-gly) 支援擴充的錯誤訊息，讓通訊連結的側邊能夠傳達失敗的任何原因。 例如， [*kerberos 通訊協定*](/windows/desktop/SecGloss/k-gly) 可能會因為 kerberos 票證要求和票證時間之間的時間差異而失敗。 用戶端可以使用傳回的延伸錯誤資訊來重新同步處理其時鐘，並產生新的連接訊息。

在 \_ \_ \_ [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)結構的 **fCapabilities** 成員中設定 SECPKG 旗標延伸錯誤旗標的安全性封裝，表示安全性封裝支援擴充錯誤訊息。

需要擴充錯誤訊息的用戶端應用程式 \_ 會 \_ \_ 在呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式時，指定 ISC 需求擴充錯誤旗標。 需要擴充錯誤訊息的伺服器應用程式會 \_ \_ \_ 在呼叫 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)時，設定 ASC 需求擴充錯誤旗標。

 

 
