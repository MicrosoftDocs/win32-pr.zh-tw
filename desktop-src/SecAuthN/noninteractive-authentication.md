---
description: 只有在進行互動式驗證之後，才可以使用非互動式驗證。 在非互動式驗證期間，使用者不會輸入登入資料，而是會使用先前建立的認證。
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: 非互動式驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658cba212403da2f970e056d7bacc1bc1bcaa559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943368"
---
# <a name="noninteractive-authentication"></a><span data-ttu-id="b5091-104">非互動式驗證</span><span class="sxs-lookup"><span data-stu-id="b5091-104">Noninteractive Authentication</span></span>

<span data-ttu-id="b5091-105">只有在進行 [互動式驗證](interactive-authentication.md) 之後，才可以使用非互動式驗證。</span><span class="sxs-lookup"><span data-stu-id="b5091-105">Noninteractive authentication can only be used after an [interactive authentication](interactive-authentication.md) has taken place.</span></span> <span data-ttu-id="b5091-106">在非互動式驗證期間，使用者不會輸入 [*登入資料*](../secgloss/l-gly.md)，而是會使用先前建立的 [*認證*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="b5091-106">During noninteractive authentication, the user does not input [*logon data*](../secgloss/l-gly.md), instead, previously established [*credentials*](../secgloss/c-gly.md) are used.</span></span>

<span data-ttu-id="b5091-107">當應用程式使用 [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 和安全性套件來建立安全的網路連線時，就會執行非互動式驗證。</span><span class="sxs-lookup"><span data-stu-id="b5091-107">Noninteractive authentication is performed when an application uses the [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and a security package to establish a secure network connection.</span></span> <span data-ttu-id="b5091-108">非互動式驗證是一種機制，可讓使用者連接到網路上的多部電腦，而不需要為每部機器重新輸入登入資訊。</span><span class="sxs-lookup"><span data-stu-id="b5091-108">Noninteractive authentication is the mechanism at work when a user connects to multiple machines on a network without having to re-enter logon information for each machine.</span></span> <span data-ttu-id="b5091-109">例如，如果應用程式需要在遠端電腦上開啟安全資料夾，而且應用程式使用者已經以互動方式登入網域帳戶，則應用程式不會要求使用者重新提供登入資料。</span><span class="sxs-lookup"><span data-stu-id="b5091-109">For example, if an application needs to open a secure folder on a remote machine and the application user is already interactively logged on to a domain account, the application does not require the user to supply logon data again.</span></span> <span data-ttu-id="b5091-110">相反地，應用程式可以使用 SSPI 要求非互動式驗證，將先前建立的安全性資訊傳遞到安全性套件。</span><span class="sxs-lookup"><span data-stu-id="b5091-110">Instead, the application can request a noninteractive authentication by using SSPI to pass the previously established security information to a security package.</span></span> <span data-ttu-id="b5091-111">然後，安全性封裝會使用 LSA 函數來檢查 [*認證*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b5091-111">The security package then uses LSA functions to check the [*credentials*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="b5091-112">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="b5091-112">The following diagram illustrates this procedure.</span></span>

![非互動式驗證](images/lsasspi2.png)

<span data-ttu-id="b5091-114">在上圖中，用戶端應用程式會起始對 SSPI 的呼叫，要求已驗證的網路連接。</span><span class="sxs-lookup"><span data-stu-id="b5091-114">In the preceding diagram, the client application initiates a call to SSPI to request an authenticated network connection.</span></span> <span data-ttu-id="b5091-115">SSPI 會將用戶端的要求傳遞至安全性封裝以進行處理。</span><span class="sxs-lookup"><span data-stu-id="b5091-115">SSPI passes the client's request to a security package for processing.</span></span> <span data-ttu-id="b5091-116">安全性套件會藉由呼叫「 [*本地安全機構*](../secgloss/l-gly.md) 」 (LSA) 來驗證使用者，並指定 [*驗證套件*](../secgloss/a-gly.md) 並提供使用者現有的認證。</span><span class="sxs-lookup"><span data-stu-id="b5091-116">The security package authenticates the user by calling the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and specifying an [*authentication package*](../secgloss/a-gly.md) and providing the user's existing credentials.</span></span>

<span data-ttu-id="b5091-117">驗證結果會從 [*驗證套件*](../secgloss/a-gly.md)、透過 LSA 傳送到 [*安全性套件*](../secgloss/s-gly.md)，最後傳遞給 SSPI。</span><span class="sxs-lookup"><span data-stu-id="b5091-117">The authentication result is passed from the [*authentication package*](../secgloss/a-gly.md), through the LSA, to the [*security package*](../secgloss/s-gly.md), and finally to SSPI.</span></span> <span data-ttu-id="b5091-118">SSPI 會通知用戶端應用程式有關要求的結果。</span><span class="sxs-lookup"><span data-stu-id="b5091-118">SSPI notifies the client application about the outcome of the request.</span></span>

<span data-ttu-id="b5091-119">如需 SSPI 的詳細資訊，請參閱 [安全性支援提供者介面](sspi.md)。</span><span class="sxs-lookup"><span data-stu-id="b5091-119">For more information about SSPI, see [Security Support Provider Interface](sspi.md).</span></span>

 

 
