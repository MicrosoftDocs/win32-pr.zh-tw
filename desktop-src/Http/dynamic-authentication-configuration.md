---
title: 動態驗證設定
description: 應用程式可以隨時變更 URL 群組或伺服器會話的驗證設定。
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300327"
---
# <a name="dynamic-authentication-configuration"></a><span data-ttu-id="39ac2-103">動態驗證設定</span><span class="sxs-lookup"><span data-stu-id="39ac2-103">Dynamic Authentication Configuration</span></span>

<span data-ttu-id="39ac2-104">根據預設，HTTP 伺服器 API 不會執行驗證，除非應用程式明確啟用它。</span><span class="sxs-lookup"><span data-stu-id="39ac2-104">By default, the HTTP Server API does not perform authentication unless the application specifically enables it.</span></span> <span data-ttu-id="39ac2-105">應用程式可以隨時變更 URL 群組或伺服器會話的驗證設定。</span><span class="sxs-lookup"><span data-stu-id="39ac2-105">Applications can change authentication configurations on a URL Group or server session at any time.</span></span> <span data-ttu-id="39ac2-106">驗證設定的變更不會影響已經過驗證或正在分派至應用程式的要求</span><span class="sxs-lookup"><span data-stu-id="39ac2-106">Changes to the authentication configuration do not affect requests that are already authenticated or being dispatched to the application</span></span>

<span data-ttu-id="39ac2-107">針對需要多次交握的驗證配置，如果目前的配置因為應用程式的設定變更而不再受支援，則 HTTP 伺服器 API 會卸載驗證交握。</span><span class="sxs-lookup"><span data-stu-id="39ac2-107">For authentication schemes where multiple rounds of handshake are required, the HTTP Server API drops the authentication handshake if the current scheme is no longer supported due to configuration changes from the application.</span></span> <span data-ttu-id="39ac2-108">例如，如果應用程式啟用 Negotiate 並停用 NTLM，而 HTTP 伺服器 API 在 NTLM 的中繼驗證交握中，則會捨棄 NTLM 的交握，並將要求傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="39ac2-108">For example, if the application enables Negotiate and disables NTLM, and the HTTP Server API is in the intermediate authentication handshake for NTLM, the handshake for NTLM is discarded and the request is passed to the application.</span></span> <span data-ttu-id="39ac2-109">應用程式會使用 WWW-Authenticate 標頭中指定的新驗證類型來傳送401驗證挑戰。</span><span class="sxs-lookup"><span data-stu-id="39ac2-109">The application sends a 401 authentication challenge with the new authentication types specified in the WWW-Authenticate header.</span></span>

 

 




