---
description: 資料庫物件的 DatabaseState 屬性是唯讀屬性。
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: DatabaseState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987050"
---
# <a name="databasedatabasestate-property"></a><span data-ttu-id="f9e65-103">DatabaseState 屬性</span><span class="sxs-lookup"><span data-stu-id="f9e65-103">Database.DatabaseState property</span></span>

<span data-ttu-id="f9e65-104">[**資料庫**](database-object.md)物件的 **DatabaseState** 屬性是唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="f9e65-104">The **DatabaseState** property of the [**Database**](database-object.md) object is a read-only property.</span></span>

<span data-ttu-id="f9e65-105">這個屬性會以下列其中一個參數傳回資料庫的持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="f9e65-105">This property returns the persistence state of the database as one of the following parameters.</span></span>



| <span data-ttu-id="f9e65-106">資料庫狀態</span><span class="sxs-lookup"><span data-stu-id="f9e65-106">Database state</span></span>        | <span data-ttu-id="f9e65-107">值</span><span class="sxs-lookup"><span data-stu-id="f9e65-107">Value</span></span> | <span data-ttu-id="f9e65-108">描述</span><span class="sxs-lookup"><span data-stu-id="f9e65-108">Description</span></span>                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e65-109">msiDatabaseStateRead</span><span class="sxs-lookup"><span data-stu-id="f9e65-109">msiDatabaseStateRead</span></span>  | <span data-ttu-id="f9e65-110">0</span><span class="sxs-lookup"><span data-stu-id="f9e65-110">0</span></span>     | <span data-ttu-id="f9e65-111">資料庫會以唯讀方式開啟。</span><span class="sxs-lookup"><span data-stu-id="f9e65-111">Database opens as read-only.</span></span> <span data-ttu-id="f9e65-112">不允許變更持續性資料，也不會儲存暫存資料。</span><span class="sxs-lookup"><span data-stu-id="f9e65-112">Changes to persistent data are not permitted and temporary data is not saved.</span></span> |
| <span data-ttu-id="f9e65-113">msiDatabaseStateWrite</span><span class="sxs-lookup"><span data-stu-id="f9e65-113">msiDatabaseStateWrite</span></span> | <span data-ttu-id="f9e65-114">1</span><span class="sxs-lookup"><span data-stu-id="f9e65-114">1</span></span>     | <span data-ttu-id="f9e65-115">資料庫可完全運作以進行讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="f9e65-115">Database is fully operational for read and write.</span></span>                                                          |



 

<span data-ttu-id="f9e65-116">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f9e65-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e65-117">語法</span><span class="sxs-lookup"><span data-stu-id="f9e65-117">Syntax</span></span>


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a><span data-ttu-id="f9e65-118">屬性值</span><span class="sxs-lookup"><span data-stu-id="f9e65-118">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e65-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9e65-119">Requirements</span></span>



| <span data-ttu-id="f9e65-120">需求</span><span class="sxs-lookup"><span data-stu-id="f9e65-120">Requirement</span></span> | <span data-ttu-id="f9e65-121">值</span><span class="sxs-lookup"><span data-stu-id="f9e65-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e65-122">版本</span><span class="sxs-lookup"><span data-stu-id="f9e65-122">Version</span></span><br/> | <span data-ttu-id="f9e65-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f9e65-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f9e65-124">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f9e65-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f9e65-125">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f9e65-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f9e65-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f9e65-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9e65-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9e65-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f9e65-128">IID</span><span class="sxs-lookup"><span data-stu-id="f9e65-128">IID</span></span><br/>     | <span data-ttu-id="f9e65-129">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f9e65-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




