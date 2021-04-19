---
description: 資料庫物件會存取安裝程式資料庫。
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: 資料庫物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996084"
---
# <a name="database-object"></a><span data-ttu-id="7d482-103">資料庫物件</span><span class="sxs-lookup"><span data-stu-id="7d482-103">Database object</span></span>

<span data-ttu-id="7d482-104">**資料庫** 物件會存取安裝程式資料庫。</span><span class="sxs-lookup"><span data-stu-id="7d482-104">The **Database** object accesses an installer database.</span></span>

<span data-ttu-id="7d482-105">當 **資料庫** 物件被移出範圍，或與其相關聯的物件變數設定為 null 時，就會釋放該物件。</span><span class="sxs-lookup"><span data-stu-id="7d482-105">The **Database** object is released when it is either taken out of scope or when the object variable associated with it is set to null.</span></span> <span data-ttu-id="7d482-106">您必須在釋放 **資料庫** 物件之前呼叫 [**Commit**](database-commit.md)方法，以寫出所有持續性變更。</span><span class="sxs-lookup"><span data-stu-id="7d482-106">The [**Commit**](database-commit.md) method must be called before the **Database** object is released to write out all persistent changes.</span></span> <span data-ttu-id="7d482-107">如果未呼叫 **Commit** 方法，安裝程式會在物件終結時執行隱含復原。</span><span class="sxs-lookup"><span data-stu-id="7d482-107">If the **Commit** method is not called, the installer performs an implicit rollback upon object destruction.</span></span>

<span data-ttu-id="7d482-108">用戶端可以使用下列程式進行資料存取。</span><span class="sxs-lookup"><span data-stu-id="7d482-108">The client can use the following procedure for data access.</span></span>

<span data-ttu-id="7d482-109">**若要查詢 API 排序**</span><span class="sxs-lookup"><span data-stu-id="7d482-109">**To Query API Sequencing**</span></span>

