---
description: 範例的規格是從安裝資料庫中的自訂資料表讀取使用者帳戶資訊，而不是硬式編碼為自訂動作。
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: 新增自訂 CustomUserAccounts 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975052"
---
# <a name="adding-a-custom-customuseraccounts-table"></a><span data-ttu-id="00ceb-103">新增自訂 CustomUserAccounts 資料表</span><span class="sxs-lookup"><span data-stu-id="00ceb-103">Adding a Custom CustomUserAccounts Table</span></span>

<span data-ttu-id="00ceb-104">範例的規格是從安裝資料庫中的自訂資料表讀取使用者帳戶資訊，而不是硬式編碼為自訂動作。</span><span class="sxs-lookup"><span data-stu-id="00ceb-104">A specification of the sample is that user account information be read from a custom table in the installation database and not hard-coded into the custom action.</span></span>

<span data-ttu-id="00ceb-105">將自訂資料表新增至名為 CustomUserAccounts 的範例安裝資料庫，以保存使用者帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="00ceb-105">Add a custom table to the sample installation database named CustomUserAccounts to hold user account information.</span></span> <span data-ttu-id="00ceb-106">如需如何加入自訂資料表的範例，請參閱 [使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md) 。</span><span class="sxs-lookup"><span data-stu-id="00ceb-106">See [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md) for an example of how to add a custom table.</span></span> <span data-ttu-id="00ceb-107">針對 CustomUserAccounts 資料表使用下列架構。</span><span class="sxs-lookup"><span data-stu-id="00ceb-107">Use the following schema for the CustomUserAccounts table.</span></span> <span data-ttu-id="00ceb-108">如需資料行類型的說明，請參閱資料 [行定義格式](column-definition-format.md) 。</span><span class="sxs-lookup"><span data-stu-id="00ceb-108">See [Column Definition Format](column-definition-format.md) for an explanation of the column types.</span></span>



