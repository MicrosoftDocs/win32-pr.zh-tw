---
title: RAS 安全性主機支援
description: Windows NT 4.0 提供了一種方法，可讓協力廠商 RAS 安全性 DLL 增強內建的 RAS 安全性功能。 Windows 95 未提供此支援。
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- 主機支援，RAS
- 安全性主機支援，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674027"
---
# <a name="ras-security-host-support"></a><span data-ttu-id="aad6c-106">RAS 安全性主機支援</span><span class="sxs-lookup"><span data-stu-id="aad6c-106">RAS Security Host Support</span></span>

<span data-ttu-id="aad6c-107">Windows NT 4.0 提供了一種方法，可讓協力廠商 RAS 安全性 DLL 增強內建的 RAS 安全性功能。</span><span class="sxs-lookup"><span data-stu-id="aad6c-107">Windows NT 4.0 provides a way for a third-party RAS security DLL to enhance the built-in RAS security features.</span></span> <span data-ttu-id="aad6c-108">Windows 95 未提供此支援。</span><span class="sxs-lookup"><span data-stu-id="aad6c-108">Windows 95 does not provide this support.</span></span>

<span data-ttu-id="aad6c-109">Windows NT/Windows 2000 RAS 伺服器提供驗證遠端使用者網路存取的安全性機制。</span><span class="sxs-lookup"><span data-stu-id="aad6c-109">A Windows NT/Windows 2000 RAS server provides security mechanisms for validating the network access of remote users.</span></span> <span data-ttu-id="aad6c-110">當 RAS 伺服器接收到呼叫時，會針對本機或網域帳戶資料庫驗證使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="aad6c-110">When a RAS server receives a call, it validates the user's credentials against the local or domain account database.</span></span> <span data-ttu-id="aad6c-111">RAS 也支援回呼安全性，在這種情況下，RAS 伺服器會掛斷，然後再回呼遠端使用者來建立連線。</span><span class="sxs-lookup"><span data-stu-id="aad6c-111">RAS also supports call-back security, in which the RAS server hangs up and then calls back to the remote user to establish the connection.</span></span> <span data-ttu-id="aad6c-112">對於此安全性層級不足的網路，您可以安裝協力廠商 RAS 安全性 DLL。</span><span class="sxs-lookup"><span data-stu-id="aad6c-112">For networks in which this level of security is not enough, you can install a third-party RAS security DLL.</span></span> <span data-ttu-id="aad6c-113">然後，安全性 DLL 可以從標準使用者帳戶資料庫以外的資料庫讀取安全性資訊，以驗證遠端使用者。</span><span class="sxs-lookup"><span data-stu-id="aad6c-113">The security DLL can then authenticate a remote user by reading security information from a database other than the standard user account database.</span></span>

<span data-ttu-id="aad6c-114">當 RAS 伺服器接收到呼叫時，它會叫用安全性 DLL 來驗證遠端使用者。</span><span class="sxs-lookup"><span data-stu-id="aad6c-114">When the RAS server receives a call, it invokes the security DLL to authenticate the remote user.</span></span> <span data-ttu-id="aad6c-115">RAS 安全性主機支援提供一種機制，讓安全性 DLL 透過遠端電腦上的終端機視窗與遠端使用者進行通訊。</span><span class="sxs-lookup"><span data-stu-id="aad6c-115">The RAS security host support provides a mechanism for the security DLL to communicate with the remote user through a terminal window on the remote computer.</span></span> <span data-ttu-id="aad6c-116">在一般案例中，安全性 DLL 會要求遠端使用者的登入名稱。</span><span class="sxs-lookup"><span data-stu-id="aad6c-116">In a typical scenario, the security DLL asks for the logon name of the remote user.</span></span> <span data-ttu-id="aad6c-117">然後，DLL 會使用其私用安全性資料庫來制定傳送至遠端終端機機的挑戰。</span><span class="sxs-lookup"><span data-stu-id="aad6c-117">The DLL then uses its private security database to formulate a challenge to send to the remote terminal.</span></span> <span data-ttu-id="aad6c-118">例如，這項挑戰可能是使用者必須提供做為 cardkey 讀者輸入的程式碼。</span><span class="sxs-lookup"><span data-stu-id="aad6c-118">For example, the challenge could be a code that the user must provide as input to a cardkey reader.</span></span> <span data-ttu-id="aad6c-119">Cardkey 讀取器接著會顯示遠端使用者在終端機視窗中輸入的回應。</span><span class="sxs-lookup"><span data-stu-id="aad6c-119">The cardkey reader then displays a response that the remote user types in the terminal window.</span></span> <span data-ttu-id="aad6c-120">然後，安全性 DLL 會根據使用者在私用安全性資料庫中的資訊來驗證回應。</span><span class="sxs-lookup"><span data-stu-id="aad6c-120">The security DLL then validates the response against the user's information in the private security database.</span></span>

<span data-ttu-id="aad6c-121">如果安全性 DLL 驗證遠端使用者，RAS 伺服器會執行自己的驗證。</span><span class="sxs-lookup"><span data-stu-id="aad6c-121">If the security DLL authenticates the remote user, the RAS server performs its own authentication.</span></span> <span data-ttu-id="aad6c-122">如此可確保 RAS 安全性一律會驗證遠端使用者，即使已安裝可授與存取權給所有使用者的安全性 DLL 也是如此。</span><span class="sxs-lookup"><span data-stu-id="aad6c-122">This ensures that RAS security always authenticates a remote user, even if a security DLL is installed that grants access to all users.</span></span>

> [!Note]  
> <span data-ttu-id="aad6c-123">Windows NT/Windows 2000 目前僅針對非同步數據機連線提供 RAS 安全性主機支援;不支援其他類型的連線（例如乙太網路 (）不是數據機連線) 、VPN (也不是數據機連線) ，或 (為同步) 的 ISDN。</span><span class="sxs-lookup"><span data-stu-id="aad6c-123">Windows NT/Windows 2000 currently provides RAS security host support only for asynchronous modem connections; other types of connections such as Ethernet (which is not a modem connection), VPN (which is also not a modem connection), or ISDN (which is synchronous), are not supported.</span></span>

 

 

 




