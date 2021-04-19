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
# <a name="server-continuation"></a><span data-ttu-id="da3d4-103">伺服器接續</span><span class="sxs-lookup"><span data-stu-id="da3d4-103">Server Continuation</span></span>

<span data-ttu-id="da3d4-104">根據先前呼叫 AcceptSecurityCoNtext 的傳回碼 [**(一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)，伺服器可以等候來自用戶端的回應，並可與用戶端參與其他交換。</span><span class="sxs-lookup"><span data-stu-id="da3d4-104">Based on the return code from a previous call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), the server can wait for a response from the client and can participate in additional exchanges with the client.</span></span> <span data-ttu-id="da3d4-105">若要繼續驗證通訊協定，伺服器會重複呼叫 **AcceptSecurityCoNtext (一般)**。</span><span class="sxs-lookup"><span data-stu-id="da3d4-105">To continue the authentication protocol, the server repeats calls to **AcceptSecurityContext (General)**.</span></span>

<span data-ttu-id="da3d4-106">[**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)所傳回的狀態會進行檢查，以查看伺服器是否需要等候來自用戶端的其他訊息。</span><span class="sxs-lookup"><span data-stu-id="da3d4-106">The status returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) is checked to see if the server needs to wait for additional messages from the client.</span></span> <span data-ttu-id="da3d4-107">在大部分的驗證通訊協定中，即使是相互驗證，也會有最大的交換數目。</span><span class="sxs-lookup"><span data-stu-id="da3d4-107">In most authentication protocols, there is a maximum number of exchanges even for mutual authentication.</span></span> <span data-ttu-id="da3d4-108">目前，NTLM 和 [*Kerberos 通訊協定*](../secgloss/k-gly.md) 會使用三個交換進行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="da3d4-108">Currently, both the NTLM and [*Kerberos protocols*](../secgloss/k-gly.md) do mutual authentication with three exchanges.</span></span>

 

 