1.  <span data-ttu-id="7d482-110">藉由呼叫 [**OpenDatabase**](installer-opendatabase.md)或 [**安裝程式**](installer-object.md)物件來取得 **資料庫** 物件。</span><span class="sxs-lookup"><span data-stu-id="7d482-110">Obtain a **Database** object by calling the [**OpenDatabase**](installer-opendatabase.md) or the [**Installer**](installer-object.md) object.</span></span>
2.  <span data-ttu-id="7d482-111">藉由呼叫 **Database** 物件的 [**OpenView**](database-openview.md)方法，使用 SQL 字串初始化查詢。</span><span class="sxs-lookup"><span data-stu-id="7d482-111">Initiate a query using a SQL string by calling the [**OpenView**](database-openview.md) method of the **Database** object.</span></span>
3.  <span data-ttu-id="7d482-112">在 [**記錄**](record-object.md)物件中設定查詢參數，並藉由呼叫 [**View**](view-object.md)物件的 [**execute**](view-execute.md)方法來執行資料庫查詢。</span><span class="sxs-lookup"><span data-stu-id="7d482-112">Set query parameters in a [**Record**](record-object.md) object and execute the database query by calling the [**Execute**](view-execute.md) method of the [**View**](view-object.md) object.</span></span> <span data-ttu-id="7d482-113">這會產生可提取或更新的結果。</span><span class="sxs-lookup"><span data-stu-id="7d482-113">This produces a result that can be fetched or updated.</span></span>
4.  <span data-ttu-id="7d482-114">重複呼叫 [**View**](view-object.md)物件的 [**Fetch**](view-fetch.md)方法，以傳回 [**記錄**](record-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="7d482-114">Call the [**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object repeatedly to return [**Record**](record-object.md) objects.</span></span>
5.  <span data-ttu-id="7d482-115">使用 [**View**](view-object.md)物件的 [**Modify**](view-modify.md)方法，更新 [**Fetch**](view-fetch.md)方法所取得之 [**記錄**](record-object.md)物件的資料庫資料列。</span><span class="sxs-lookup"><span data-stu-id="7d482-115">Update database rows of a [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method using the [**Modify**](view-modify.md) method of the [**View**](view-object.md) object.</span></span>
6.  <span data-ttu-id="7d482-116">藉由呼叫 [**View**](view-object.md)物件的 [**Close**](view-close.md)方法來釋放查詢和任何 unfetched 記錄。</span><span class="sxs-lookup"><span data-stu-id="7d482-116">Release the query and any unfetched records by calling the [**Close**](view-close.md) method of the [**View**](view-object.md) object.</span></span>
7.  <span data-ttu-id="7d482-117">藉由呼叫 **database** 物件的 [**Commit**](database-commit.md)方法，保存任何資料庫更新。</span><span class="sxs-lookup"><span data-stu-id="7d482-117">Persist any database updates by calling the [**Commit**](database-commit.md) method of the **Database** object.</span></span>

## <a name="members"></a><span data-ttu-id="7d482-118">成員</span><span class="sxs-lookup"><span data-stu-id="7d482-118">Members</span></span>

<span data-ttu-id="7d482-119">**資料庫** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7d482-119">The **Database** object has these types of members:</span></span>

-   [<span data-ttu-id="7d482-120">方法</span><span class="sxs-lookup"><span data-stu-id="7d482-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="7d482-121">屬性</span><span class="sxs-lookup"><span data-stu-id="7d482-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7d482-122">方法</span><span class="sxs-lookup"><span data-stu-id="7d482-122">Methods</span></span>

<span data-ttu-id="7d482-123">**資料庫** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7d482-123">The **Database** object has these methods.</span></span>



| <span data-ttu-id="7d482-124">方法</span><span class="sxs-lookup"><span data-stu-id="7d482-124">Method</span></span>                                                                    | <span data-ttu-id="7d482-125">描述</span><span class="sxs-lookup"><span data-stu-id="7d482-125">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d482-126">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="7d482-126">**ApplyTransform**</span></span>](database-applytransform.md)                         | <span data-ttu-id="7d482-127">將轉換套用至這個資料庫。</span><span class="sxs-lookup"><span data-stu-id="7d482-127">Applies the transform to this database.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="7d482-128">**Commit**</span><span class="sxs-lookup"><span data-stu-id="7d482-128">**Commit**</span></span>](database-commit.md)                                         | <span data-ttu-id="7d482-129">完成資料庫的持續性形式。</span><span class="sxs-lookup"><span data-stu-id="7d482-129">Finalizes the persistent form of the database.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="7d482-130">**CreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="7d482-130">**CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md) | <span data-ttu-id="7d482-131">建立並填入現有轉換檔案的摘要資訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="7d482-131">Creates and populates the summary information stream of an existing transform file.</span></span><br/>                                                                            |
| [<span data-ttu-id="7d482-132">**EnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="7d482-132">**EnableUIPreview**</span></span>](database-enableuipreview.md)                       | <span data-ttu-id="7d482-133">藉由提供所需的支援來查看儲存在安裝程式資料庫中的使用者介面對話方塊，以加速撰寫對話方塊和公告欄。</span><span class="sxs-lookup"><span data-stu-id="7d482-133">Facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span><br/> |
| [<span data-ttu-id="7d482-134">**出口**</span><span class="sxs-lookup"><span data-stu-id="7d482-134">**Export**</span></span>](database-export.md)                                         | <span data-ttu-id="7d482-135">將指定資料表中的結構和資料複製到文字封存檔案。</span><span class="sxs-lookup"><span data-stu-id="7d482-135">Copies the structure and data from a specified table to a text archive file.</span></span><br/>                                                                                   |
| [<span data-ttu-id="7d482-136">**基表**</span><span class="sxs-lookup"><span data-stu-id="7d482-136">**GenerateTransform**</span></span>](database-generatetransform.md)                   | <span data-ttu-id="7d482-137">建立轉換。</span><span class="sxs-lookup"><span data-stu-id="7d482-137">Creates a transform.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="7d482-138">**匯入**</span><span class="sxs-lookup"><span data-stu-id="7d482-138">**Import**</span></span>](database-import.md)                                         | <span data-ttu-id="7d482-139">從文字保存檔案匯入資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="7d482-139">Imports a database table from a text archive file.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="7d482-140">**合併**</span><span class="sxs-lookup"><span data-stu-id="7d482-140">**Merge**</span></span>](database-merge.md)                                           | <span data-ttu-id="7d482-141">合併參考資料庫與基底資料庫。</span><span class="sxs-lookup"><span data-stu-id="7d482-141">Merges the reference database with the base database.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="7d482-142">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="7d482-142">**OpenView**</span></span>](database-openview.md)                                     | <span data-ttu-id="7d482-143">傳回 [**View**](view-object.md) 物件，表示 SQL 字串所指定的查詢。</span><span class="sxs-lookup"><span data-stu-id="7d482-143">Returns a [**View**](view-object.md) object representing the query specified by a SQL string.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="7d482-144">屬性</span><span class="sxs-lookup"><span data-stu-id="7d482-144">Properties</span></span>

<span data-ttu-id="7d482-145">**資料庫** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7d482-145">The **Database** object has these properties.</span></span>



| <span data-ttu-id="7d482-146">屬性</span><span class="sxs-lookup"><span data-stu-id="7d482-146">Property</span></span>                                                                               | <span data-ttu-id="7d482-147">描述</span><span class="sxs-lookup"><span data-stu-id="7d482-147">Description</span></span>                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d482-148">**DatabaseState**</span><span class="sxs-lookup"><span data-stu-id="7d482-148">**DatabaseState**</span></span>](database-databasestate.md)<br/>                             | <span data-ttu-id="7d482-149">傳回資料庫的持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="7d482-149">Returns the persistence state of the database.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="7d482-150">**PrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="7d482-150">**PrimaryKeys**</span></span>](database-primarykeys.md)<br/>                                 | <span data-ttu-id="7d482-151">傳回包含資料表名稱和資料行名稱的 [**記錄**](record-object.md) 物件， (將主鍵組成) 。</span><span class="sxs-lookup"><span data-stu-id="7d482-151">Returns a [**Record**](record-object.md) object containing the table name and the column names (comprising the primary keys).</span></span><br/>                        |
| [<span data-ttu-id="7d482-152">**SummaryInformation (資料庫物件)**</span><span class="sxs-lookup"><span data-stu-id="7d482-152">**SummaryInformation (Database Object)**</span></span>](database-summaryinformation.md)<br/> | <span data-ttu-id="7d482-153">傳回 [**SummaryInfo**](summaryinfo-object.md) 物件，這個物件可以用來檢查、更新和加入屬性至摘要資訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="7d482-153">Returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream.</span></span><br/> |
| [<span data-ttu-id="7d482-154">**TablePersistent**</span><span class="sxs-lookup"><span data-stu-id="7d482-154">**TablePersistent**</span></span>](database-tablepersistent.md)<br/>                         | <span data-ttu-id="7d482-155">傳回資料表的持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="7d482-155">Returns the persistence state of the table.</span></span><br/>                                                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="7d482-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d482-156">Requirements</span></span>



| <span data-ttu-id="7d482-157">需求</span><span class="sxs-lookup"><span data-stu-id="7d482-157">Requirement</span></span> | <span data-ttu-id="7d482-158">值</span><span class="sxs-lookup"><span data-stu-id="7d482-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d482-159">版本</span><span class="sxs-lookup"><span data-stu-id="7d482-159">Version</span></span><br/> | <span data-ttu-id="7d482-160">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7d482-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7d482-161">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7d482-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7d482-162">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7d482-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7d482-163">DLL</span><span class="sxs-lookup"><span data-stu-id="7d482-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d482-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d482-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7d482-165">IID</span><span class="sxs-lookup"><span data-stu-id="7d482-165">IID</span></span><br/>     | <span data-ttu-id="7d482-166">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7d482-166">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="7d482-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d482-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d482-168">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="7d482-168">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




