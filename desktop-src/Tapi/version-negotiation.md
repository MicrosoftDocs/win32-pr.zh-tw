---
description: 經過一段時間後，TAPI 應用程式、TAPI 和服務提供者可能會有不同的版本。
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: 版本交涉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945030"
---
# <a name="version-negotiation"></a><span data-ttu-id="aa38c-103">版本交涉</span><span class="sxs-lookup"><span data-stu-id="aa38c-103">Version Negotiation</span></span>

<span data-ttu-id="aa38c-104">經過一段時間後，TAPI 應用程式、TAPI 和服務提供者可能會有不同的版本。</span><span class="sxs-lookup"><span data-stu-id="aa38c-104">Over time, different versions may exist for TAPI applications, TAPI, and the service providers.</span></span> <span data-ttu-id="aa38c-105">TAPI 應用程式的最佳互通性需要知道應用程式的 TAPI 版本，也需要知道 TAPI DLL、TAPISVR 和服務提供者版本。</span><span class="sxs-lookup"><span data-stu-id="aa38c-105">Optimal interoperability of a TAPI application requires knowledge of not just the application's TAPI version, but also of the TAPI DLL, TAPISVR, and service provider versions.</span></span>

<span data-ttu-id="aa38c-106">無法進行適當的版本協商可能會導致嚴重的問題。</span><span class="sxs-lookup"><span data-stu-id="aa38c-106">Failure to do proper version negotiation can result in serious problems.</span></span> <span data-ttu-id="aa38c-107">例如，某些大量使用的結構會將資料成員從某個版本新增至下一個版本。</span><span class="sxs-lookup"><span data-stu-id="aa38c-107">For example, some heavily used structures have data members added from one version to the next.</span></span> <span data-ttu-id="aa38c-108">如果結構大小不符合應用程式或 TAPI 預期的大小，則結果的範圍是從記憶體流失到間歇性的 AVs。</span><span class="sxs-lookup"><span data-stu-id="aa38c-108">If the structure size does not match what the application or TAPI expects, the consequences range from memory leaks to intermittent AVs.</span></span>

<span data-ttu-id="aa38c-109">如需詳細資訊，請參閱 [TAPI 版本](./tapi-versioning.md)設定。</span><span class="sxs-lookup"><span data-stu-id="aa38c-109">For additional information, see [TAPI Versioning](./tapi-versioning.md).</span></span>

<span data-ttu-id="aa38c-110">**TAPI 2.x：** 在 [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)期間，應用程式會與 TAPI 和 TAPISVR 協調。</span><span class="sxs-lookup"><span data-stu-id="aa38c-110">**TAPI 2.x:** Applications negotiate with TAPI and TAPISVR during [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span> <span data-ttu-id="aa38c-111">應用程式會針對應用程式可能會使用的每一行呼叫 [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) ，以對服務提供者執行裝置的協商。</span><span class="sxs-lookup"><span data-stu-id="aa38c-111">Applications perform device negotiation with service providers by calling [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) for each line that the application might use.</span></span>

<span data-ttu-id="aa38c-112">**TAPI 3.x：** 不需要執行版本協商;不過，您可以使用 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來判斷介面是否可在其版本上使用。</span><span class="sxs-lookup"><span data-stu-id="aa38c-112">**TAPI 3.x:** There is no need to perform version negotiation; however, you can use [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to determine if an interface is available on their version.</span></span>

 

 
