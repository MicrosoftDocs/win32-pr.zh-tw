---
title: Web 應用程式 Proxy
description: Web 應用程式 Proxy
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104093424"
---
# <a name="web-application-proxy"></a><span data-ttu-id="cba09-103">Web 應用程式 Proxy</span><span class="sxs-lookup"><span data-stu-id="cba09-103">Web Application Proxy</span></span>

## <a name="platform"></a><span data-ttu-id="cba09-104">平台</span><span class="sxs-lookup"><span data-stu-id="cba09-104">Platform</span></span>

<span data-ttu-id="cba09-105">**伺服器-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cba09-105">**Servers -** Windows Server 2012 R2</span></span>  






## <a name="description"></a><span data-ttu-id="cba09-106">Description</span><span class="sxs-lookup"><span data-stu-id="cba09-106">Description</span></span>

<span data-ttu-id="cba09-107">在 Windows Server 2012 R2 中，我們在遠端存取角色下新增了稱為 Web 應用程式 Proxy 的新服務，可讓系統管理員發行應用程式以進行外部存取。</span><span class="sxs-lookup"><span data-stu-id="cba09-107">In Windows Server 2012 R2, we added a new service called the Web Application Proxy under the Remote Access role that allows administrators to publish applications for external access.</span></span> <span data-ttu-id="cba09-108">這種服務會作為反向 proxy，並做為 Active Directory 同盟服務 (AD FS) proxy。</span><span class="sxs-lookup"><span data-stu-id="cba09-108">This service acts as a reverse proxy and as an Active Directory Federation Services (AD FS) proxy.</span></span> <span data-ttu-id="cba09-109">事實上，這項服務會取代 Windows Server 2012 中已知的 AD FS proxy 服務。</span><span class="sxs-lookup"><span data-stu-id="cba09-109">In fact, this service replaces the AD FS proxy service as it was known in Windows Server 2012.</span></span>

<span data-ttu-id="cba09-110">使用 Web 應用程式 Proxy 時，組織可以讓內部部署 Web 資源可供外部存取，同時也能控制 AD FS 上的驗證和授權原則，藉此管理此存取的風險。</span><span class="sxs-lookup"><span data-stu-id="cba09-110">With the Web Application Proxy, an organization can make on-premises web resources available for external access while at the same time managing the risk of this access by controlling authentication and authorization policies on the AD FS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="cba09-111">表現</span><span class="sxs-lookup"><span data-stu-id="cba09-111">Manifestation</span></span>

<span data-ttu-id="cba09-112">AD FS proxy 服務已不再位於 Active Directory 同盟服務角色 (AD FS) ，但已由遠端存取角色下的 Web 應用程式 Proxy 取代。</span><span class="sxs-lookup"><span data-stu-id="cba09-112">The AD FS proxy service is no longer under the Active Directory Federation Services role (AD FS), but has been replaced by the Web Application Proxy under the Remote Access role.</span></span> <span data-ttu-id="cba09-113">這代表 AD FS proxy 服務的擴充，包括應用程式發行的反向 proxy 功能。</span><span class="sxs-lookup"><span data-stu-id="cba09-113">This represents an expansion of the AD FS proxy service by including reverse proxy functionality for application publishing.</span></span>

## <a name="solution"></a><span data-ttu-id="cba09-114">解決方法</span><span class="sxs-lookup"><span data-stu-id="cba09-114">Solution</span></span>

<span data-ttu-id="cba09-115">若要存取 Web 應用程式 Proxy，系統管理員可以移至伺服器管理員並新增角色/角色服務。</span><span class="sxs-lookup"><span data-stu-id="cba09-115">To access the Web Application Proxy, administrators can go to Server Manager and add a new role/role service.</span></span> <span data-ttu-id="cba09-116">系統管理員會在遠端存取角色下找到 Web 應用程式 Proxy。</span><span class="sxs-lookup"><span data-stu-id="cba09-116">The administrator will find the Web Application Proxy under the Remote Access role.</span></span>

## <a name="resources"></a><span data-ttu-id="cba09-117">資源</span><span class="sxs-lookup"><span data-stu-id="cba09-117">Resources</span></span>

-   <span data-ttu-id="cba09-118">[解決方案指南](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="cba09-118">[Solution guide](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span></span>

 

 