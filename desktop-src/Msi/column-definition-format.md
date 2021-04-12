---
description: View 物件的 MsiViewGetColumnInfo 和 ColumnInfo 屬性會使用下列格式來描述資料庫資料行定義。
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: 資料行定義格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193125"
---
# <a name="column-definition-format"></a><span data-ttu-id="aecfb-103">資料行定義格式</span><span class="sxs-lookup"><span data-stu-id="aecfb-103">Column Definition Format</span></span>

<span data-ttu-id="aecfb-104">[**View**](view-object.md)物件的 [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)和 [**ColumnInfo 屬性**](view-columninfo.md)會使用下列格式來描述資料庫資料行定義。</span><span class="sxs-lookup"><span data-stu-id="aecfb-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) and the [**ColumnInfo Property**](view-columninfo.md) of the [**View**](view-object.md) object use the following format to describe database column definitions.</span></span> <span data-ttu-id="aecfb-105">每個資料行都是由函數或屬性所傳回之對應記錄欄位中的字串所描述。</span><span class="sxs-lookup"><span data-stu-id="aecfb-105">Each column is described by a string in the corresponding record field returned by the function or property.</span></span> <span data-ttu-id="aecfb-106">定義字串是由代表資料類型的單一字母所組成，後面接著資料行的寬度 (字元（如果適用的話），否則) 。</span><span class="sxs-lookup"><span data-stu-id="aecfb-106">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise).</span></span> <span data-ttu-id="aecfb-107">寬度為零會指定未系結的寬度 (例如，長文字欄位和資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="aecfb-107">A width of zero designates an unbounded width (for example, long text fields and streams).</span></span> <span data-ttu-id="aecfb-108">大寫字母表示資料行中允許 null 值。</span><span class="sxs-lookup"><span data-stu-id="aecfb-108">An uppercase letter indicates that null values are allowed in the column.</span></span>



| <span data-ttu-id="aecfb-109">資料行描述項</span><span class="sxs-lookup"><span data-stu-id="aecfb-109">Column descriptor</span></span> | <span data-ttu-id="aecfb-110">定義字串</span><span class="sxs-lookup"><span data-stu-id="aecfb-110">Definition string</span></span>                 |
|-------------------|-----------------------------------|
| <span data-ttu-id="aecfb-111">！?</span><span class="sxs-lookup"><span data-stu-id="aecfb-111">s?</span></span>                | <span data-ttu-id="aecfb-112">字串，變數長度 (？ = 1-255) </span><span class="sxs-lookup"><span data-stu-id="aecfb-112">String, variable length (?=1-255)</span></span> |
| <span data-ttu-id="aecfb-113">s0</span><span class="sxs-lookup"><span data-stu-id="aecfb-113">s0</span></span>                | <span data-ttu-id="aecfb-114">字串、可變長度</span><span class="sxs-lookup"><span data-stu-id="aecfb-114">String, variable length</span></span>           |
| <span data-ttu-id="aecfb-115">i2</span><span class="sxs-lookup"><span data-stu-id="aecfb-115">i2</span></span>                | <span data-ttu-id="aecfb-116">Short 整數</span><span class="sxs-lookup"><span data-stu-id="aecfb-116">Short integer</span></span>                     |
| <span data-ttu-id="aecfb-117">i4</span><span class="sxs-lookup"><span data-stu-id="aecfb-117">i4</span></span>                | <span data-ttu-id="aecfb-118">長整數</span><span class="sxs-lookup"><span data-stu-id="aecfb-118">Long integer</span></span>                      |
| <span data-ttu-id="aecfb-119">v0</span><span class="sxs-lookup"><span data-stu-id="aecfb-119">v0</span></span>                | <span data-ttu-id="aecfb-120">二進位資料流程</span><span class="sxs-lookup"><span data-stu-id="aecfb-120">Binary Stream</span></span>                     |
| <span data-ttu-id="aecfb-121">G？</span><span class="sxs-lookup"><span data-stu-id="aecfb-121">g?</span></span>                | <span data-ttu-id="aecfb-122">暫存字串 (？ = 0-255) </span><span class="sxs-lookup"><span data-stu-id="aecfb-122">Temporary string (?=0-255)</span></span>        |
| <span data-ttu-id="aecfb-123">J？</span><span class="sxs-lookup"><span data-stu-id="aecfb-123">j?</span></span>                | <span data-ttu-id="aecfb-124">暫存整數 (？ = 0，1，2，4) </span><span class="sxs-lookup"><span data-stu-id="aecfb-124">Temporary integer (?=0,1,2,4)</span></span>     |
| <span data-ttu-id="aecfb-125">O0</span><span class="sxs-lookup"><span data-stu-id="aecfb-125">O0</span></span>                | <span data-ttu-id="aecfb-126">暫存物件</span><span class="sxs-lookup"><span data-stu-id="aecfb-126">Temporary object</span></span>                  |



 

