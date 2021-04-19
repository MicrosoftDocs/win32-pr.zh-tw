---
description: 說明如何使用自訂安全性封裝 API 建立自訂安全性套件。
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: 自訂安全性套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4c447f1a24a3edc2f25a55f83d82c174094c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998075"
---
# <a name="custom-security-packages"></a><span data-ttu-id="f919b-103">自訂安全性套件</span><span class="sxs-lookup"><span data-stu-id="f919b-103">Custom Security Packages</span></span>

<span data-ttu-id="f919b-104">若要執行與 Windows Server 和 Windows 作業系統整合的新安全性通訊協定，請使用自訂安全性封裝 API 和 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 函數。</span><span class="sxs-lookup"><span data-stu-id="f919b-104">To implement new security protocols that are integrated with the Windows Server and Windows operating systems, use the custom security package API and the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) functions.</span></span>

<span data-ttu-id="f919b-105">自訂安全性封裝 API 支援自訂 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) 的合併開發 (ssp) ，其提供 [非互動式驗證](noninteractive-authentication.md) 服務和安全訊息交換給用戶端/伺服器應用程式，並開發自訂 [*驗證套件*](/windows/desktop/SecGloss/a-gly)，以提供服務給執行 [互動式驗證](interactive-authentication.md)的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f919b-105">The custom security package API supports combined development of custom [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), which provide [Noninteractive Authentication](noninteractive-authentication.md) services and secure message exchange to client/server applications, with the development of custom [*authentication packages*](/windows/desktop/SecGloss/a-gly), which provide services for applications that perform [Interactive Authentication](interactive-authentication.md).</span></span> <span data-ttu-id="f919b-106">這些服務在組合成單一套件時，稱為安全性支援提供者/驗證套件 (SSP/AP) 。</span><span class="sxs-lookup"><span data-stu-id="f919b-106">These services, when combined in a single package, are called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="f919b-107">如同 Microsoft 提供的安全性套件，自訂安全性套件的使用者會使用 [LSA 登入功能](authentication-functions.md)來存取互動式驗證服務。</span><span class="sxs-lookup"><span data-stu-id="f919b-107">As with Microsoft-provided security packages, users of the custom security package access interactive authentication services using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="f919b-108">您可以使用 [安全性支援提供者介面](sspi.md) (SSPI) 直接存取非互動式驗證和訊息保護服務。</span><span class="sxs-lookup"><span data-stu-id="f919b-108">Noninteractive authentication and message protection services can be accessed directly using [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="f919b-109">部署在 SSP/Ap 中的安全性套件會與 LSA 完全整合。</span><span class="sxs-lookup"><span data-stu-id="f919b-109">The security packages deployed in SSP/APs are fully integrated with the LSA.</span></span> <span data-ttu-id="f919b-110">使用自訂安全性套件可用的 LSA 支援函式，開發人員可以執行高階安全性功能，例如建立權杖、 [*補充*](/windows/desktop/SecGloss/s-gly) 認證支援和傳遞驗證。</span><span class="sxs-lookup"><span data-stu-id="f919b-110">Using the LSA support functions available to custom security packages, developers can implement advanced security features such as token creation, [*supplemental credentials*](/windows/desktop/SecGloss/s-gly) support, and pass-through authentication.</span></span> <span data-ttu-id="f919b-111">如需這些支援函式的清單，請參閱 [驗證套件所呼叫的 LSA 函數](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="f919b-111">For a list of these support functions, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span> <span data-ttu-id="f919b-112">如需如何執行自訂安全性封裝的詳細資訊，請參閱 [建立自訂安全性封裝](creating-custom-security-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="f919b-112">For information about how to implement custom security packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

<span data-ttu-id="f919b-113">如需有關自訂安全性封裝的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="f919b-113">For more information about custom security packages, see the following topics.</span></span>



| <span data-ttu-id="f919b-114">主題</span><span class="sxs-lookup"><span data-stu-id="f919b-114">Topic</span></span>                                                                                                                                                 | <span data-ttu-id="f919b-115">描述</span><span class="sxs-lookup"><span data-stu-id="f919b-115">Description</span></span>                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f919b-116">SSP/Ap 與 Ssp</span><span class="sxs-lookup"><span data-stu-id="f919b-116">SSP/APs vs. SSPs</span></span>](ssp-aps-versus-ssps.md)<br/>                                                                                                | <span data-ttu-id="f919b-117">有關如何判斷安全性封裝是否應該位於 SSP/AP 或 SSP 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="f919b-117">Information about how to determine whether a security package should be in an SSP/AP or SSP.</span></span><br/> |
| [<span data-ttu-id="f919b-118">LSA 模式與使用者模式的比較</span><span class="sxs-lookup"><span data-stu-id="f919b-118">LSA Mode vs. User Mode</span></span>](lsa-mode-versus-user-mode.md)<br/>                                                                                    | <span data-ttu-id="f919b-119">LSA 模式和使用者模式不同的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f919b-119">Details about how LSA mode and user mode are different.</span></span><br/>                                      |
| [<span data-ttu-id="f919b-120">註冊和安裝安全性套件的限制</span><span class="sxs-lookup"><span data-stu-id="f919b-120">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)<br/> | <span data-ttu-id="f919b-121">Windows 不支援之安全性封裝的動作。</span><span class="sxs-lookup"><span data-stu-id="f919b-121">Actions by security packages that are not supported in Windows.</span></span><br/>                              |



 

 

