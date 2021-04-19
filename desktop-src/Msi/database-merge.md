---
description: 資料庫物件的 Merge 方法會合並參考資料庫與基底資料庫。
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994148"
---
# <a name="databasemerge-method"></a><span data-ttu-id="b9ee3-103">Database. Merge 方法</span><span class="sxs-lookup"><span data-stu-id="b9ee3-103">Database.Merge method</span></span>

<span data-ttu-id="b9ee3-104">[**資料庫**](database-object.md)物件的 **Merge** 方法會合並參考資料庫與基底資料庫。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-104">The **Merge** method of the [**Database**](database-object.md) object merges the reference database with the base database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ee3-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9ee3-105">Syntax</span></span>


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a><span data-ttu-id="b9ee3-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9ee3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ee3-107">*reference*</span><span class="sxs-lookup"><span data-stu-id="b9ee3-107">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="b9ee3-108">要合併到資料庫的必要 [**資料庫**](database-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-108">The required [**Database**](database-object.md) object to be merged into the database.</span></span>

</dd> <dt>

<span data-ttu-id="b9ee3-109">*errorTable*</span><span class="sxs-lookup"><span data-stu-id="b9ee3-109">*errorTable*</span></span> 
</dt> <dd>

<span data-ttu-id="b9ee3-110">資料表的選擇性名稱，包含包含合併衝突之資料表的名稱、資料表中的衝突資料列數目，以及包含合併衝突之資料表的參考。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-110">An optional name of a table to contain the names of the tables containing merge conflicts, the number of conflicting rows within the table, and a reference to the table with the merge conflict.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ee3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9ee3-111">Return value</span></span>

<span data-ttu-id="b9ee3-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9ee3-113">備註</span><span class="sxs-lookup"><span data-stu-id="b9ee3-113">Remarks</span></span>

<span data-ttu-id="b9ee3-114">[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)函式和 [**資料庫**](database-object.md)物件的 **merge** 方法不能用來合併安裝封裝內所含的模組。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-114">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the **Merge** method of the [**Database**](database-object.md) object cannot be used to merge a module included within an installation package.</span></span> <span data-ttu-id="b9ee3-115">它們不應該用來將 [合併模組](merge-modules.md) 合併成 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-115">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="b9ee3-116">若要在安裝套件中包含合併模組，安裝套件的作者應遵循套用 [合併模組](applying-merge-modules.md) 主題中所述的指導方針。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-116">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="b9ee3-117">**Merge** 方法不會將內嵌的封 [包](cabinet-files.md)檔或 [內嵌的轉換](embedded-transforms.md)從參考資料庫複製到目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-117">The **Merge** method does not copy over embedded [cabinet files](cabinet-files.md) or [embedded transforms](embedded-transforms.md) from the reference database into the target database.</span></span> <span data-ttu-id="b9ee3-118">[二進位資料表](binary-table.md)或[圖示資料表](icon-table.md)中所列的內嵌資料串流，會從參考資料庫複製到目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-118">Embedded data streams that are listed in the [Binary Table](binary-table.md) or [Icon Table](icon-table.md) are copied from the reference database to the target database.</span></span> <span data-ttu-id="b9ee3-119">內嵌于參考資料庫中的儲存體不會複製到目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-119">Storages embedded in the reference database are not copied to the target database.</span></span>

<span data-ttu-id="b9ee3-120">如果未提供任何資料表，則一般錯誤訊息會提供包含合併衝突的資料表數目。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-120">If no table is provided, the general error message provides the number of tables containing merge conflicts.</span></span> <span data-ttu-id="b9ee3-121">可以傳入任何資料表，但所有其他資料行都必須是可為 null，因為如果資料行不可為 null，則更新 [錯誤資料表](error-table.md) 的作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-121">Any table can be passed in, but all other columns must be nullable because the operation to update the [Error Table](error-table.md) fails if a column is not nullable.</span></span> <span data-ttu-id="b9ee3-122">您也可以傳入新建立的資料表，因為當找到合併衝突時， **merge** 方法會自動建立所使用的資料行。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-122">A newly created table can be passed in as well because the **Merge** method automatically creates the columns it uses if merge conflicts are found.</span></span> <span data-ttu-id="b9ee3-123">有兩個數據行用來呈現合併衝突。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-123">Two columns are used to present merge conflicts.</span></span> <span data-ttu-id="b9ee3-124">第一個資料行是資料表名稱和主鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-124">The first column is the table name and the primary key column.</span></span> <span data-ttu-id="b9ee3-125">第二個數據行是該資料表中有合併失敗的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-125">The second column is the number of rows of that table that have merge failures.</span></span>

<span data-ttu-id="b9ee3-126">如果兩個資料庫中相同名稱的資料表不符合主鍵的數目、資料行類型、資料行數目或資料行名稱， **合併** 方法將會失敗，並張貼一則錯誤訊息，指出發生了什麼事。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-126">If tables of the same name in both databases do not match in the number of primary keys, the column types, the number of columns, or the column names, the **Merge** method fails and posts an error message stating what occurred.</span></span>

<span data-ttu-id="b9ee3-127">若要保留錯誤資料表，錯誤處理常式必須認可錯誤資料表所屬的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-127">For the Error table to remain, the error handler must commit the database to which the Error table belongs.</span></span> <span data-ttu-id="b9ee3-128">不過，您應該在使用第三個數據行來取得發生合併衝突之資料表的參考之後，進行這種認可。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-128">However, this commit should be done after using the third column to obtain the references to those tables where merge conflicts occurred.</span></span>

<span data-ttu-id="b9ee3-129">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-129">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ee3-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9ee3-130">Requirements</span></span>



| <span data-ttu-id="b9ee3-131">需求</span><span class="sxs-lookup"><span data-stu-id="b9ee3-131">Requirement</span></span> | <span data-ttu-id="b9ee3-132">值</span><span class="sxs-lookup"><span data-stu-id="b9ee3-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ee3-133">版本</span><span class="sxs-lookup"><span data-stu-id="b9ee3-133">Version</span></span><br/> | <span data-ttu-id="b9ee3-134">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b9ee3-135">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="b9ee3-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b9ee3-136">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b9ee3-136">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b9ee3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b9ee3-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="b9ee3-138"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ee3-138"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b9ee3-139">IID</span><span class="sxs-lookup"><span data-stu-id="b9ee3-139">IID</span></span><br/>     | <span data-ttu-id="b9ee3-140">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b9ee3-140">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