<span data-ttu-id="aecfb-127">用來描述資料行的字串與 CREATE 和 ALTER 所使用的 SQL 查詢字串具有下列關聯性。</span><span class="sxs-lookup"><span data-stu-id="aecfb-127">The strings used to describe columns have the following relationship to the SQL query strings used by CREATE and ALTER.</span></span> <span data-ttu-id="aecfb-128">如需詳細資訊，請參閱 [SQL 語法](sql-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="aecfb-128">For more information, see [SQL Syntax](sql-syntax.md).</span></span>



| <span data-ttu-id="aecfb-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="aecfb-129">Returned value</span></span> | <span data-ttu-id="aecfb-130">SQL 語法</span><span class="sxs-lookup"><span data-stu-id="aecfb-130">SQL syntax</span></span>                |
|----------------|---------------------------|
| <span data-ttu-id="aecfb-131">s0</span><span class="sxs-lookup"><span data-stu-id="aecfb-131">s0</span></span>             | <span data-ttu-id="aecfb-132">LONGCHAR</span><span class="sxs-lookup"><span data-stu-id="aecfb-132">LONGCHAR</span></span>                  |
| <span data-ttu-id="aecfb-133">l0</span><span class="sxs-lookup"><span data-stu-id="aecfb-133">l0</span></span>             | <span data-ttu-id="aecfb-134">LONGCHAR 可當地語系化</span><span class="sxs-lookup"><span data-stu-id="aecfb-134">LONGCHAR LOCALIZABLE</span></span>      |
| <span data-ttu-id="aecfb-135">！ \#</span><span class="sxs-lookup"><span data-stu-id="aecfb-135">s \#</span></span>           | <span data-ttu-id="aecfb-136">CHAR (\#) </span><span class="sxs-lookup"><span data-stu-id="aecfb-136">CHAR(\#)</span></span>                  |
| <span data-ttu-id="aecfb-137">！ \#</span><span class="sxs-lookup"><span data-stu-id="aecfb-137">s \#</span></span>           | <span data-ttu-id="aecfb-138">字元 (\#) </span><span class="sxs-lookup"><span data-stu-id="aecfb-138">CHARACTER(\#)</span></span>             |
| <span data-ttu-id="aecfb-139">我 \#</span><span class="sxs-lookup"><span data-stu-id="aecfb-139">l \#</span></span>           | <span data-ttu-id="aecfb-140">可當地語系化的 CHAR (\#) </span><span class="sxs-lookup"><span data-stu-id="aecfb-140">CHAR(\#) LOCALIZABLE</span></span>      |
| <span data-ttu-id="aecfb-141">我 \#</span><span class="sxs-lookup"><span data-stu-id="aecfb-141">l \#</span></span>           | <span data-ttu-id="aecfb-142"> () 可當地語系化的字元 \#</span><span class="sxs-lookup"><span data-stu-id="aecfb-142">CHARACTER(\#) LOCALIZABLE</span></span> |
| <span data-ttu-id="aecfb-143">i2</span><span class="sxs-lookup"><span data-stu-id="aecfb-143">i2</span></span>             | <span data-ttu-id="aecfb-144">SHORT</span><span class="sxs-lookup"><span data-stu-id="aecfb-144">SHORT</span></span>                     |
| <span data-ttu-id="aecfb-145">i2</span><span class="sxs-lookup"><span data-stu-id="aecfb-145">i2</span></span>             | <span data-ttu-id="aecfb-146">INT</span><span class="sxs-lookup"><span data-stu-id="aecfb-146">INT</span></span>                       |
| <span data-ttu-id="aecfb-147">i2</span><span class="sxs-lookup"><span data-stu-id="aecfb-147">i2</span></span>             | <span data-ttu-id="aecfb-148">INTEGER</span><span class="sxs-lookup"><span data-stu-id="aecfb-148">INTEGER</span></span>                   |
| <span data-ttu-id="aecfb-149">i4</span><span class="sxs-lookup"><span data-stu-id="aecfb-149">i4</span></span>             | <span data-ttu-id="aecfb-150">LONG</span><span class="sxs-lookup"><span data-stu-id="aecfb-150">LONG</span></span>                      |
| <span data-ttu-id="aecfb-151">v0</span><span class="sxs-lookup"><span data-stu-id="aecfb-151">v0</span></span>             | <span data-ttu-id="aecfb-152">OBJECT</span><span class="sxs-lookup"><span data-stu-id="aecfb-152">OBJECT</span></span>                    |



 

<span data-ttu-id="aecfb-153">如果字母不是大寫，則應該附加非 Null 的 SQL 語句。</span><span class="sxs-lookup"><span data-stu-id="aecfb-153">If the letter is not capitalized, the SQL statement should be appended with NOT NULL.</span></span>



| <span data-ttu-id="aecfb-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="aecfb-154">Returned value</span></span> | <span data-ttu-id="aecfb-155">SQL 語法</span><span class="sxs-lookup"><span data-stu-id="aecfb-155">SQL syntax</span></span>        |
|----------------|-------------------|
| <span data-ttu-id="aecfb-156">s0</span><span class="sxs-lookup"><span data-stu-id="aecfb-156">s0</span></span>             | <span data-ttu-id="aecfb-157">LONGCHAR 不可為 Null</span><span class="sxs-lookup"><span data-stu-id="aecfb-157">LONGCHAR NOT NULL</span></span> |



 

<span data-ttu-id="aecfb-158">安裝程式不會在內部將資料行的長度限制為數據行定義格式所指定的值。</span><span class="sxs-lookup"><span data-stu-id="aecfb-158">The installer does not internally limit the length of columns to the value specified by the column definition format.</span></span> <span data-ttu-id="aecfb-159">如果在欄位中輸入的資料超過指定的資料行長度，封裝就無法通過 [封裝驗證](package-validation.md)。</span><span class="sxs-lookup"><span data-stu-id="aecfb-159">If the data entered into a field exceeds the specified column length, the package fails to pass [package validation](package-validation.md).</span></span> <span data-ttu-id="aecfb-160">若要在這種情況下通過驗證，則必須變更資料或資料庫架構。</span><span class="sxs-lookup"><span data-stu-id="aecfb-160">To pass validation in this case, either the data or the database schema must be changed.</span></span> <span data-ttu-id="aecfb-161">變更標準資料表之資料行長度的唯一方法是使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出資料表、編輯匯出的 idt 檔案，然後使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)匯入資料表。</span><span class="sxs-lookup"><span data-stu-id="aecfb-161">The only means to change the column length of a standard table is by exporting the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editing the exported .idt file, and then importing the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="aecfb-162">作者無法變更標準資料表中任何資料行的資料行資料類型、null 屬性或當地語系化屬性。</span><span class="sxs-lookup"><span data-stu-id="aecfb-162">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="aecfb-163">作者可以使用具有任何資料行屬性的資料行來建立自訂資料表。</span><span class="sxs-lookup"><span data-stu-id="aecfb-163">Authors can create custom tables with columns having any column attributes.</span></span>

