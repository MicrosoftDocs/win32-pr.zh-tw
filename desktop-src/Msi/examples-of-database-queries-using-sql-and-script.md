---
description: 使用腳本驅動的資料庫查詢的範例，可在 Windows Installer 軟體發展工具組 (SDK) 中提供作為公用程式 WiRunSQL.vbs。
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: 使用 SQL 和腳本的資料庫查詢範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692491"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a><span data-ttu-id="e609f-103">使用 SQL 和腳本的資料庫查詢範例</span><span class="sxs-lookup"><span data-stu-id="e609f-103">Examples of Database Queries Using SQL and Script</span></span>

<span data-ttu-id="e609f-104">Windows [Installer 軟體發展工具組](platform-sdk-components-for-windows-installer-developers.md) 中提供使用腳本驅動資料庫查詢的範例， (SDK) 作為公用程式 WiRunSQL.vbs。</span><span class="sxs-lookup"><span data-stu-id="e609f-104">An example of using script-driven database queries is provided in the Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="e609f-105">此公用程式會使用 [Sql 語法](sql-syntax.md)一節中所述的 sql Windows Installer 版本來處理資料庫查詢。</span><span class="sxs-lookup"><span data-stu-id="e609f-105">This utility handles database queries using the Windows Installer version of SQL described in the section [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="e609f-106">**從資料表中刪除記錄**</span><span class="sxs-lookup"><span data-stu-id="e609f-106">**Delete a record from a table**</span></span>

<span data-ttu-id="e609f-107">下列命令列將從 Test.msi 資料庫的 [功能](feature-table.md) 資料表中，刪除具有主鍵 RED 的記錄。</span><span class="sxs-lookup"><span data-stu-id="e609f-107">The following command line deletes the record having the primary key RED from the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="e609f-108">**Cscript WiRunSQL.vbs Test.msi」功能的 [刪除] \` \` \` \` 。 \`Feature \` = ' RED ' "**</span><span class="sxs-lookup"><span data-stu-id="e609f-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \`Feature\` WHERE \`Feature\`.\`Feature\`='RED'"**</span></span>

<span data-ttu-id="e609f-109">**將資料表加入至資料庫**</span><span class="sxs-lookup"><span data-stu-id="e609f-109">**Add a table to a database**</span></span>

<span data-ttu-id="e609f-110">下列命令列將 [目錄](directory-table.md) 資料表新增至 Test.msi 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e609f-110">The following command line adds the [Directory](directory-table.md) table to the Test.msi database.</span></span>

<span data-ttu-id="e609f-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` directory \` (\` directory \` CHAR (72) NOT Null、 \` Directory \_ Parent \` char (72) 、 \` DEFAULTDIR \` CHAR (255) NOT Null 可當地語系化的 PRIMARY KEY \` Directory \`) "**</span><span class="sxs-lookup"><span data-stu-id="e609f-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \`Directory\` (\`Directory\` CHAR(72) NOT NULL, \`Directory\_Parent\` CHAR(72), \`DefaultDir\` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \`Directory\`)"**</span></span>

<span data-ttu-id="e609f-112">**從資料庫中移除資料表**</span><span class="sxs-lookup"><span data-stu-id="e609f-112">**Remove a table from a database**</span></span>

<span data-ttu-id="e609f-113">下列命令列將從 Test.msi 資料庫移除 [功能](feature-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="e609f-113">The following command line removes the [Feature](feature-table.md) table from the Test.msi database.</span></span>

<span data-ttu-id="e609f-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \` Feature \` "**</span><span class="sxs-lookup"><span data-stu-id="e609f-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \`Feature\`"**</span></span>

<span data-ttu-id="e609f-115">**將新資料行加入至資料表**</span><span class="sxs-lookup"><span data-stu-id="e609f-115">**Add a new column to a table**</span></span>

<span data-ttu-id="e609f-116">下列命令列會將測試資料行加入 Test.msi 資料庫的 [CustomAction](customaction-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="e609f-116">The following command line adds the Test column to the [CustomAction](customaction-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="e609f-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` ADD \` Test \` INTEGER"**</span><span class="sxs-lookup"><span data-stu-id="e609f-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`CustomAction\` ADD \`Test\` INTEGER"**</span></span>

<span data-ttu-id="e609f-118">**在資料表中插入新的記錄**</span><span class="sxs-lookup"><span data-stu-id="e609f-118">**Insert a new record into a table**</span></span>

<span data-ttu-id="e609f-119">下列命令列將新記錄插入 Test.msi 資料庫的 [功能](feature-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="e609f-119">The following command line inserts a new record into the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="e609f-120">**Cscript WiRunSQL.vbs Test.msi 「插入 \` 功能 \` (\` 功能 \` 。 \`功能 \` \` \` 。 \`功能 \_ 父系 \` 、 \` 功能 \` 。 \`標題 \` 、 \` 功能 \` 。 \`描述 \` ， \` 功能 \` 。 \`顯示 \` 、 \` 功能 \` 。 \`層級 \` 、 \` 功能 \` 。 \`目錄 \_ \` 、 \` 功能 \` 。 \`屬性 \`) 值 ( 「網球」、「運動」、「網球」、「聯賽」、25、3、「SPORTDIR」、2) 」**</span><span class="sxs-lookup"><span data-stu-id="e609f-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \`Feature\` (\`Feature\`.\`Feature\`,\`Feature\`.\`Feature\_Parent\`,\`Feature\`.\`Title\`,\`Feature\`.\`Description\`, \`Feature\`.\`Display\`,\`Feature\`.\`Level\`,\`Feature\`.\`Directory\_\`,\`Feature\`.\`Attributes\`) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**</span></span>

<span data-ttu-id="e609f-121">這會將下列記錄插入 Test.msi 的 [功能](feature-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="e609f-121">This inserts the following record into the [Feature](feature-table.md) table of Test.msi.</span></span>

<span data-ttu-id="e609f-122">[功能](feature-table.md) 表</span><span class="sxs-lookup"><span data-stu-id="e609f-122">[Feature](feature-table.md) Table</span></span>



| <span data-ttu-id="e609f-123">功能</span><span class="sxs-lookup"><span data-stu-id="e609f-123">Feature</span></span> | <span data-ttu-id="e609f-124">功能 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="e609f-124">Feature\_Parent</span></span> | <span data-ttu-id="e609f-125">標題</span><span class="sxs-lookup"><span data-stu-id="e609f-125">Title</span></span>  | <span data-ttu-id="e609f-126">描述</span><span class="sxs-lookup"><span data-stu-id="e609f-126">Description</span></span> | <span data-ttu-id="e609f-127">顯示</span><span class="sxs-lookup"><span data-stu-id="e609f-127">Display</span></span> | <span data-ttu-id="e609f-128">層級</span><span class="sxs-lookup"><span data-stu-id="e609f-128">Level</span></span> | <span data-ttu-id="e609f-129">目錄\_</span><span class="sxs-lookup"><span data-stu-id="e609f-129">Directory\_</span></span> | <span data-ttu-id="e609f-130">屬性</span><span class="sxs-lookup"><span data-stu-id="e609f-130">Attributes</span></span> |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| <span data-ttu-id="e609f-131">網球</span><span class="sxs-lookup"><span data-stu-id="e609f-131">Tennis</span></span>  | <span data-ttu-id="e609f-132">運動項目</span><span class="sxs-lookup"><span data-stu-id="e609f-132">Sport</span></span>           | <span data-ttu-id="e609f-133">網球</span><span class="sxs-lookup"><span data-stu-id="e609f-133">Tennis</span></span> | <span data-ttu-id="e609f-134">比賽</span><span class="sxs-lookup"><span data-stu-id="e609f-134">Tournament</span></span>  | <span data-ttu-id="e609f-135">25</span><span class="sxs-lookup"><span data-stu-id="e609f-135">25</span></span>      | <span data-ttu-id="e609f-136">3</span><span class="sxs-lookup"><span data-stu-id="e609f-136">3</span></span>     | <span data-ttu-id="e609f-137">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="e609f-137">SPORTDIR</span></span>    | <span data-ttu-id="e609f-138">2</span><span class="sxs-lookup"><span data-stu-id="e609f-138">2</span></span>          |



 

<span data-ttu-id="e609f-139">請注意，二進位資料無法使用 INSERT INTO 或 UPDATE SQL 查詢直接插入資料表中。</span><span class="sxs-lookup"><span data-stu-id="e609f-139">Note that binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="e609f-140">如需詳細資訊，請參閱 [使用 SQL 將二進位資料加入至資料表](adding-binary-data-to-a-table-using-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="e609f-140">For information see [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).</span></span>

<span data-ttu-id="e609f-141">**修改資料表中的現有記錄**</span><span class="sxs-lookup"><span data-stu-id="e609f-141">**Modify an existing record in a table**</span></span>

<span data-ttu-id="e609f-142">下列命令列將 [標題] 欄位中的現有值變更為 [效能]。</span><span class="sxs-lookup"><span data-stu-id="e609f-142">The following command line changes the existing value in the Title field to "Performances."</span></span> <span data-ttu-id="e609f-143">更新的記錄會以 "藝術" 作為其主鍵，而且位於 Test.msi 資料庫的功能資料表中。</span><span class="sxs-lookup"><span data-stu-id="e609f-143">The updated record has "Arts" as its primary key and is in the Feature table of the Test.msi database.</span></span>

<span data-ttu-id="e609f-144">**Cscript WiRunSQL.vbs Test.msi 「更新 \` 功能 \` 集」 \` 功能 \` 。 \`Title \` = 功能的「效能 \` 」 \` 。 \`Feature \` = ' 藝術 ' "**</span><span class="sxs-lookup"><span data-stu-id="e609f-144">**Cscript WiRunSQL.vbs Test.msi "UPDATE \`Feature\` SET \`Feature\`.\`Title\`='Performances' WHERE \`Feature\`.\`Feature\`='Arts'"**</span></span>

<span data-ttu-id="e609f-145">**選取一組記錄**</span><span class="sxs-lookup"><span data-stu-id="e609f-145">**Select a group of records**</span></span>

<span data-ttu-id="e609f-146">下列命令列會選取屬於 Test.msi 資料庫中 ErrorDialog 之所有控制項的名稱和類型。</span><span class="sxs-lookup"><span data-stu-id="e609f-146">The following command line selects the name and type of all controls that belong to the ErrorDialog in the Test.msi database.</span></span>

<span data-ttu-id="e609f-147">**CScript WiRunSQL.vbs Test.msi 選取 \` 控制項 \` ，然後 \` \` \` \` 在 \` 對話方塊 \_ \` = ' ErrorDialog ' 的控制項中輸入**</span><span class="sxs-lookup"><span data-stu-id="e609f-147">**CScript WiRunSQL.vbs Test.msi "SELECT \`Control\`, \`Type\` FROM \`Control\` WHERE \`Dialog\_\`='ErrorDialog' "**</span></span>

<span data-ttu-id="e609f-148">**將資料表放入記憶體中**</span><span class="sxs-lookup"><span data-stu-id="e609f-148">**Hold a table in memory**</span></span>

<span data-ttu-id="e609f-149">下列命令列將鎖定記憶體中 Test.msi 資料庫的 [元件](component-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="e609f-149">The following command line locks the [Component](component-table.md) table of the Test.msi database in memory.</span></span>

<span data-ttu-id="e609f-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` HOLD"**</span><span class="sxs-lookup"><span data-stu-id="e609f-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` HOLD"**</span></span>

<span data-ttu-id="e609f-151">**釋放記憶體中的資料表**</span><span class="sxs-lookup"><span data-stu-id="e609f-151">**Free a table in memory**</span></span>

<span data-ttu-id="e609f-152">下列命令列將從記憶體釋放 Test.msi 資料庫的 [元件](component-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="e609f-152">The following command line frees the [Component](component-table.md) table of the Test.msi database from memory.</span></span>

<span data-ttu-id="e609f-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` FREE"**</span><span class="sxs-lookup"><span data-stu-id="e609f-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` FREE"**</span></span>

 

 



