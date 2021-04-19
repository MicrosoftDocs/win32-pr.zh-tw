---
description: Windows SDK 包含命令列公用程式（Sc.exe），可用來查詢或修改已安裝服務的資料庫。 其命令會對應至 SCM 提供的函式。 語法如下所示。
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: 使用 SC 設定服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991700"
---
# <a name="configuring-a-service-using-sc"></a><span data-ttu-id="b3138-105">使用 SC 設定服務</span><span class="sxs-lookup"><span data-stu-id="b3138-105">Configuring a Service Using SC</span></span>

<span data-ttu-id="b3138-106">Windows SDK 包含命令列公用程式（Sc.exe），可用來查詢或修改已安裝服務的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3138-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to query or modify the database of installed services.</span></span> <span data-ttu-id="b3138-107">其命令會對應至 SCM 提供的函式。</span><span class="sxs-lookup"><span data-stu-id="b3138-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="b3138-108">語法如下所示。</span><span class="sxs-lookup"><span data-stu-id="b3138-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3138-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3138-109">Syntax</span></span>

<span data-ttu-id="b3138-110">**sc** \[*ServerName* \]*命令* \[ \] ServiceName \[ \] option1 \[*option2* \]...</span><span class="sxs-lookup"><span data-stu-id="b3138-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="b3138-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span><span class="sxs-lookup"><span data-stu-id="b3138-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="b3138-112">選用的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b3138-112">Optional server name.</span></span> <span data-ttu-id="b3138-113">使用表單 \\ \\ *ServerName*。</span><span class="sxs-lookup"><span data-stu-id="b3138-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="b3138-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*命令*</span><span class="sxs-lookup"><span data-stu-id="b3138-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="b3138-115">下列其中一個命令：</span><span class="sxs-lookup"><span data-stu-id="b3138-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="b3138-116">boot</span><span class="sxs-lookup"><span data-stu-id="b3138-116">boot</span></span></dd> <dd><span data-ttu-id="b3138-117">config</span><span class="sxs-lookup"><span data-stu-id="b3138-117">config</span></span></dd> <dd><span data-ttu-id="b3138-118">建立</span><span class="sxs-lookup"><span data-stu-id="b3138-118">create</span></span></dd> <dd><span data-ttu-id="b3138-119">delete</span><span class="sxs-lookup"><span data-stu-id="b3138-119">delete</span></span></dd> <dd><span data-ttu-id="b3138-120">description</span><span class="sxs-lookup"><span data-stu-id="b3138-120">description</span></span></dd> <dd><span data-ttu-id="b3138-121">EnumDepend</span><span class="sxs-lookup"><span data-stu-id="b3138-121">EnumDepend</span></span></dd> <dd><span data-ttu-id="b3138-122">失敗</span><span class="sxs-lookup"><span data-stu-id="b3138-122">failure</span></span></dd> <dd><span data-ttu-id="b3138-123">failureflag</span><span class="sxs-lookup"><span data-stu-id="b3138-123">failureflag</span></span></dd> <dd><span data-ttu-id="b3138-124">GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="b3138-124">GetDisplayName</span></span></dd> <dd><span data-ttu-id="b3138-125">GetKeyName</span><span class="sxs-lookup"><span data-stu-id="b3138-125">GetKeyName</span></span></dd> <dd><span data-ttu-id="b3138-126">鎖定</span><span class="sxs-lookup"><span data-stu-id="b3138-126">Lock</span></span></dd> <dd><span data-ttu-id="b3138-127">qc</span><span class="sxs-lookup"><span data-stu-id="b3138-127">qc</span></span></dd> <dd><span data-ttu-id="b3138-128">qdescription</span><span class="sxs-lookup"><span data-stu-id="b3138-128">qdescription</span></span></dd> <dd><span data-ttu-id="b3138-129">qfailure</span><span class="sxs-lookup"><span data-stu-id="b3138-129">qfailure</span></span></dd> <dd><span data-ttu-id="b3138-130">qfailureflag</span><span class="sxs-lookup"><span data-stu-id="b3138-130">qfailureflag</span></span></dd> <dd><span data-ttu-id="b3138-131">qprivs</span><span class="sxs-lookup"><span data-stu-id="b3138-131">qprivs</span></span></dd> <dd><span data-ttu-id="b3138-132">qsidtype</span><span class="sxs-lookup"><span data-stu-id="b3138-132">qsidtype</span></span></dd> <dd><span data-ttu-id="b3138-133">查詢</span><span class="sxs-lookup"><span data-stu-id="b3138-133">query</span></span></dd> <dd><span data-ttu-id="b3138-134">queryex</span><span class="sxs-lookup"><span data-stu-id="b3138-134">queryex</span></span></dd> <dd><span data-ttu-id="b3138-135">privs</span><span class="sxs-lookup"><span data-stu-id="b3138-135">privs</span></span></dd> <dd><span data-ttu-id="b3138-136">QueryLock</span><span class="sxs-lookup"><span data-stu-id="b3138-136">QueryLock</span></span></dd> <dd><span data-ttu-id="b3138-137">sdset</span><span class="sxs-lookup"><span data-stu-id="b3138-137">sdset</span></span></dd> <dd><span data-ttu-id="b3138-138">sdshow</span><span class="sxs-lookup"><span data-stu-id="b3138-138">sdshow</span></span></dd> <dd><span data-ttu-id="b3138-139">showsid</span><span class="sxs-lookup"><span data-stu-id="b3138-139">showsid</span></span></dd> <dd><span data-ttu-id="b3138-140">sidtype</span><span class="sxs-lookup"><span data-stu-id="b3138-140">sidtype</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="b3138-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="b3138-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="b3138-142">安裝時所指定的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b3138-142">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="b3138-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span><span class="sxs-lookup"><span data-stu-id="b3138-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="b3138-144">選用參數。</span><span class="sxs-lookup"><span data-stu-id="b3138-144">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b3138-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span><span class="sxs-lookup"><span data-stu-id="b3138-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="b3138-146">選用參數。</span><span class="sxs-lookup"><span data-stu-id="b3138-146">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3138-147">備註</span><span class="sxs-lookup"><span data-stu-id="b3138-147">Remarks</span></span>

<span data-ttu-id="b3138-148">若要查看命令的完整語法，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="b3138-148">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="b3138-149">**sc** *命令*</span><span class="sxs-lookup"><span data-stu-id="b3138-149">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3138-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3138-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3138-151">服務設定</span><span class="sxs-lookup"><span data-stu-id="b3138-151">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="b3138-152">服務安裝、移除和列舉</span><span class="sxs-lookup"><span data-stu-id="b3138-152">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



