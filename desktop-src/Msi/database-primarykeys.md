---
description: 資料庫物件的 PrimaryKeys 屬性會傳回記錄物件，其中包含欄位0中的資料表名稱和資料行名稱， (在對應至其資料行編號的後續欄位中) 的主鍵。
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: PrimaryKeys 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995501"
---
# <a name="databaseprimarykeys-property"></a><span data-ttu-id="ad7cf-103">PrimaryKeys 屬性</span><span class="sxs-lookup"><span data-stu-id="ad7cf-103">Database.PrimaryKeys property</span></span>

<span data-ttu-id="ad7cf-104">資料庫物件的 **PrimaryKeys** 屬性會傳回 [**記錄**](record-object.md)物件，其中包含欄位0中的資料表名稱和 [**資料**](database-object.md)行名稱， (在對應至其資料行編號的後續欄位中) 的主鍵。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-104">The **PrimaryKeys** property of the [**Database**](database-object.md) object returns a [**Record**](record-object.md) object containing the table name in field 0 and the column names (comprising the primary keys) in succeeding fields corresponding to their column numbers.</span></span> <span data-ttu-id="ad7cf-105">記錄的欄位計數是主鍵資料行的計數。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-105">The field count of the record is the count of primary key columns.</span></span>

<span data-ttu-id="ad7cf-106">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7cf-107">語法</span><span class="sxs-lookup"><span data-stu-id="ad7cf-107">Syntax</span></span>


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a><span data-ttu-id="ad7cf-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="ad7cf-108">Property value</span></span>

<span data-ttu-id="ad7cf-109">現有資料表的必要名稱。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-109">Required name of an existing table.</span></span> <span data-ttu-id="ad7cf-110">如果資料表不存在，就會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-110">An error is generated if the table does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad7cf-111">備註</span><span class="sxs-lookup"><span data-stu-id="ad7cf-111">Remarks</span></span>

<span data-ttu-id="ad7cf-112">**PrimaryKeys** 屬性不能與 [ \_ Tables 資料表](-tables-table.md)或 [ \_ Columns 資料表](-columns-table.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-112">The **PrimaryKeys** property cannot be used with the [\_Tables table](-tables-table.md) or the [\_Columns table](-columns-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7cf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad7cf-113">Requirements</span></span>



| <span data-ttu-id="ad7cf-114">需求</span><span class="sxs-lookup"><span data-stu-id="ad7cf-114">Requirement</span></span> | <span data-ttu-id="ad7cf-115">值</span><span class="sxs-lookup"><span data-stu-id="ad7cf-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7cf-116">版本</span><span class="sxs-lookup"><span data-stu-id="ad7cf-116">Version</span></span><br/> | <span data-ttu-id="ad7cf-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ad7cf-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ad7cf-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ad7cf-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ad7cf-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ad7cf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ad7cf-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad7cf-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad7cf-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ad7cf-122">IID</span><span class="sxs-lookup"><span data-stu-id="ad7cf-122">IID</span></span><br/>     | <span data-ttu-id="ad7cf-123">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ad7cf-123">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




