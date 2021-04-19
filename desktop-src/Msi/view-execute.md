---
description: View 物件的 Execute 方法會使用問號標記來代表 SQL 語句中的參數。 如需詳細資訊，請參閱 SQL 語法。 這些參數的值會傳入做為參數記錄的對應欄位。
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exe刻意的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982510"
---
# <a name="viewexecute-method"></a><span data-ttu-id="e1227-105">View.Exe刻意的方法</span><span class="sxs-lookup"><span data-stu-id="e1227-105">View.Execute method</span></span>

<span data-ttu-id="e1227-106">[**View**](view-object.md)物件的 **Execute** 方法會使用問號標記來代表 SQL 語句中的參數。</span><span class="sxs-lookup"><span data-stu-id="e1227-106">The **Execute** method of the [**View**](view-object.md) object uses the question mark token to represent parameters in an SQL statement.</span></span> <span data-ttu-id="e1227-107">如需詳細資訊，請參閱 [SQL 語法](sql-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="e1227-107">For more information, see [SQL Syntax](sql-syntax.md).</span></span> <span data-ttu-id="e1227-108">這些參數的值會傳入做為參數記錄的對應欄位。</span><span class="sxs-lookup"><span data-stu-id="e1227-108">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1227-109">語法</span><span class="sxs-lookup"><span data-stu-id="e1227-109">Syntax</span></span>


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="e1227-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1227-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1227-111">*記錄*</span><span class="sxs-lookup"><span data-stu-id="e1227-111">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="e1227-112">選擇性 [**記錄**](record-object.md) 物件，其中包含在 SQL 查詢中 (？ ) 取代參數標記的值。</span><span class="sxs-lookup"><span data-stu-id="e1227-112">Optional [**Record**](record-object.md) objects that contains the values that replace the parameter tokens (?) in the SQL query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1227-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1227-113">Return value</span></span>

<span data-ttu-id="e1227-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e1227-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1227-115">備註</span><span class="sxs-lookup"><span data-stu-id="e1227-115">Remarks</span></span>

<span data-ttu-id="e1227-116">您必須在對 [**Fetch**](view-fetch.md) 方法的任何呼叫之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e1227-116">This method must be called before any calls to the [**Fetch**](view-fetch.md) method.</span></span>

<span data-ttu-id="e1227-117">如果 SQL 查詢指定具有參數標記 (？ ) 的值，則必須提供包含所有取代值的記錄，而這些取代值必須與參數標記具有相同的順序和相同的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e1227-117">If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values, which must be in the same order and of the same data type as the parameter markers.</span></span> <span data-ttu-id="e1227-118">當此方法與 INSERT 和 UPDATE 查詢搭配使用時，問號標記必須在所有非參數化的值之前。</span><span class="sxs-lookup"><span data-stu-id="e1227-118">When this method is used with INSERT and UPDATE queries, the question mark tokens must precede all the non-parameterized values.</span></span>

<span data-ttu-id="e1227-119">例如，以下是有效的查詢：</span><span class="sxs-lookup"><span data-stu-id="e1227-119">For example, these queries are valid:</span></span>

<span data-ttu-id="e1227-120">更新 {資料表清單} 集合 {column} =？</span><span class="sxs-lookup"><span data-stu-id="e1227-120">UPDATE {table-list} SET {column}= ?</span></span> <span data-ttu-id="e1227-121">，{column} = {常數}</span><span class="sxs-lookup"><span data-stu-id="e1227-121">, {column}= {constant}</span></span>

<span data-ttu-id="e1227-122">插入 {table} ( {column-list} ) 值 (？，{常數清單} ) </span><span class="sxs-lookup"><span data-stu-id="e1227-122">INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})</span></span>

<span data-ttu-id="e1227-123">不過，這些查詢無效：</span><span class="sxs-lookup"><span data-stu-id="e1227-123">However these queries are invalid:</span></span>

<span data-ttu-id="e1227-124">更新 {資料表清單} 集合 {column} = {常數}，{column} =？</span><span class="sxs-lookup"><span data-stu-id="e1227-124">UPDATE {table-list} SET {column}= {constant}, {column}=?</span></span>

<span data-ttu-id="e1227-125">插入 {table} ( {column-list} ) 值 ( {常數清單} 中？</span><span class="sxs-lookup"><span data-stu-id="e1227-125">INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ?</span></span> <span data-ttu-id="e1227-126">)</span><span class="sxs-lookup"><span data-stu-id="e1227-126">)</span></span>

<span data-ttu-id="e1227-127">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="e1227-127">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1227-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1227-128">Requirements</span></span>



| <span data-ttu-id="e1227-129">需求</span><span class="sxs-lookup"><span data-stu-id="e1227-129">Requirement</span></span> | <span data-ttu-id="e1227-130">值</span><span class="sxs-lookup"><span data-stu-id="e1227-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1227-131">版本</span><span class="sxs-lookup"><span data-stu-id="e1227-131">Version</span></span><br/> | <span data-ttu-id="e1227-132">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e1227-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1227-133">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e1227-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1227-134">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e1227-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e1227-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e1227-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1227-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1227-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e1227-137">IID</span><span class="sxs-lookup"><span data-stu-id="e1227-137">IID</span></span><br/>     | <span data-ttu-id="e1227-138">IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e1227-138">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