| <span data-ttu-id="00ceb-109">Column</span><span class="sxs-lookup"><span data-stu-id="00ceb-109">Column</span></span>     | <span data-ttu-id="00ceb-110">類型</span><span class="sxs-lookup"><span data-stu-id="00ceb-110">Type</span></span> | <span data-ttu-id="00ceb-111">答案</span><span class="sxs-lookup"><span data-stu-id="00ceb-111">Key</span></span> | <span data-ttu-id="00ceb-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="00ceb-112">Nullable</span></span> | <span data-ttu-id="00ceb-113">描述</span><span class="sxs-lookup"><span data-stu-id="00ceb-113">Description</span></span>                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ceb-114">UserName</span><span class="sxs-lookup"><span data-stu-id="00ceb-114">UserName</span></span>   | <span data-ttu-id="00ceb-115">s72</span><span class="sxs-lookup"><span data-stu-id="00ceb-115">s72</span></span>  | <span data-ttu-id="00ceb-116">Y</span><span class="sxs-lookup"><span data-stu-id="00ceb-116">Y</span></span>   | <span data-ttu-id="00ceb-117">N</span><span class="sxs-lookup"><span data-stu-id="00ceb-117">N</span></span>        | <span data-ttu-id="00ceb-118">正在建立之使用者帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="00ceb-118">Name of user account being created.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="00ceb-119">密碼</span><span class="sxs-lookup"><span data-stu-id="00ceb-119">Password</span></span>   | <span data-ttu-id="00ceb-120">s72</span><span class="sxs-lookup"><span data-stu-id="00ceb-120">s72</span></span>  |     | <span data-ttu-id="00ceb-121">N</span><span class="sxs-lookup"><span data-stu-id="00ceb-121">N</span></span>        | <span data-ttu-id="00ceb-122">包含帳戶密碼的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="00ceb-122">Name of property containing the password for the account.</span></span> <span data-ttu-id="00ceb-123">這是在命令列上或透過使用者介面中的[編輯控制項](edit-control.md)設定的[公用屬性](public-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="00ceb-123">This is a [public property](public-properties.md) set on the command line or through an [edit control](edit-control.md) in the user interface.</span></span> <span data-ttu-id="00ceb-124">此編輯控制項應具有 [密碼控制項屬性](password-control-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="00ceb-124">This edit control should have the [Password Control Attribute](password-control-attribute.md).</span></span> |
| <span data-ttu-id="00ceb-125">屬性</span><span class="sxs-lookup"><span data-stu-id="00ceb-125">Attributes</span></span> | <span data-ttu-id="00ceb-126">i4</span><span class="sxs-lookup"><span data-stu-id="00ceb-126">i4</span></span>   |     | <span data-ttu-id="00ceb-127">Y</span><span class="sxs-lookup"><span data-stu-id="00ceb-127">Y</span></span>        | <span data-ttu-id="00ceb-128">帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="00ceb-128">Attributes for account.</span></span> <span data-ttu-id="00ceb-129">這些會定義為 \_ 使用者 \_ 資訊1結構之 usri1 旗標成員的 DWORD 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="00ceb-129">These are defined as the **DWORD** values for the usri1\_flags member of the USER\_INFO\_1 structure.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="00ceb-130">將 CustomUserAccounts 資料表加入至資料庫之後，您可以使用 Orca、Windows Installer SDK 提供的資料表編輯器或其他編輯器來編輯此資料表。</span><span class="sxs-lookup"><span data-stu-id="00ceb-130">After the CustomUserAccounts table has been added to the database you may edit this table using Orca, a table editor provided with the Windows Installer SDK, or another editor.</span></span> <span data-ttu-id="00ceb-131">在 CustomUserAccounts 資料表中輸入下列記錄，為名為 TestUser 的使用者建立密碼安全的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="00ceb-131">Enter the following record in the CustomUserAccounts table to create a password secured user account for a user called TestUser.</span></span> <span data-ttu-id="00ceb-132">請注意，512是 UF \_ 標準帳戶的數值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="00ceb-132">Note that 512 is the numeric value for UF\_NORMAL\_ACCOUNT.</span></span>

<span data-ttu-id="00ceb-133">CustomUserAccounts 資料表</span><span class="sxs-lookup"><span data-stu-id="00ceb-133">CustomUserAccounts Table</span></span>



| <span data-ttu-id="00ceb-134">UserName</span><span class="sxs-lookup"><span data-stu-id="00ceb-134">UserName</span></span> | <span data-ttu-id="00ceb-135">密碼</span><span class="sxs-lookup"><span data-stu-id="00ceb-135">Password</span></span>         | <span data-ttu-id="00ceb-136">屬性</span><span class="sxs-lookup"><span data-stu-id="00ceb-136">Attributes</span></span> |
|----------|------------------|------------|
| <span data-ttu-id="00ceb-137">TestUser</span><span class="sxs-lookup"><span data-stu-id="00ceb-137">TestUser</span></span> | <span data-ttu-id="00ceb-138">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="00ceb-138">TESTUSERPASSWORD</span></span> | <span data-ttu-id="00ceb-139">512</span><span class="sxs-lookup"><span data-stu-id="00ceb-139">512</span></span>        |



 

<span data-ttu-id="00ceb-140">將下列記錄加入 \_ 自訂資料表的驗證資料表中。</span><span class="sxs-lookup"><span data-stu-id="00ceb-140">Add the following records to the \_Validation table for the custom table.</span></span>

[<span data-ttu-id="00ceb-141">\_驗證資料表</span><span class="sxs-lookup"><span data-stu-id="00ceb-141">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="00ceb-142">資料表</span><span class="sxs-lookup"><span data-stu-id="00ceb-142">Table</span></span>              | <span data-ttu-id="00ceb-143">資料行</span><span class="sxs-lookup"><span data-stu-id="00ceb-143">Column</span></span>     | <span data-ttu-id="00ceb-144">Nullable</span><span class="sxs-lookup"><span data-stu-id="00ceb-144">Nullable</span></span> | <span data-ttu-id="00ceb-145">MinValue</span><span class="sxs-lookup"><span data-stu-id="00ceb-145">MinValue</span></span> | <span data-ttu-id="00ceb-146">MaxValue</span><span class="sxs-lookup"><span data-stu-id="00ceb-146">MaxValue</span></span>   | <span data-ttu-id="00ceb-147">KeyTable</span><span class="sxs-lookup"><span data-stu-id="00ceb-147">KeyTable</span></span> | <span data-ttu-id="00ceb-148">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="00ceb-148">KeyColumn</span></span> | <span data-ttu-id="00ceb-149">類別</span><span class="sxs-lookup"><span data-stu-id="00ceb-149">Category</span></span>                     | <span data-ttu-id="00ceb-150">設定</span><span class="sxs-lookup"><span data-stu-id="00ceb-150">Set</span></span> | <span data-ttu-id="00ceb-151">Description</span><span class="sxs-lookup"><span data-stu-id="00ceb-151">Description</span></span> |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| <span data-ttu-id="00ceb-152">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="00ceb-152">CustomUserAccounts</span></span> | <span data-ttu-id="00ceb-153">UserName</span><span class="sxs-lookup"><span data-stu-id="00ceb-153">UserName</span></span>   | <span data-ttu-id="00ceb-154">N</span><span class="sxs-lookup"><span data-stu-id="00ceb-154">N</span></span>        |          |            |          |           | [<span data-ttu-id="00ceb-155">Text</span><span class="sxs-lookup"><span data-stu-id="00ceb-155">Text</span></span>](text.md)             |     |             |
| <span data-ttu-id="00ceb-156">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="00ceb-156">CustomUserAccounts</span></span> | <span data-ttu-id="00ceb-157">密碼</span><span class="sxs-lookup"><span data-stu-id="00ceb-157">Password</span></span>   | <span data-ttu-id="00ceb-158">N</span><span class="sxs-lookup"><span data-stu-id="00ceb-158">N</span></span>        |          |            |          |           | [<span data-ttu-id="00ceb-159">識別碼</span><span class="sxs-lookup"><span data-stu-id="00ceb-159">Identifier</span></span>](identifier.md) |     |             |
| <span data-ttu-id="00ceb-160">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="00ceb-160">CustomUserAccounts</span></span> | <span data-ttu-id="00ceb-161">屬性</span><span class="sxs-lookup"><span data-stu-id="00ceb-161">Attributes</span></span> | <span data-ttu-id="00ceb-162">Y</span><span class="sxs-lookup"><span data-stu-id="00ceb-162">Y</span></span>        | <span data-ttu-id="00ceb-163">0</span><span class="sxs-lookup"><span data-stu-id="00ceb-163">0</span></span>        | <span data-ttu-id="00ceb-164">2147483647</span><span class="sxs-lookup"><span data-stu-id="00ceb-164">2147483647</span></span> |          |           | <span data-ttu-id="00ceb-165">null</span><span class="sxs-lookup"><span data-stu-id="00ceb-165">null</span></span>                         |     |             |



 

<span data-ttu-id="00ceb-166">繼續 [撰寫 ActionText 和錯誤資料表](authoring-the-actiontext-and-error-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="00ceb-166">Continue to [Authoring the ActionText and Error Tables](authoring-the-actiontext-and-error-tables.md).</span></span>

 

 



