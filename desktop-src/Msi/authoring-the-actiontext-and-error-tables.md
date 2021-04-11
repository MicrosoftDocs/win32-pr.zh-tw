---
description: 範例規格包括在自訂動作建立或移除使用者帳戶時傳送 ActionData 訊息，以及在無法建立帳戶時報告錯誤。
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: 撰寫 ActionText 和錯誤資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848958"
---
# <a name="authoring-the-actiontext-and-error-tables"></a><span data-ttu-id="d5b89-103">撰寫 ActionText 和錯誤資料表</span><span class="sxs-lookup"><span data-stu-id="d5b89-103">Authoring the ActionText and Error Tables</span></span>

<span data-ttu-id="d5b89-104">範例規格包括在自訂動作建立或移除使用者帳戶時傳送 ActionData 訊息，以及在無法建立帳戶時報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5b89-104">The sample specifications include sending ActionData messages when a custom action creates or removes a user account, and reporting an error if an account cannot be created.</span></span>

<span data-ttu-id="d5b89-105">在 ActionText 資料表中輸入下列專案，以提供 ActionText 訊息所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="d5b89-105">Enter the following entries into the ActionText table to provide information used by ActionText messages.</span></span>

[<span data-ttu-id="d5b89-106">ActionText 資料表</span><span class="sxs-lookup"><span data-stu-id="d5b89-106">ActionText Table</span></span>](actiontext-table.md)



| <span data-ttu-id="d5b89-107">動作</span><span class="sxs-lookup"><span data-stu-id="d5b89-107">Action</span></span>            | <span data-ttu-id="d5b89-108">描述</span><span class="sxs-lookup"><span data-stu-id="d5b89-108">Description</span></span>                                                       | <span data-ttu-id="d5b89-109">範本</span><span class="sxs-lookup"><span data-stu-id="d5b89-109">Template</span></span>                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="d5b89-110">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="d5b89-110">ProcessAccounts</span></span>   | <span data-ttu-id="d5b89-111">正在產生可在本機電腦上建立使用者帳戶的動作。</span><span class="sxs-lookup"><span data-stu-id="d5b89-111">Generating actions to create user accounts on the local computer.</span></span> | <span data-ttu-id="d5b89-112">帳戶： \[ 1 \] ，屬性： \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d5b89-112">Account: \[1\], Attributes: \[2\]</span></span> |
| <span data-ttu-id="d5b89-113">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="d5b89-113">CreateAccount</span></span>     | <span data-ttu-id="d5b89-114">在本機電腦上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d5b89-114">Creating user account on the local computer.</span></span>                      | <span data-ttu-id="d5b89-115">帳戶： \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d5b89-115">Account: \[1\]</span></span>                    |
| <span data-ttu-id="d5b89-116">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="d5b89-116">RemoveAccount</span></span>     | <span data-ttu-id="d5b89-117">正在從本機電腦移除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d5b89-117">Removing user account from the local computer.</span></span>                    | <span data-ttu-id="d5b89-118">帳戶： \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d5b89-118">Account: \[1\]</span></span>                    |
| <span data-ttu-id="d5b89-119">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="d5b89-119">RollbackAccount</span></span>   | <span data-ttu-id="d5b89-120">正在復原在本機電腦上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d5b89-120">Rolling back the creation of user accounts on the local computer.</span></span> | <span data-ttu-id="d5b89-121">帳戶： \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d5b89-121">Account: \[1\]</span></span>                    |
| <span data-ttu-id="d5b89-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="d5b89-122">UninstallAccounts</span></span> | <span data-ttu-id="d5b89-123">產生動作以移除本機電腦上的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d5b89-123">Generating actions to remove user accounts on the local computer.</span></span> | <span data-ttu-id="d5b89-124">帳戶： \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d5b89-124">Account: \[1\]</span></span>                    |



 

<span data-ttu-id="d5b89-125">在錯誤資料表中輸入下列專案，以提供錯誤報表所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="d5b89-125">Enter the following entries into the Error table to provide information used by error reporting.</span></span>

[<span data-ttu-id="d5b89-126">錯誤資料表</span><span class="sxs-lookup"><span data-stu-id="d5b89-126">Error Table</span></span>](error-table.md)



| <span data-ttu-id="d5b89-127">錯誤</span><span class="sxs-lookup"><span data-stu-id="d5b89-127">Error</span></span> | <span data-ttu-id="d5b89-128">訊息</span><span class="sxs-lookup"><span data-stu-id="d5b89-128">Message</span></span>                                                                        |
|-------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d5b89-129">25001</span><span class="sxs-lookup"><span data-stu-id="d5b89-129">25001</span></span> | <span data-ttu-id="d5b89-130">無法 \[ 在本機電腦上建立使用者帳戶 ' 2 \] '。</span><span class="sxs-lookup"><span data-stu-id="d5b89-130">Unable to create user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="d5b89-131">錯誤碼： \[ 3 \] 。</span><span class="sxs-lookup"><span data-stu-id="d5b89-131">Error Code: \[3\].</span></span> |
| <span data-ttu-id="d5b89-132">25002</span><span class="sxs-lookup"><span data-stu-id="d5b89-132">25002</span></span> | <span data-ttu-id="d5b89-133">\[ \] 本機電腦上已有使用者帳戶 ' 2 '。</span><span class="sxs-lookup"><span data-stu-id="d5b89-133">User account '\[2\]' already exists on the local machine.</span></span>                      |
| <span data-ttu-id="d5b89-134">25003</span><span class="sxs-lookup"><span data-stu-id="d5b89-134">25003</span></span> | <span data-ttu-id="d5b89-135">無法移除 \[ \] 本機電腦上的使用者帳戶 ' 2 '。</span><span class="sxs-lookup"><span data-stu-id="d5b89-135">Unable to remove user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="d5b89-136">錯誤碼： \[ 3 \] 。</span><span class="sxs-lookup"><span data-stu-id="d5b89-136">Error Code: \[3\].</span></span> |
| <span data-ttu-id="d5b89-137">25004</span><span class="sxs-lookup"><span data-stu-id="d5b89-137">25004</span></span> | <span data-ttu-id="d5b89-138">使用者帳戶 ' \[ 2 \] ' 不存在於本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="d5b89-138">User account '\[2\]' does not exist on the local machine.</span></span>                      |



 

<span data-ttu-id="d5b89-139">繼續 [撰寫 InstallExecuteSequence 資料表](authoring-the-installexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="d5b89-139">Continue to [Authoring the InstallExecuteSequence Table](authoring-the-installexecutesequence-table.md).</span></span>

 

 



