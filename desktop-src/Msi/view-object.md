---
description: View 物件代表使用資料庫物件的 OpenView 方法處理查詢時所取得的結果集。
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: View 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994122"
---
# <a name="view-object"></a><span data-ttu-id="414b4-103">View 物件</span><span class="sxs-lookup"><span data-stu-id="414b4-103">View object</span></span>

<span data-ttu-id="414b4-104">**View** 物件代表使用 [**資料庫**](database-object.md)物件的 [**OpenView**](database-openview.md)方法處理查詢時所取得的結果集。</span><span class="sxs-lookup"><span data-stu-id="414b4-104">The **View** object represents a result set obtained when processing a query using the [**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="414b4-105">在可以傳輸任何資料之前，必須使用 [**Execute**](view-execute.md) 方法來執行查詢，並將 SQL 查詢字串中指定的所有可取代參數傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="414b4-105">Before any data can be transferred, the query must be executed using the [**Execute**](view-execute.md) method, passing to it all replaceable parameters designated within the SQL query string.</span></span> <span data-ttu-id="414b4-106">您可以視需要使用不同的參數再次執行查詢，但只在釋放結果集之後，只要提取所有記錄或呼叫 [**Close**](view-close.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="414b4-106">The query may be executed again, with different parameters if needed, but only after freeing the result set either by fetching all the records or by calling the [**Close**](view-close.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="414b4-107">成員</span><span class="sxs-lookup"><span data-stu-id="414b4-107">Members</span></span>

<span data-ttu-id="414b4-108">**View** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="414b4-108">The **View** object has these types of members:</span></span>

-   [<span data-ttu-id="414b4-109">方法</span><span class="sxs-lookup"><span data-stu-id="414b4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="414b4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="414b4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="414b4-111">方法</span><span class="sxs-lookup"><span data-stu-id="414b4-111">Methods</span></span>

<span data-ttu-id="414b4-112">**View** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="414b4-112">The **View** object has these methods.</span></span>



| <span data-ttu-id="414b4-113">方法</span><span class="sxs-lookup"><span data-stu-id="414b4-113">Method</span></span>                            | <span data-ttu-id="414b4-114">描述</span><span class="sxs-lookup"><span data-stu-id="414b4-114">Description</span></span>                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="414b4-115">**關閉**</span><span class="sxs-lookup"><span data-stu-id="414b4-115">**Close**</span></span>](view-close.md)       | <span data-ttu-id="414b4-116">終止查詢執行並釋放資料庫資源。</span><span class="sxs-lookup"><span data-stu-id="414b4-116">Terminates query execution and releases database resources.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="414b4-117">**執行**</span><span class="sxs-lookup"><span data-stu-id="414b4-117">**Execute**</span></span>](view-execute.md)   | <span data-ttu-id="414b4-118">使用問號標記來代表 SQL 查詢中的參數。</span><span class="sxs-lookup"><span data-stu-id="414b4-118">Uses the question mark token to represent parameters in a SQL query.</span></span> <span data-ttu-id="414b4-119">這些參數的值會傳入做為參數記錄的對應欄位。</span><span class="sxs-lookup"><span data-stu-id="414b4-119">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span><br/> |
| [<span data-ttu-id="414b4-120">**獲取**</span><span class="sxs-lookup"><span data-stu-id="414b4-120">**Fetch**</span></span>](view-fetch.md)       | <span data-ttu-id="414b4-121">如果結果集中有多個資料列可供使用，則傳回包含所要求資料行資料的 [**記錄**](record-object.md) 物件，否則會傳回 null。</span><span class="sxs-lookup"><span data-stu-id="414b4-121">Returns a [**Record**](record-object.md) object containing the requested column data if more rows are available in the result set, otherwise, it returns null.</span></span><br/>      |
| [<span data-ttu-id="414b4-122">**GetError**</span><span class="sxs-lookup"><span data-stu-id="414b4-122">**GetError**</span></span>](view-geterror.md) | <span data-ttu-id="414b4-123">傳回發生錯誤的驗證錯誤和資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="414b4-123">Returns the Validation error and column name for which the error occurred.</span></span><br/>                                                                                           |
| [<span data-ttu-id="414b4-124">**修改**</span><span class="sxs-lookup"><span data-stu-id="414b4-124">**Modify**</span></span>](view-modify.md)     | <span data-ttu-id="414b4-125">使用 [**Fetch**](view-fetch.md)方法取得的修改 [**記錄**](record-object.md)物件來修改資料庫資料列。</span><span class="sxs-lookup"><span data-stu-id="414b4-125">Modifies a database row with a modified [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method.</span></span><br/>                                   |



 

### <a name="properties"></a><span data-ttu-id="414b4-126">屬性</span><span class="sxs-lookup"><span data-stu-id="414b4-126">Properties</span></span>

<span data-ttu-id="414b4-127">**View** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="414b4-127">The **View** object has these properties.</span></span>



| <span data-ttu-id="414b4-128">屬性</span><span class="sxs-lookup"><span data-stu-id="414b4-128">Property</span></span>                                         | <span data-ttu-id="414b4-129">描述</span><span class="sxs-lookup"><span data-stu-id="414b4-129">Description</span></span>                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="414b4-130">**ColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="414b4-130">**ColumnInfo**</span></span>](view-columninfo.md)<br/> | <span data-ttu-id="414b4-131">傳回 [**記錄**](record-object.md) 物件，其中包含結果集中每個資料行的要求資訊。</span><span class="sxs-lookup"><span data-stu-id="414b4-131">Returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="414b4-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="414b4-132">Requirements</span></span>



| <span data-ttu-id="414b4-133">需求</span><span class="sxs-lookup"><span data-stu-id="414b4-133">Requirement</span></span> | <span data-ttu-id="414b4-134">值</span><span class="sxs-lookup"><span data-stu-id="414b4-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="414b4-135">版本</span><span class="sxs-lookup"><span data-stu-id="414b4-135">Version</span></span><br/> | <span data-ttu-id="414b4-136">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="414b4-136">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="414b4-137">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="414b4-137">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="414b4-138">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="414b4-138">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="414b4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="414b4-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="414b4-140"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="414b4-140"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="414b4-141">IID</span><span class="sxs-lookup"><span data-stu-id="414b4-141">IID</span></span><br/>     | <span data-ttu-id="414b4-142">IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="414b4-142">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="414b4-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="414b4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414b4-144">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="414b4-144">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




