---
description: 某些安全性套件支援擴充的錯誤訊息，讓通訊連結的側邊能夠傳達失敗的任何原因。
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: 延伸錯誤資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980340"
---
# <a name="extended-error-information"></a><span data-ttu-id="4cc0f-103">延伸錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="4cc0f-103">Extended Error Information</span></span>

<span data-ttu-id="4cc0f-104">某些 [*安全性套件*](/windows/desktop/SecGloss/s-gly) 支援擴充的錯誤訊息，讓通訊連結的側邊能夠傳達失敗的任何原因。</span><span class="sxs-lookup"><span data-stu-id="4cc0f-104">Some [*security packages*](/windows/desktop/SecGloss/s-gly) support extended error messages that allow the sides of a communication link to communicate any reasons for a failure.</span></span> <span data-ttu-id="4cc0f-105">例如， [*kerberos 通訊協定*](/windows/desktop/SecGloss/k-gly) 可能會因為 kerberos 票證要求和票證時間之間的時間差異而失敗。</span><span class="sxs-lookup"><span data-stu-id="4cc0f-105">For example, the [*Kerberos protocol*](/windows/desktop/SecGloss/k-gly) could fail because of a time discrepancy between the time of request for a Kerberos ticket and the ticket's time of issue.</span></span> <span data-ttu-id="4cc0f-106">用戶端可以使用傳回的延伸錯誤資訊來重新同步處理其時鐘，並產生新的連接訊息。</span><span class="sxs-lookup"><span data-stu-id="4cc0f-106">With information from returned extended error information, a client can resynchronize its clock and generate a new connection message.</span></span>

<span data-ttu-id="4cc0f-107">在 \_ \_ \_ [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)結構的 **fCapabilities** 成員中設定 SECPKG 旗標延伸錯誤旗標的安全性封裝，表示安全性封裝支援擴充錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4cc0f-107">A security package setting the SECPKG\_FLAG\_EXTENDED\_ERROR flag in the **fCapabilities** member of a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure indicates that the security package supports extended error messages.</span></span>

<span data-ttu-id="4cc0f-108">需要擴充錯誤訊息的用戶端應用程式 \_ 會 \_ \_ 在呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式時，指定 ISC 需求擴充錯誤旗標。</span><span class="sxs-lookup"><span data-stu-id="4cc0f-108">Client applications requiring extended error messages specify the ISC\_REQ\_EXTENDED\_ERROR flag when calling the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="4cc0f-109">需要擴充錯誤訊息的伺服器應用程式會 \_ \_ \_ 在呼叫 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)時，設定 ASC 需求擴充錯誤旗標。</span><span class="sxs-lookup"><span data-stu-id="4cc0f-109">Server applications requiring extended error messages set the ASC\_REQ\_EXTENDED\_ERROR flag when calling [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span>

 

 
