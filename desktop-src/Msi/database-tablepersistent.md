---
description: 資料庫物件的 TablePersistent 屬性會以下列其中一個參數傳回資料表的持續性狀態。
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: TablePersistent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999521"
---
# <a name="databasetablepersistent-property"></a><span data-ttu-id="50e5d-103">TablePersistent 屬性</span><span class="sxs-lookup"><span data-stu-id="50e5d-103">Database.TablePersistent property</span></span>

<span data-ttu-id="50e5d-104">[**資料庫**](database-object.md)物件的 **TablePersistent** 屬性會以下列其中一個參數傳回資料表的持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="50e5d-104">The **TablePersistent** property of the [**Database**](database-object.md) object returns the persistence state of the table as one of the following parameters.</span></span>



| <span data-ttu-id="50e5d-105">資料表狀態</span><span class="sxs-lookup"><span data-stu-id="50e5d-105">Table state</span></span>               | <span data-ttu-id="50e5d-106">值</span><span class="sxs-lookup"><span data-stu-id="50e5d-106">Value</span></span> | <span data-ttu-id="50e5d-107">描述</span><span class="sxs-lookup"><span data-stu-id="50e5d-107">Description</span></span>                    |
|---------------------------|-------|--------------------------------|
| <span data-ttu-id="50e5d-108">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="50e5d-108">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="50e5d-109">0</span><span class="sxs-lookup"><span data-stu-id="50e5d-109">0</span></span>     | <span data-ttu-id="50e5d-110">資料表是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="50e5d-110">Table is temporary.</span></span>            |
| <span data-ttu-id="50e5d-111">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="50e5d-111">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="50e5d-112">1</span><span class="sxs-lookup"><span data-stu-id="50e5d-112">1</span></span>     | <span data-ttu-id="50e5d-113">資料表是永久性的。</span><span class="sxs-lookup"><span data-stu-id="50e5d-113">Table is persistent.</span></span>           |
| <span data-ttu-id="50e5d-114">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="50e5d-114">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="50e5d-115">2</span><span class="sxs-lookup"><span data-stu-id="50e5d-115">2</span></span>     | <span data-ttu-id="50e5d-116">資料表不在資料庫中。</span><span class="sxs-lookup"><span data-stu-id="50e5d-116">Table is not in the database.</span></span>  |
| <span data-ttu-id="50e5d-117">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="50e5d-117">msiEvaluateConditionError</span></span> | <span data-ttu-id="50e5d-118">3</span><span class="sxs-lookup"><span data-stu-id="50e5d-118">3</span></span>     | <span data-ttu-id="50e5d-119">無效或遺漏資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="50e5d-119">Invalid or missing table name.</span></span> |



 

<span data-ttu-id="50e5d-120">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="50e5d-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e5d-121">語法</span><span class="sxs-lookup"><span data-stu-id="50e5d-121">Syntax</span></span>


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a><span data-ttu-id="50e5d-122">屬性值</span><span class="sxs-lookup"><span data-stu-id="50e5d-122">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="50e5d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="50e5d-123">Requirements</span></span>



| <span data-ttu-id="50e5d-124">需求</span><span class="sxs-lookup"><span data-stu-id="50e5d-124">Requirement</span></span> | <span data-ttu-id="50e5d-125">值</span><span class="sxs-lookup"><span data-stu-id="50e5d-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e5d-126">版本</span><span class="sxs-lookup"><span data-stu-id="50e5d-126">Version</span></span><br/> | <span data-ttu-id="50e5d-127">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="50e5d-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="50e5d-128">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="50e5d-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="50e5d-129">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="50e5d-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="50e5d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="50e5d-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="50e5d-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e5d-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="50e5d-132">IID</span><span class="sxs-lookup"><span data-stu-id="50e5d-132">IID</span></span><br/>     | <span data-ttu-id="50e5d-133">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="50e5d-133">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




