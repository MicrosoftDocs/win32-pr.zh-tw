---
description: 根據先前呼叫 AcceptSecurityCoNtext 的傳回碼 (一般) ，伺服器可以等候來自用戶端的回應，並可與用戶端參與其他交換。
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: 伺服器接續
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985647"
---
# <a name="server-continuation"></a>伺服器接續

根據先前呼叫 AcceptSecurityCoNtext 的傳回碼 [**(一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)，伺服器可以等候來自用戶端的回應，並可與用戶端參與其他交換。 若要繼續驗證通訊協定，伺服器會重複呼叫 **AcceptSecurityCoNtext (一般)**。

[**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)所傳回的狀態會進行檢查，以查看伺服器是否需要等候來自用戶端的其他訊息。 在大部分的驗證通訊協定中，即使是相互驗證，也會有最大的交換數目。 目前，NTLM 和 [*Kerberos 通訊協定*](../secgloss/k-gly.md) 會使用三個交換進行相互驗證。

 

 
