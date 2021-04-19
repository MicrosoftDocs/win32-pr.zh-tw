---
description: Windows SDK 包含可用於控制服務的命令列公用程式（Sc.exe）。 其命令會對應至 SCM 提供的函式。 語法如下所示。
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: 使用 SC 控制服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990393"
---
# <a name="controlling-a-service-using-sc"></a><span data-ttu-id="e48b5-105">使用 SC 控制服務</span><span class="sxs-lookup"><span data-stu-id="e48b5-105">Controlling a Service Using SC</span></span>

<span data-ttu-id="e48b5-106">Windows SDK 包含可用於控制服務的命令列公用程式（Sc.exe）。</span><span class="sxs-lookup"><span data-stu-id="e48b5-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to control a service.</span></span> <span data-ttu-id="e48b5-107">其命令會對應至 SCM 提供的函式。</span><span class="sxs-lookup"><span data-stu-id="e48b5-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="e48b5-108">語法如下所示。</span><span class="sxs-lookup"><span data-stu-id="e48b5-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48b5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e48b5-109">Syntax</span></span>

<span data-ttu-id="e48b5-110">**sc** \[*ServerName* \]*命令* \[ \] ServiceName \[ \] option1 \[*option2* \]...</span><span class="sxs-lookup"><span data-stu-id="e48b5-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="e48b5-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span><span class="sxs-lookup"><span data-stu-id="e48b5-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="e48b5-112">選用的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e48b5-112">Optional server name.</span></span> <span data-ttu-id="e48b5-113">使用表單 \\ \\ *ServerName*。</span><span class="sxs-lookup"><span data-stu-id="e48b5-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="e48b5-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*命令*</span><span class="sxs-lookup"><span data-stu-id="e48b5-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="e48b5-115">下列其中一個命令：</span><span class="sxs-lookup"><span data-stu-id="e48b5-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="e48b5-116">continue</span><span class="sxs-lookup"><span data-stu-id="e48b5-116">continue</span></span></dd> <dd><span data-ttu-id="e48b5-117">控制</span><span class="sxs-lookup"><span data-stu-id="e48b5-117">control</span></span></dd> <dd><span data-ttu-id="e48b5-118">審問</span><span class="sxs-lookup"><span data-stu-id="e48b5-118">interrogate</span></span></dd> <dd><span data-ttu-id="e48b5-119">pause</span><span class="sxs-lookup"><span data-stu-id="e48b5-119">pause</span></span></dd> <dd><span data-ttu-id="e48b5-120">start</span><span class="sxs-lookup"><span data-stu-id="e48b5-120">start</span></span></dd> <dd><span data-ttu-id="e48b5-121">stop</span><span class="sxs-lookup"><span data-stu-id="e48b5-121">stop</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="e48b5-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="e48b5-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="e48b5-123">安裝時所指定的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e48b5-123">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="e48b5-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span><span class="sxs-lookup"><span data-stu-id="e48b5-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="e48b5-125">選用參數。</span><span class="sxs-lookup"><span data-stu-id="e48b5-125">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e48b5-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span><span class="sxs-lookup"><span data-stu-id="e48b5-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="e48b5-127">選用參數。</span><span class="sxs-lookup"><span data-stu-id="e48b5-127">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e48b5-128">備註</span><span class="sxs-lookup"><span data-stu-id="e48b5-128">Remarks</span></span>

<span data-ttu-id="e48b5-129">若要查看命令的完整語法，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="e48b5-129">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="e48b5-130">**sc** *命令*</span><span class="sxs-lookup"><span data-stu-id="e48b5-130">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="e48b5-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="e48b5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e48b5-132">服務控制要求</span><span class="sxs-lookup"><span data-stu-id="e48b5-132">Service Control Requests</span></span>](service-control-requests.md)
</dt> <dt>

[<span data-ttu-id="e48b5-133">服務啟動</span><span class="sxs-lookup"><span data-stu-id="e48b5-133">Service Startup</span></span>](service-startup.md)
</dt> </dl>

 

 



