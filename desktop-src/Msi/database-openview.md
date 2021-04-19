---
description: 資料庫物件的 OpenView 方法會傳回 View 物件，該物件表示 SQL 字串所指定的查詢。
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: '資料庫. .h 方法 (Certview .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984446"
---
# <a name="databaseopenview-method"></a><span data-ttu-id="0bbad-103">資料庫. OpenView 方法</span><span class="sxs-lookup"><span data-stu-id="0bbad-103">Database.OpenView method</span></span>

<span data-ttu-id="0bbad-104">[**資料庫**](database-object.md)物件的 **OpenView** 方法會傳回 [**View**](view-object.md)物件，該物件表示 SQL 字串所指定的查詢。</span><span class="sxs-lookup"><span data-stu-id="0bbad-104">The **OpenView** method of the [**Database**](database-object.md) object returns a [**View**](view-object.md) object that represents the query specified by a SQL string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbad-105">語法</span><span class="sxs-lookup"><span data-stu-id="0bbad-105">Syntax</span></span>


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a><span data-ttu-id="0bbad-106">參數</span><span class="sxs-lookup"><span data-stu-id="0bbad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bbad-107">*sql*</span><span class="sxs-lookup"><span data-stu-id="0bbad-107">*sql*</span></span> 
</dt> <dd>

<span data-ttu-id="0bbad-108">必要的 SQL 查詢字串。</span><span class="sxs-lookup"><span data-stu-id="0bbad-108">Required SQL query string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bbad-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bbad-109">Return value</span></span>

<span data-ttu-id="0bbad-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0bbad-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bbad-111">備註</span><span class="sxs-lookup"><span data-stu-id="0bbad-111">Remarks</span></span>

<span data-ttu-id="0bbad-112">如需安裝程式中所執行 SQL 語法的詳細資訊，請參閱 [Sql 語法](sql-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="0bbad-112">For information about SQL syntax implemented in the installer, see [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="0bbad-113">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="0bbad-113">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bbad-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bbad-114">Requirements</span></span>



| <span data-ttu-id="0bbad-115">需求</span><span class="sxs-lookup"><span data-stu-id="0bbad-115">Requirement</span></span> | <span data-ttu-id="0bbad-116">值</span><span class="sxs-lookup"><span data-stu-id="0bbad-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbad-117">版本</span><span class="sxs-lookup"><span data-stu-id="0bbad-117">Version</span></span><br/> | <span data-ttu-id="0bbad-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="0bbad-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0bbad-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="0bbad-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0bbad-120">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0bbad-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0bbad-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0bbad-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0bbad-122"><dt>Certview。h</dt></span><span class="sxs-lookup"><span data-stu-id="0bbad-122"><dt>Certview.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="0bbad-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0bbad-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0bbad-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bbad-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0bbad-125">IID</span><span class="sxs-lookup"><span data-stu-id="0bbad-125">IID</span></span><br/>     | <span data-ttu-id="0bbad-126">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0bbad-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0bbad-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bbad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bbad-128">**資料庫**</span><span class="sxs-lookup"><span data-stu-id="0bbad-128">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="0bbad-129">SQL 語法</span><span class="sxs-lookup"><span data-stu-id="0bbad-129">SQL Syntax</span></span>](sql-syntax.md)
</dt> </dl>

 

 