<span data-ttu-id="aecfb-164">使用 [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) 將參考資料庫合併到目標資料庫時，資料行名稱、主鍵數目和資料行資料類型必須相符。</span><span class="sxs-lookup"><span data-stu-id="aecfb-164">When using [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to merge a reference database into a target database, the column names, number of primary keys, and column data types must match.</span></span> <span data-ttu-id="aecfb-165">**MsiDatabaseMerge** 會忽略當地語系化和資料行長度屬性。</span><span class="sxs-lookup"><span data-stu-id="aecfb-165">**MsiDatabaseMerge** ignores the localization and column length attributes.</span></span> <span data-ttu-id="aecfb-166">如果參考資料庫中的資料行長度為0或大於該資料行在目標資料庫中的長度， **MsiDatabaseMerge** 會將目標資料庫中的資料行長度增加到參考資料庫中的長度。</span><span class="sxs-lookup"><span data-stu-id="aecfb-166">If a column in the reference database has a length that is 0 or greater than the that column's length in the target database, **MsiDatabaseMerge** increases the column length in the target database to the length in the reference database.</span></span>

<span data-ttu-id="aecfb-167">使用 Mergmod.dll 版本2.0 時，將合併模組的應用程式寫入 .msi 檔案時，絕對不會變更資料行的長度或現有資料庫資料表的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="aecfb-167">When using Mergmod.dll version 2.0, the application of a merge module to a .msi file never changes the length of columns or the column types of an existing database table.</span></span> <span data-ttu-id="aecfb-168">但是，如果模組將新的資料行加入至資料表，以便加入資料行，則合併模組的應用程式可以變更現有資料庫資料表的架構。</span><span class="sxs-lookup"><span data-stu-id="aecfb-168">The application of a merge module can however change the schema of an existing database table if the module adds new columns to a table for which it is valid to add columns.</span></span> <span data-ttu-id="aecfb-169">使用小於2.0 版的 Mergemod.dll 版本時，合併模組的應用程式永遠不會變更資料行的長度，而且永遠不會變更目標資料庫的架構。</span><span class="sxs-lookup"><span data-stu-id="aecfb-169">When using a Mergemod.dll version less than version 2.0, the application of a merge module never changes the length of columns and never changes the schema of the target database.</span></span>

 

 



