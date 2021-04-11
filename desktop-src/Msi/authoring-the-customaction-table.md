---
description: 針對在上一節中建立的五個範例自訂動作，輸入 CustomAction 資料表的記錄。 如需有關如何為這種類型的自訂動作填入 CustomAction 資料表的詳細資訊，請參閱自訂動作類型1。
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: 撰寫 CustomAction 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944005"
---
# <a name="authoring-the-customaction-table"></a><span data-ttu-id="a3fd1-104">撰寫 CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="a3fd1-104">Authoring the CustomAction Table</span></span>

<span data-ttu-id="a3fd1-105">針對在上一節中建立的五個範例自訂動作，輸入 [CustomAction 資料表](customaction-table.md)的記錄。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-105">Enter records for the five sample custom actions created in the previous section to the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="a3fd1-106">如需有關如何為這種類型的自訂動作填入 CustomAction 資料表的詳細資訊，請參閱 [自訂動作類型 1](custom-action-type-1.md)。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-106">For more information on how to populate the CustomAction table for this type of custom action see [Custom Action Type 1](custom-action-type-1.md).</span></span>

[<span data-ttu-id="a3fd1-107">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="a3fd1-107">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="a3fd1-108">動作</span><span class="sxs-lookup"><span data-stu-id="a3fd1-108">Action</span></span>            | <span data-ttu-id="a3fd1-109">類型</span><span class="sxs-lookup"><span data-stu-id="a3fd1-109">Type</span></span>  | <span data-ttu-id="a3fd1-110">來源</span><span class="sxs-lookup"><span data-stu-id="a3fd1-110">Source</span></span>      | <span data-ttu-id="a3fd1-111">目標</span><span class="sxs-lookup"><span data-stu-id="a3fd1-111">Target</span></span>                |
|-------------------|-------|-------------|-----------------------|
| <span data-ttu-id="a3fd1-112">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="a3fd1-112">ProcessAccounts</span></span>   | <span data-ttu-id="a3fd1-113">1</span><span class="sxs-lookup"><span data-stu-id="a3fd1-113">1</span></span>     | <span data-ttu-id="a3fd1-114">Process.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-114">Process.dll</span></span> | <span data-ttu-id="a3fd1-115">ProcessUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a3fd1-115">ProcessUserAccounts</span></span>   |
| <span data-ttu-id="a3fd1-116">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="a3fd1-116">UninstallAccounts</span></span> | <span data-ttu-id="a3fd1-117">1</span><span class="sxs-lookup"><span data-stu-id="a3fd1-117">1</span></span>     | <span data-ttu-id="a3fd1-118">Process.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-118">Process.dll</span></span> | <span data-ttu-id="a3fd1-119">UninstallUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a3fd1-119">UninstallUserAccounts</span></span> |
| <span data-ttu-id="a3fd1-120">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="a3fd1-120">CreateAccount</span></span>     | <span data-ttu-id="a3fd1-121">11265</span><span class="sxs-lookup"><span data-stu-id="a3fd1-121">11265</span></span> | <span data-ttu-id="a3fd1-122">Create.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-122">Create.dll</span></span>  | <span data-ttu-id="a3fd1-123">CreateUserAccount</span><span class="sxs-lookup"><span data-stu-id="a3fd1-123">CreateUserAccount</span></span>     |
| <span data-ttu-id="a3fd1-124">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="a3fd1-124">RemoveAccount</span></span>     | <span data-ttu-id="a3fd1-125">11265</span><span class="sxs-lookup"><span data-stu-id="a3fd1-125">11265</span></span> | <span data-ttu-id="a3fd1-126">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-126">Remove.dll</span></span>  | <span data-ttu-id="a3fd1-127">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="a3fd1-127">RemoveUserAccount</span></span>     |
| <span data-ttu-id="a3fd1-128">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="a3fd1-128">RollbackAccount</span></span>   | <span data-ttu-id="a3fd1-129">9473</span><span class="sxs-lookup"><span data-stu-id="a3fd1-129">9473</span></span>  | <span data-ttu-id="a3fd1-130">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-130">Remove.dll</span></span>  | <span data-ttu-id="a3fd1-131">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="a3fd1-131">RemoveUserAccount</span></span>     |



 

<span data-ttu-id="a3fd1-132">Windows Installer SDK 提供動態連結程式庫的 c + + 原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-132">The C++ source code for the dynamic-link libraries are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="a3fd1-133">使用進程 .cpp 來建立檔案 Process.dll。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-133">Use Process.cpp to create the file Process.dll.</span></span> <span data-ttu-id="a3fd1-134">使用 Create .cpp Create.dll 建立檔案。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-134">Use Create.cpp to create the file Create.dll.</span></span> <span data-ttu-id="a3fd1-135">您可以使用 Remove .cpp 來建立 Remove.dll。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-135">Use Remove.cpp to create Remove.dll.</span></span> <span data-ttu-id="a3fd1-136">將這些動態連結程式庫檔案新增至二進位資料表。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-136">Add these dynamic-link library files to the Binary table.</span></span>

[<span data-ttu-id="a3fd1-137">二進位資料表</span><span class="sxs-lookup"><span data-stu-id="a3fd1-137">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="a3fd1-138">Name</span><span class="sxs-lookup"><span data-stu-id="a3fd1-138">Name</span></span>        | <span data-ttu-id="a3fd1-139">資料</span><span class="sxs-lookup"><span data-stu-id="a3fd1-139">Data</span></span>            |
|-------------|-----------------|
| <span data-ttu-id="a3fd1-140">Process.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-140">Process.dll</span></span> | <span data-ttu-id="a3fd1-141">{*二進位資料*}</span><span class="sxs-lookup"><span data-stu-id="a3fd1-141">{*binary data*}</span></span> |
| <span data-ttu-id="a3fd1-142">Create.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-142">Create.dll</span></span>  | <span data-ttu-id="a3fd1-143">{*二進位資料*}</span><span class="sxs-lookup"><span data-stu-id="a3fd1-143">{*binary data*}</span></span> |
| <span data-ttu-id="a3fd1-144">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="a3fd1-144">Remove.dll</span></span>  | <span data-ttu-id="a3fd1-145">{*二進位資料*}</span><span class="sxs-lookup"><span data-stu-id="a3fd1-145">{*binary data*}</span></span> |



 

<span data-ttu-id="a3fd1-146">繼續 [新增自訂 CustomUserAccounts 資料表](adding-a-custom-customuseraccounts-table.md)。</span><span class="sxs-lookup"><span data-stu-id="a3fd1-146">Continue to [Adding a Custom CustomUserAccounts Table](adding-a-custom-customuseraccounts-table.md).</span></span>

 

 



