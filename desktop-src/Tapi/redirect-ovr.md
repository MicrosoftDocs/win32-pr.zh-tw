---
description: 會話重新導向可讓應用程式在不接聽來電的情況下，將提供的會話轉移到另一個位址。
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: 重新導向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695847"
---
# <a name="redirect"></a><span data-ttu-id="ffe14-103">重新導向</span><span class="sxs-lookup"><span data-stu-id="ffe14-103">Redirect</span></span>

<span data-ttu-id="ffe14-104">會話重新導向可讓應用程式在不接聽來電的情況下，將提供的會話轉移到另一個位址。</span><span class="sxs-lookup"><span data-stu-id="ffe14-104">Session redirection allows an application to deflect an offered session to another address without answering the call.</span></span> <span data-ttu-id="ffe14-105">應用程式可以依呼叫逐一執行重新導向。</span><span class="sxs-lookup"><span data-stu-id="ffe14-105">The application can do redirection on a call-by-call basis.</span></span> <span data-ttu-id="ffe14-106">例如，應用程式可能會允許使用者根據呼叫者識別碼資訊指定不同的重新導向。</span><span class="sxs-lookup"><span data-stu-id="ffe14-106">For example, an application might allow a user to specify different redirections based on caller ID information.</span></span> <span data-ttu-id="ffe14-107">成功重新導向呼叫之後，狀態通常會轉換成閒置，而且必須釋放相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="ffe14-107">After a call has been successfully redirected, the state typically transitions to idle and associated resources must be released.</span></span>

<span data-ttu-id="ffe14-108">重新導向與 [轉寄](forward-ovr.md) 不同之處在于，在設定轉送之後，此作業會由 TAPI、服務提供者或交換器執行，而不需要進一步參與應用程式。</span><span class="sxs-lookup"><span data-stu-id="ffe14-108">Redirect differs from [forward](forward-ovr.md) in that once forwarding has been set up, the operation is performed by TAPI, the service provider, or the switch without further involvement of the application.</span></span> <span data-ttu-id="ffe14-109">重新導向與 [傳輸](transfer-ovr.md) 不同，因為重新導向不需要先接聽呼叫。</span><span class="sxs-lookup"><span data-stu-id="ffe14-109">Redirect differs from [transfer](transfer-ovr.md) in that redirect does not require answering the call first.</span></span>

<span data-ttu-id="ffe14-110">並非所有服務提供者都支援使用這項作業。</span><span class="sxs-lookup"><span data-stu-id="ffe14-110">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="ffe14-111">**TAPI 2.x：** 請參閱 [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect)。</span><span class="sxs-lookup"><span data-stu-id="ffe14-111">**TAPI 2.x:** See [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span></span>

 

 
