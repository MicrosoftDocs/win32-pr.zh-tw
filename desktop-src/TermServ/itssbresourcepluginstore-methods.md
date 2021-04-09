---
title: ITsSbResourcePluginStore 方法
description: ITsSbResourcePluginStore 介面會公開下列方法。
ms.assetid: D3D59244-E319-47C8-A931-72679C11AC40
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c56d403bc681152a5076d6c219790b452bd749d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840291"
---
# <a name="itssbresourcepluginstore-methods"></a><span data-ttu-id="01594-103">ITsSbResourcePluginStore 方法</span><span class="sxs-lookup"><span data-stu-id="01594-103">ITsSbResourcePluginStore Methods</span></span>

<span data-ttu-id="01594-104">[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="01594-104">The [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="01594-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="01594-105">In this section</span></span>

-   [<span data-ttu-id="01594-106">**AcquireTargetLock 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-106">**AcquireTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)
-   [<span data-ttu-id="01594-107">**AddEnvironmentToStore 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-107">**AddEnvironmentToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)
-   [<span data-ttu-id="01594-108">**AddSessionToStore 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-108">**AddSessionToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)
-   [<span data-ttu-id="01594-109">**AddTargetToStore 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-109">**AddTargetToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)
-   [<span data-ttu-id="01594-110">**DeleteTarget 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-110">**DeleteTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)
-   [<span data-ttu-id="01594-111">**EnumerateEnvironments 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-111">**EnumerateEnvironments method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)
-   [<span data-ttu-id="01594-112">**EnumerateFarms 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-112">**EnumerateFarms method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)
-   [<span data-ttu-id="01594-113">**EnumerateSessions 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-113">**EnumerateSessions method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)
-   [<span data-ttu-id="01594-114">**EnumerateTargets 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-114">**EnumerateTargets method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)
-   [<span data-ttu-id="01594-115">**GetFarmProperty 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-115">**GetFarmProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)
-   [<span data-ttu-id="01594-116">**GetServerState 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-116">**GetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getserverstate)
-   [<span data-ttu-id="01594-117">**QueryEnvironment 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-117">**QueryEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)
-   [<span data-ttu-id="01594-118">**QuerySessionBySessionId 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-118">**QuerySessionBySessionId method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)
-   [<span data-ttu-id="01594-119">**QueryTarget 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-119">**QueryTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)
-   [<span data-ttu-id="01594-120">**ReleaseTargetLock 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-120">**ReleaseTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)
-   [<span data-ttu-id="01594-121">**RemoveEnvironmentFromStore 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-121">**RemoveEnvironmentFromStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)
-   [<span data-ttu-id="01594-122">**SaveEnvironment 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-122">**SaveEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)
-   [<span data-ttu-id="01594-123">**SaveSession 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-123">**SaveSession method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)
-   [<span data-ttu-id="01594-124">**SaveTarget 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-124">**SaveTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)
-   [<span data-ttu-id="01594-125">**SetEnvironmentProperty 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-125">**SetEnvironmentProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)
-   [<span data-ttu-id="01594-126">**SetEnvironmentPropertyWithVersionCheck 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-126">**SetEnvironmentPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck)
-   [<span data-ttu-id="01594-127">**SetServerDrainMode 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-127">**SetServerDrainMode method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverdrainmode)
-   [<span data-ttu-id="01594-128">**SetServerWaitingToStart 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-128">**SetServerWaitingToStart method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverwaitingtostart)
-   [<span data-ttu-id="01594-129">**SetSessionState 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-129">**SetSessionState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)
-   [<span data-ttu-id="01594-130">**SetTargetProperty 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-130">**SetTargetProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)
-   [<span data-ttu-id="01594-131">**SetTargetPropertyWithVersionCheck 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-131">**SetTargetPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)
-   [<span data-ttu-id="01594-132">**SetTargetState 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-132">**SetTargetState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)
-   [<span data-ttu-id="01594-133">**TestAndSetServerState 方法**</span><span class="sxs-lookup"><span data-stu-id="01594-133">**TestAndSetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-testandsetserverstate)

 

 




