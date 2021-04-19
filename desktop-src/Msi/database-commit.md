---
description: 資料庫物件的 Commit 方法會完成資料庫的持續性形式。
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001150"
---
# <a name="databasecommit-method"></a><span data-ttu-id="2b60e-103">Database. Commit 方法</span><span class="sxs-lookup"><span data-stu-id="2b60e-103">Database.Commit method</span></span>

<span data-ttu-id="2b60e-104">[**資料庫**](database-object.md)物件的 **Commit** 方法會完成資料庫的持續性形式。</span><span class="sxs-lookup"><span data-stu-id="2b60e-104">The **Commit** method of the [**Database**](database-object.md) object finalizes the persistent form of the database.</span></span> <span data-ttu-id="2b60e-105">所有持續性資料都會寫入至可寫入的資料庫，而且不會寫入任何暫存資料行或資料列。</span><span class="sxs-lookup"><span data-stu-id="2b60e-105">All persistent data is written to the writeable database, and no temporary columns or rows are written.</span></span> <span data-ttu-id="2b60e-106">這個方法不會影響以唯讀方式開啟的資料庫。</span><span class="sxs-lookup"><span data-stu-id="2b60e-106">This method has no effect on a database opened as read-only.</span></span> <span data-ttu-id="2b60e-107">您可以多次呼叫這個方法，以儲存載入記憶體之資料表的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="2b60e-107">This method can be called multiple times to save the current state of tables loaded into memory.</span></span> <span data-ttu-id="2b60e-108">當資料庫最後關閉時，最後一次 **認可** 之後所做的任何變更都會復原。</span><span class="sxs-lookup"><span data-stu-id="2b60e-108">When the database is finally closed, any changes made subsequent to the last **Commit** are rolled back.</span></span> <span data-ttu-id="2b60e-109">當所有資料庫變更都已完成時，通常會在關閉之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2b60e-109">This method is normally called prior to shutdown when all database changes have been finalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b60e-110">語法</span><span class="sxs-lookup"><span data-stu-id="2b60e-110">Syntax</span></span>


```JScript
Database.Commit()
```



## <a name="parameters"></a><span data-ttu-id="2b60e-111">參數</span><span class="sxs-lookup"><span data-stu-id="2b60e-111">Parameters</span></span>

<span data-ttu-id="2b60e-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2b60e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b60e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b60e-113">Return value</span></span>

<span data-ttu-id="2b60e-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2b60e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b60e-115">備註</span><span class="sxs-lookup"><span data-stu-id="2b60e-115">Remarks</span></span>

<span data-ttu-id="2b60e-116">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="2b60e-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b60e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b60e-117">Requirements</span></span>



| <span data-ttu-id="2b60e-118">需求</span><span class="sxs-lookup"><span data-stu-id="2b60e-118">Requirement</span></span> | <span data-ttu-id="2b60e-119">值</span><span class="sxs-lookup"><span data-stu-id="2b60e-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b60e-120">版本</span><span class="sxs-lookup"><span data-stu-id="2b60e-120">Version</span></span><br/> | <span data-ttu-id="2b60e-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="2b60e-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2b60e-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="2b60e-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2b60e-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2b60e-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2b60e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2b60e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b60e-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b60e-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2b60e-126">IID</span><span class="sxs-lookup"><span data-stu-id="2b60e-126">IID</span></span><br/>     | <span data-ttu-id="2b60e-127">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2b60e-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




