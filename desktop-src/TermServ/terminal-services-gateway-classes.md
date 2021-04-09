---
title: 遠端桌面閘道類別
description: 遠端桌面閘道 (RD 閘道) WMI 提供者提供下列類別。
ms.assetid: 482ba056-0de7-4c91-816c-dd3c926662ef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d17adca523833f3418661cd3f9851d7c814cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675060"
---
# <a name="remote-desktop-gateway-classes"></a><span data-ttu-id="a93e3-103">遠端桌面閘道類別</span><span class="sxs-lookup"><span data-stu-id="a93e3-103">Remote Desktop Gateway classes</span></span>

<span data-ttu-id="a93e3-104">遠端桌面閘道 (RD 閘道) WMI 提供者提供下列類別。</span><span class="sxs-lookup"><span data-stu-id="a93e3-104">The Remote Desktop Gateway (RD Gateway) WMI provider provides the following classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a93e3-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="a93e3-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a93e3-106">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="a93e3-106">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dd>

<span data-ttu-id="a93e3-107">代表從用戶端電腦到 RD 閘道伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="a93e3-107">Represents a connection from a client computer to a RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="a93e3-108">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="a93e3-108">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="a93e3-109">描述 (RD CAP) 的遠端桌面連線授權原則。</span><span class="sxs-lookup"><span data-stu-id="a93e3-109">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="a93e3-110">RD Cap 用來判斷是否允許使用者連線至 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="a93e3-110">RD CAPs are used to determine whether a user is allowed to connect to the RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="a93e3-111">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="a93e3-111">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dd>

<span data-ttu-id="a93e3-112">描述一組 RD 閘道負載平衡伺服器。</span><span class="sxs-lookup"><span data-stu-id="a93e3-112">Describes a set of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="a93e3-113">這些是用來在多部伺服器之間 RD 閘道連接之間進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="a93e3-113">These are used to load balance RD Gateway connections across multiple servers.</span></span>

</dd> <dt>

[<span data-ttu-id="a93e3-114">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="a93e3-114">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dd>

<span data-ttu-id="a93e3-115">描述遠端驗證撥入消費者服務 (RADIUS) 伺服器，其具有一組遠端桌面服務連線授權原則 (RD Cap) 。</span><span class="sxs-lookup"><span data-stu-id="a93e3-115">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

</dd> <dt>

[<span data-ttu-id="a93e3-116">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="a93e3-116">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="a93e3-117">描述 (RD RAP) 的遠端桌面資源授權原則。</span><span class="sxs-lookup"><span data-stu-id="a93e3-117">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="a93e3-118">RD RAP 用來決定是否授權使用者透過 RD 閘道連接到指定的資源。</span><span class="sxs-lookup"><span data-stu-id="a93e3-118">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="a93e3-119">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="a93e3-119">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dd>

<span data-ttu-id="a93e3-120">描述資源群組，這會將一組資源 (電腦名稱稱) 對應至單一實體。</span><span class="sxs-lookup"><span data-stu-id="a93e3-120">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

</dd> <dt>

[<span data-ttu-id="a93e3-121">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="a93e3-121">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> <dd>

<span data-ttu-id="a93e3-122">用於 RD 閘道伺服器特定的作業。</span><span class="sxs-lookup"><span data-stu-id="a93e3-122">Used for RD Gateway server-specific operations.</span></span>

</dd> <dt>

[<span data-ttu-id="a93e3-123">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="a93e3-123">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dd>

<span data-ttu-id="a93e3-124">提供方法和屬性來查看和設定 RD 閘道伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="a93e3-124">Provides methods and properties to view and configure RD Gateway server settings.</span></span>

</dd> </dl>

 

 




