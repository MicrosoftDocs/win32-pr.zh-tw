---
description: 列出並說明初始化安全性封裝所需的步驟。
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: 初始化安全性封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115065"
---
# <a name="initializing-the-security-package"></a><span data-ttu-id="1085c-103">初始化安全性封裝</span><span class="sxs-lookup"><span data-stu-id="1085c-103">Initializing the Security Package</span></span>

<span data-ttu-id="1085c-104">使用 SSPI 之前，必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1085c-104">These steps are necessary before using SSPI:</span></span>

1.  <span data-ttu-id="1085c-105">您必須呼叫初始化函式，才能取得安全性函式資料表的位址。</span><span class="sxs-lookup"><span data-stu-id="1085c-105">The initialization function must be called to obtain the address of the security function table.</span></span>

    <span data-ttu-id="1085c-106">[**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea)分派資料表指標的用戶端和伺服器呼叫 [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) 。</span><span class="sxs-lookup"><span data-stu-id="1085c-106">The client and server call [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) for a pointer to a [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) dispatch table.</span></span> <span data-ttu-id="1085c-107">此資料表包含在 Sspi 中宣告之回呼函式的指標。</span><span class="sxs-lookup"><span data-stu-id="1085c-107">This table contains pointers to callback functions declared in Sspi.h.</span></span> <span data-ttu-id="1085c-108">這些指標可讓您存取各種 SSPI 函式的 DLL 實作為。</span><span class="sxs-lookup"><span data-stu-id="1085c-108">These pointers provide access to the DLL's implementations of the various SSPI functions.</span></span>

2.  <span data-ttu-id="1085c-109">您必須取得有關支援之安全性封裝的資訊。</span><span class="sxs-lookup"><span data-stu-id="1085c-109">Information must be obtained about the supported security packages.</span></span>

    <span data-ttu-id="1085c-110">雖然大部分的應用程式都使用支援預設或一般功能的安全性封裝，但安全性套件可能具有應用程式所需的獨特功能。</span><span class="sxs-lookup"><span data-stu-id="1085c-110">While most applications use security packages that support default or common capabilities, security packages can have unique capabilities of interest to the application.</span></span> <span data-ttu-id="1085c-111">需要特殊功能的應用程式可以使用提供這些功能的套件。</span><span class="sxs-lookup"><span data-stu-id="1085c-111">An application needing special capabilities can use a package that offers those capabilities.</span></span> <span data-ttu-id="1085c-112">如需詳細資訊，請參閱 [取得安全性封裝的相關資訊](getting-information-about-security-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="1085c-112">For more information, see [Getting Information About Security Packages](getting-information-about-security-packages.md).</span></span>

<span data-ttu-id="1085c-113">此時，應用程式已成功將 SSP 初始化，並選擇具有足夠功能的安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="1085c-113">At this point, the application has successfully initialized an SSP and chosen a security package with sufficient capabilities.</span></span>

<span data-ttu-id="1085c-114">您可以在用戶端與伺服器之間，使用可在幕後使用哪一個 [*安全性封裝*](../secgloss/s-gly.md)進行 [*協商*](../secgloss/n-gly.md)的合約套件。</span><span class="sxs-lookup"><span data-stu-id="1085c-114">The [*Negotiate*](../secgloss/n-gly.md) package can be used where agreement between client and server about which [*security package*](../secgloss/s-gly.md) to use is done behind the scenes.</span></span> <span data-ttu-id="1085c-115">如果未使用 Negotiate 套件，用戶端和伺服器必須同意特定安全性封裝，才能執行上述設定步驟。</span><span class="sxs-lookup"><span data-stu-id="1085c-115">If the Negotiate package is not used, the client and server must agree on the specific security package to use before performing the setup steps above.</span></span>

 

 
