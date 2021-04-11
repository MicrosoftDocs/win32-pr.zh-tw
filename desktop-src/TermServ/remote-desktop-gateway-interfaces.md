---
title: 遠端桌面閘道介面
description: 遠端桌面閘道 (RD 閘道) API 支援下列介面。 您可以使用這些介面來執行提供自訂驗證與授權的外掛程式。
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931943"
---
# <a name="remote-desktop-gateway-interfaces"></a><span data-ttu-id="6ee27-104">遠端桌面閘道介面</span><span class="sxs-lookup"><span data-stu-id="6ee27-104">Remote Desktop Gateway Interfaces</span></span>

<span data-ttu-id="6ee27-105">遠端桌面閘道 (RD 閘道) API 支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="6ee27-105">The Remote Desktop Gateway (RD Gateway) API supports the following interfaces.</span></span> <span data-ttu-id="6ee27-106">您可以使用這些介面來執行提供自訂驗證與授權的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="6ee27-106">You can use these interfaces to implement plug-ins that provide customized authentication and authorization.</span></span> <span data-ttu-id="6ee27-107">驗證外掛程式與授權外掛程式之間沒有相依性，而且您可以在選擇的情況下，只執行一個外掛程式。</span><span class="sxs-lookup"><span data-stu-id="6ee27-107">There is no dependency between the authentication plug-in and the authorization plug-in, and you can implement only a single plug-in if you choose.</span></span>

<span data-ttu-id="6ee27-108">驗證外掛程式為 [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) 和 [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)。</span><span class="sxs-lookup"><span data-stu-id="6ee27-108">The authentication plug-ins are [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) and [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span></span>

<span data-ttu-id="6ee27-109">授權外掛程式為 [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)、 [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)、 [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)和 [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)。</span><span class="sxs-lookup"><span data-stu-id="6ee27-109">The authorization plug-ins are [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink), and [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6ee27-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="6ee27-110">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6ee27-111">**ITSGAccountingEngine**</span><span class="sxs-lookup"><span data-stu-id="6ee27-111">**ITSGAccountingEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

<span data-ttu-id="6ee27-112">公開方法，以提供有關建立或關閉連接之會話的資訊。</span><span class="sxs-lookup"><span data-stu-id="6ee27-112">Exposes methods that provide information about the creation or closing of sessions for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6ee27-113">**ITSGAuthenticateUserSink**</span><span class="sxs-lookup"><span data-stu-id="6ee27-113">**ITSGAuthenticateUserSink**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

<span data-ttu-id="6ee27-114">公開通知 RD 閘道有關驗證事件的方法。</span><span class="sxs-lookup"><span data-stu-id="6ee27-114">Exposes methods that notify RD Gateway about authentication events.</span></span>

</dd> <dt>

[<span data-ttu-id="6ee27-115">**ITSGAuthenticationEngine**</span><span class="sxs-lookup"><span data-stu-id="6ee27-115">**ITSGAuthenticationEngine**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

<span data-ttu-id="6ee27-116">公開驗證使用者以進行 RD 閘道的方法。</span><span class="sxs-lookup"><span data-stu-id="6ee27-116">Exposes methods that authenticate users for RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="6ee27-117">**ITSGAuthorizeConnectionSink**</span><span class="sxs-lookup"><span data-stu-id="6ee27-117">**ITSGAuthorizeConnectionSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

<span data-ttu-id="6ee27-118">公開通知 RD 閘道有關嘗試授權連接之結果的方法。</span><span class="sxs-lookup"><span data-stu-id="6ee27-118">Exposes methods that notify RD Gateway about the result of an attempt to authorize a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6ee27-119">**ITSGAuthorizeResourceSink**</span><span class="sxs-lookup"><span data-stu-id="6ee27-119">**ITSGAuthorizeResourceSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

<span data-ttu-id="6ee27-120">公開方法，以通知 RD 閘道有關嘗試授權資源的結果。</span><span class="sxs-lookup"><span data-stu-id="6ee27-120">Exposes methods that notify RD Gateway about the result of an attempt to authorize a resource.</span></span>

</dd> <dt>

[<span data-ttu-id="6ee27-121">**ITSGPolicyEngine**</span><span class="sxs-lookup"><span data-stu-id="6ee27-121">**ITSGPolicyEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

<span data-ttu-id="6ee27-122">公開授權連接和資源的方法。</span><span class="sxs-lookup"><span data-stu-id="6ee27-122">Exposes methods that authorize connections and resources.</span></span>

</dd> </dl>

 

 




