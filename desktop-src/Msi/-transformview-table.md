---
description: 這是唯讀的臨時表，用來以轉換視圖模式來查看轉換。 安裝程式永遠不會保存此資料表。
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513249"
---
# <a name="_transformview-table"></a><span data-ttu-id="400e1-104">\_TransformView 資料表</span><span class="sxs-lookup"><span data-stu-id="400e1-104">\_TransformView Table</span></span>

<span data-ttu-id="400e1-105">這是唯讀的臨時表，用來以轉換視圖模式來查看轉換。</span><span class="sxs-lookup"><span data-stu-id="400e1-105">This is a read-only temporary table used to view transforms with the transform view mode.</span></span> <span data-ttu-id="400e1-106">安裝程式永遠不會保存此資料表。</span><span class="sxs-lookup"><span data-stu-id="400e1-106">This table is never persisted by the installer.</span></span>

<span data-ttu-id="400e1-107">若要叫用轉換視圖模式，請取得控制碼，並開啟參考資料庫。</span><span class="sxs-lookup"><span data-stu-id="400e1-107">To invoke the transform view mode, obtain a handle and open the reference database.</span></span> <span data-ttu-id="400e1-108">請參閱 [取得資料庫控制碼](obtaining-a-database-handle.md)。</span><span class="sxs-lookup"><span data-stu-id="400e1-108">See [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span> <span data-ttu-id="400e1-109">使用 MSITRANSFORM 錯誤 VIEWTRANSFORM 來呼叫 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="400e1-109">Call [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) with MSITRANSFORM\_ERROR\_VIEWTRANSFORM.</span></span> <span data-ttu-id="400e1-110">這會停止將轉換套用至資料庫，並將轉換內容傾印至 \_ TransformView 資料表。</span><span class="sxs-lookup"><span data-stu-id="400e1-110">This stops the transform from being applied to the database and dumps the transform contents into the \_TransformView table.</span></span> <span data-ttu-id="400e1-111">您可以使用 SQL 查詢來存取資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="400e1-111">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="400e1-112">請參閱 [使用查詢](working-with-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="400e1-112">See [Working with Queries](working-with-queries.md).</span></span>

<span data-ttu-id="400e1-113">套用 \_ 其他轉換時，不會清除 TransformView 資料表。</span><span class="sxs-lookup"><span data-stu-id="400e1-113">The \_TransformView table is not cleared when another transform is applied.</span></span> <span data-ttu-id="400e1-114">資料表會反映後續應用程式的累積效果。</span><span class="sxs-lookup"><span data-stu-id="400e1-114">The table reflects the cumulative effect of successive applications.</span></span> <span data-ttu-id="400e1-115">若要個別查看轉換，您必須釋放資料表。</span><span class="sxs-lookup"><span data-stu-id="400e1-115">To view the transforms separately you must release the table.</span></span>

<span data-ttu-id="400e1-116">\_TransformView 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="400e1-116">The \_TransformView Table has the following columns.</span></span>



| <span data-ttu-id="400e1-117">Column</span><span class="sxs-lookup"><span data-stu-id="400e1-117">Column</span></span>  | <span data-ttu-id="400e1-118">類型</span><span class="sxs-lookup"><span data-stu-id="400e1-118">Type</span></span>                         | <span data-ttu-id="400e1-119">答案</span><span class="sxs-lookup"><span data-stu-id="400e1-119">Key</span></span> | <span data-ttu-id="400e1-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="400e1-120">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="400e1-121">資料表</span><span class="sxs-lookup"><span data-stu-id="400e1-121">Table</span></span>   | [<span data-ttu-id="400e1-122">識別碼</span><span class="sxs-lookup"><span data-stu-id="400e1-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="400e1-123">Y</span><span class="sxs-lookup"><span data-stu-id="400e1-123">Y</span></span>   | <span data-ttu-id="400e1-124">N</span><span class="sxs-lookup"><span data-stu-id="400e1-124">N</span></span>        |
| <span data-ttu-id="400e1-125">Column</span><span class="sxs-lookup"><span data-stu-id="400e1-125">Column</span></span>  | [<span data-ttu-id="400e1-126">Text</span><span class="sxs-lookup"><span data-stu-id="400e1-126">Text</span></span>](text.md)             | <span data-ttu-id="400e1-127">Y</span><span class="sxs-lookup"><span data-stu-id="400e1-127">Y</span></span>   | <span data-ttu-id="400e1-128">N</span><span class="sxs-lookup"><span data-stu-id="400e1-128">N</span></span>        |
| <span data-ttu-id="400e1-129">資料列</span><span class="sxs-lookup"><span data-stu-id="400e1-129">Row</span></span>     | [<span data-ttu-id="400e1-130">Text</span><span class="sxs-lookup"><span data-stu-id="400e1-130">Text</span></span>](text.md)             | <span data-ttu-id="400e1-131">Y</span><span class="sxs-lookup"><span data-stu-id="400e1-131">Y</span></span>   | <span data-ttu-id="400e1-132">Y</span><span class="sxs-lookup"><span data-stu-id="400e1-132">Y</span></span>        |
| <span data-ttu-id="400e1-133">資料</span><span class="sxs-lookup"><span data-stu-id="400e1-133">Data</span></span>    | [<span data-ttu-id="400e1-134">Text</span><span class="sxs-lookup"><span data-stu-id="400e1-134">Text</span></span>](text.md)             | <span data-ttu-id="400e1-135">N</span><span class="sxs-lookup"><span data-stu-id="400e1-135">N</span></span>   | <span data-ttu-id="400e1-136">Y</span><span class="sxs-lookup"><span data-stu-id="400e1-136">Y</span></span>        |
| <span data-ttu-id="400e1-137">目前</span><span class="sxs-lookup"><span data-stu-id="400e1-137">Current</span></span> | [<span data-ttu-id="400e1-138">Text</span><span class="sxs-lookup"><span data-stu-id="400e1-138">Text</span></span>](text.md)             | <span data-ttu-id="400e1-139">N</span><span class="sxs-lookup"><span data-stu-id="400e1-139">N</span></span>   | <span data-ttu-id="400e1-140">Y</span><span class="sxs-lookup"><span data-stu-id="400e1-140">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="400e1-141">Column</span><span class="sxs-lookup"><span data-stu-id="400e1-141">Column</span></span>

<dl> <dt>

<span data-ttu-id="400e1-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="400e1-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="400e1-143">改變的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="400e1-143">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="400e1-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>列</span><span class="sxs-lookup"><span data-stu-id="400e1-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="400e1-145">改變的資料表資料行名稱，或插入、刪除、建立或卸載。</span><span class="sxs-lookup"><span data-stu-id="400e1-145">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="400e1-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>行</span><span class="sxs-lookup"><span data-stu-id="400e1-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="400e1-147">以定位字元分隔的主鍵值清單。</span><span class="sxs-lookup"><span data-stu-id="400e1-147">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="400e1-148">Null 主鍵值是以單一空白字元表示。</span><span class="sxs-lookup"><span data-stu-id="400e1-148">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="400e1-149">此資料行中的 Null 值表示架構變更。</span><span class="sxs-lookup"><span data-stu-id="400e1-149">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="400e1-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>資料</span><span class="sxs-lookup"><span data-stu-id="400e1-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="400e1-151">資料、資料流程的名稱或資料行定義。</span><span class="sxs-lookup"><span data-stu-id="400e1-151">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="400e1-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>當前</span><span class="sxs-lookup"><span data-stu-id="400e1-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="400e1-153">參考資料庫的目前值，或資料行 a 數位。</span><span class="sxs-lookup"><span data-stu-id="400e1-153">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="400e1-154">備註</span><span class="sxs-lookup"><span data-stu-id="400e1-154">Remarks</span></span>

<span data-ttu-id="400e1-155">\_TransformView 會透過鎖定計數保留在記憶體中，可使用下列 SQL 命令來釋放。</span><span class="sxs-lookup"><span data-stu-id="400e1-155">The \_TransformView is held in memory by a lock count, that can be released with the following SQL command.</span></span>

<span data-ttu-id="400e1-156">「ALTER TABLE \_ TRANSFORMVIEW FREE」。</span><span class="sxs-lookup"><span data-stu-id="400e1-156">"ALTER TABLE \_TransformView FREE".</span></span>

<span data-ttu-id="400e1-157">您可以使用 SQL 查詢來存取資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="400e1-157">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="400e1-158">SQL 語言有兩個主要部分：「資料定義語言」 (DDL) 用來定義 SQL 資料庫中的所有物件，以及用來選取、插入、更新和刪除使用 DDL 定義之物件中資料的資料操作語言 (DML) 。</span><span class="sxs-lookup"><span data-stu-id="400e1-158">The SQL language has two main divisions: Data Definition Language (DDL) that is used to define all the objects in an SQL database, and Data Manipulation Language (DML) that is used to select, insert, update, and delete data in the objects defined using DDL.</span></span>

<span data-ttu-id="400e1-159">資料操作語言 (DML) 轉換作業，如下所示。</span><span class="sxs-lookup"><span data-stu-id="400e1-159">The Data Manipulation Language (DML) transform operations are indicated as follows.</span></span> <span data-ttu-id="400e1-160">資料操作語言 (DML) 是 SQL 中可操作的語句，而不是定義資料。</span><span class="sxs-lookup"><span data-stu-id="400e1-160">Data Manipulation Language (DML) are those statements in SQL that manipulate, as opposed to define, data.</span></span>



| <span data-ttu-id="400e1-161">轉換作業</span><span class="sxs-lookup"><span data-stu-id="400e1-161">Transform operation</span></span> | <span data-ttu-id="400e1-162">SQL 結果</span><span class="sxs-lookup"><span data-stu-id="400e1-162">SQL result</span></span>                                    |
|---------------------|-----------------------------------------------|
| <span data-ttu-id="400e1-163">修改資料</span><span class="sxs-lookup"><span data-stu-id="400e1-163">Modify data</span></span>         | <span data-ttu-id="400e1-164">表列排data{目前的值}</span><span class="sxs-lookup"><span data-stu-id="400e1-164">{table} {column} {row} {data} {current value}</span></span> |
| <span data-ttu-id="400e1-165">插入資料列</span><span class="sxs-lookup"><span data-stu-id="400e1-165">Insert row</span></span>          | <span data-ttu-id="400e1-166">表"INSERT" {row} Null null</span><span class="sxs-lookup"><span data-stu-id="400e1-166">{table} "INSERT" {row} NULL NULL</span></span>              |
| <span data-ttu-id="400e1-167">刪除資料列</span><span class="sxs-lookup"><span data-stu-id="400e1-167">Delete row</span></span>          | <span data-ttu-id="400e1-168">表"DELETE" {row} Null Null</span><span class="sxs-lookup"><span data-stu-id="400e1-168">{table} "DELETE" {row} NULL NULL</span></span>              |



 

<span data-ttu-id="400e1-169">資料定義語言 (DDL) 轉換作業如下所示。</span><span class="sxs-lookup"><span data-stu-id="400e1-169">The Data Definition Language (DDL) transform operations are indicated as follows.</span></span> <span data-ttu-id="400e1-170">資料定義語言 (DDL) 是 SQL 中定義，而不是運算元據的語句。</span><span class="sxs-lookup"><span data-stu-id="400e1-170">Data Definition Language (DDL) are those statements in SQL that define, as opposed to manipulate, data.</span></span>



| <span data-ttu-id="400e1-171">轉換作業</span><span class="sxs-lookup"><span data-stu-id="400e1-171">Transform operation</span></span> | <span data-ttu-id="400e1-172">SQL 結果</span><span class="sxs-lookup"><span data-stu-id="400e1-172">SQL result</span></span>                                   |
|---------------------|----------------------------------------------|
| <span data-ttu-id="400e1-173">新增資料行</span><span class="sxs-lookup"><span data-stu-id="400e1-173">Add column</span></span>          | <span data-ttu-id="400e1-174">表列Null {定義} {資料行編號}</span><span class="sxs-lookup"><span data-stu-id="400e1-174">{table} {column} NULL {defn} {column number}</span></span> |
| <span data-ttu-id="400e1-175">加入資料表</span><span class="sxs-lookup"><span data-stu-id="400e1-175">Add table</span></span>           | <span data-ttu-id="400e1-176">表"CREATE" Null Null Null</span><span class="sxs-lookup"><span data-stu-id="400e1-176">{table} "CREATE" NULL NULL NULL</span></span>              |
| <span data-ttu-id="400e1-177">卸除資料表</span><span class="sxs-lookup"><span data-stu-id="400e1-177">Drop table</span></span>          | <span data-ttu-id="400e1-178">表"DROP" Null Null Null</span><span class="sxs-lookup"><span data-stu-id="400e1-178">{table} "DROP" NULL NULL NULL</span></span>                |



 

<span data-ttu-id="400e1-179">當轉換的應用程式加入此資料表時，資料欄位會接收可解釋為16位整數值的文字。</span><span class="sxs-lookup"><span data-stu-id="400e1-179">When the application of a transform adds this table, the Data field receives text that can be interpreted as a 16-bit integer value.</span></span> <span data-ttu-id="400e1-180">此值描述資料列欄位中所命名的資料行。</span><span class="sxs-lookup"><span data-stu-id="400e1-180">The value describes the column named in the Column field.</span></span> <span data-ttu-id="400e1-181">您可以比較整數值與下表中的常數，以判斷改變的資料行的定義。</span><span class="sxs-lookup"><span data-stu-id="400e1-181">You can compare the integer value to the constants in the following table to determine the definition of the altered column.</span></span>



| <span data-ttu-id="400e1-182">bit</span><span class="sxs-lookup"><span data-stu-id="400e1-182">Bit</span></span>                                                                                                       | <span data-ttu-id="400e1-183">Description</span><span class="sxs-lookup"><span data-stu-id="400e1-183">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="400e1-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span><span class="sxs-lookup"><span data-stu-id="400e1-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span></span><br/>         | <span data-ttu-id="400e1-185">十六進位： 0x0000 0x0100</span><span class="sxs-lookup"><span data-stu-id="400e1-185">Hexadecimal: 0x0000 0x0100</span></span><br/> <span data-ttu-id="400e1-186">Decimal： 0 255</span><span class="sxs-lookup"><span data-stu-id="400e1-186">Decimal: 0 255</span></span><br/> <span data-ttu-id="400e1-187">資料行寬度</span><span class="sxs-lookup"><span data-stu-id="400e1-187">Column width</span></span><br/>                                                                                                                                                                                                                                  |
| <span data-ttu-id="400e1-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>位8</span><span class="sxs-lookup"><span data-stu-id="400e1-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span></span><br/>                  | <span data-ttu-id="400e1-189">十六進位：0x0100</span><span class="sxs-lookup"><span data-stu-id="400e1-189">Hexadecimal: 0x0100</span></span><br/> <span data-ttu-id="400e1-190">Decimal：256</span><span class="sxs-lookup"><span data-stu-id="400e1-190">Decimal: 256</span></span><br/> <span data-ttu-id="400e1-191">持續性資料行。</span><span class="sxs-lookup"><span data-stu-id="400e1-191">A persistent column.</span></span> <span data-ttu-id="400e1-192">零表示暫時的資料行。</span><span class="sxs-lookup"><span data-stu-id="400e1-192">Zero means a temporary column.</span></span> <br/>                                                                                                                                                                                                   |
| <span data-ttu-id="400e1-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>位9</span><span class="sxs-lookup"><span data-stu-id="400e1-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span></span><br/>                  | <span data-ttu-id="400e1-194">十六進位：0x0200</span><span class="sxs-lookup"><span data-stu-id="400e1-194">Hexadecimal: 0x0200</span></span><br/> <span data-ttu-id="400e1-195">Decimal：1023</span><span class="sxs-lookup"><span data-stu-id="400e1-195">Decimal: 1023</span></span><br/> <span data-ttu-id="400e1-196">可當地語系化的資料行。</span><span class="sxs-lookup"><span data-stu-id="400e1-196">A localizable column.</span></span> <span data-ttu-id="400e1-197">零表示資料行不可當地語系化。</span><span class="sxs-lookup"><span data-stu-id="400e1-197">Zero means the column cannot be localized.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="400e1-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span><span class="sxs-lookup"><span data-stu-id="400e1-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span></span><br/> | <span data-ttu-id="400e1-199">十六進位：0x0000</span><span class="sxs-lookup"><span data-stu-id="400e1-199">Hexadecimal: 0x0000</span></span><br/> <span data-ttu-id="400e1-200">Decimal：0</span><span class="sxs-lookup"><span data-stu-id="400e1-200">Decimal: 0</span></span><br/> <span data-ttu-id="400e1-201">長整數</span><span class="sxs-lookup"><span data-stu-id="400e1-201">Long integer</span></span><br/> <span data-ttu-id="400e1-202">十六進位：0x0400</span><span class="sxs-lookup"><span data-stu-id="400e1-202">Hexadecimal: 0x0400</span></span><br/> <span data-ttu-id="400e1-203">Decimal：1024</span><span class="sxs-lookup"><span data-stu-id="400e1-203">Decimal: 1024</span></span><br/> <span data-ttu-id="400e1-204">Short 整數</span><span class="sxs-lookup"><span data-stu-id="400e1-204">Short integer</span></span><br/> <span data-ttu-id="400e1-205">十六進位：0x0800</span><span class="sxs-lookup"><span data-stu-id="400e1-205">Hexadecimal: 0x0800</span></span><br/> <span data-ttu-id="400e1-206">Decimal：2048</span><span class="sxs-lookup"><span data-stu-id="400e1-206">Decimal: 2048</span></span><br/> <span data-ttu-id="400e1-207">Binary 物件</span><span class="sxs-lookup"><span data-stu-id="400e1-207">Binary object</span></span><br/> <span data-ttu-id="400e1-208">十六進位：0x0C00</span><span class="sxs-lookup"><span data-stu-id="400e1-208">Hexadecimal: 0x0C00</span></span><br/> <span data-ttu-id="400e1-209">Decimal：3072</span><span class="sxs-lookup"><span data-stu-id="400e1-209">Decimal: 3072</span></span><br/> <span data-ttu-id="400e1-210">String</span><span class="sxs-lookup"><span data-stu-id="400e1-210">String</span></span><br/> |
| <span data-ttu-id="400e1-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span><span class="sxs-lookup"><span data-stu-id="400e1-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span></span><br/>              | <span data-ttu-id="400e1-212">十六進位：0x1000</span><span class="sxs-lookup"><span data-stu-id="400e1-212">Hexadecimal: 0x1000</span></span><br/> <span data-ttu-id="400e1-213">Decimal：4096</span><span class="sxs-lookup"><span data-stu-id="400e1-213">Decimal: 4096</span></span><br/> <span data-ttu-id="400e1-214">可為 null 的資料行。</span><span class="sxs-lookup"><span data-stu-id="400e1-214">Nullable column.</span></span> <span data-ttu-id="400e1-215">零表示資料行不可為 null。</span><span class="sxs-lookup"><span data-stu-id="400e1-215">Zero means the column is non-nullable.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="400e1-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span><span class="sxs-lookup"><span data-stu-id="400e1-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span></span><br/>              | <span data-ttu-id="400e1-217">十六進位：0x2000</span><span class="sxs-lookup"><span data-stu-id="400e1-217">Hexadecimal: 0x2000</span></span><br/> <span data-ttu-id="400e1-218">Decimal：8192</span><span class="sxs-lookup"><span data-stu-id="400e1-218">Decimal: 8192</span></span><br/> <span data-ttu-id="400e1-219">主要索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="400e1-219">Primary key column.</span></span> <span data-ttu-id="400e1-220">零表示這個資料行不是主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="400e1-220">Zero means this column is not a primary key.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="400e1-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span><span class="sxs-lookup"><span data-stu-id="400e1-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span></span><br/> | <span data-ttu-id="400e1-222">十六進位： 0x4000 0x8000</span><span class="sxs-lookup"><span data-stu-id="400e1-222">Hexadecimal: 0x4000 0x8000</span></span><br/> <span data-ttu-id="400e1-223">Decimal： 16384 32768</span><span class="sxs-lookup"><span data-stu-id="400e1-223">Decimal: 16384 32768</span></span><br/> <span data-ttu-id="400e1-224">保留</span><span class="sxs-lookup"><span data-stu-id="400e1-224">Reserved</span></span><br/>                                                                                                                                                                                                                                |



 

<span data-ttu-id="400e1-225">如需示範 TransformView 資料表的腳本範例 \_ ，請參閱「 [查看轉換](view-a-transform.md)」。</span><span class="sxs-lookup"><span data-stu-id="400e1-225">For a script sample that demonstrates the \_TransformView table, see [View a Transform](view-a-transform.md).</span></span>

 

 




