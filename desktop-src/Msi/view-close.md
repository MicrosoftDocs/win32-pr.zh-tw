---
description: View 物件的 Close 方法會終止查詢執行，並釋放資料庫資源。
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000829"
---
# <a name="viewclose-method"></a><span data-ttu-id="4f698-103">View. Close 方法</span><span class="sxs-lookup"><span data-stu-id="4f698-103">View.Close method</span></span>

<span data-ttu-id="4f698-104">[**View**](view-object.md)物件的 **Close** 方法會終止查詢執行，並釋放資料庫資源。</span><span class="sxs-lookup"><span data-stu-id="4f698-104">The **Close** method of the [**View**](view-object.md) object terminates query execution and releases database resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f698-105">語法</span><span class="sxs-lookup"><span data-stu-id="4f698-105">Syntax</span></span>


```JScript
View.Close()
```



## <a name="parameters"></a><span data-ttu-id="4f698-106">參數</span><span class="sxs-lookup"><span data-stu-id="4f698-106">Parameters</span></span>

<span data-ttu-id="4f698-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4f698-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f698-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f698-108">Return value</span></span>

<span data-ttu-id="4f698-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f698-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f698-110">備註</span><span class="sxs-lookup"><span data-stu-id="4f698-110">Remarks</span></span>

<span data-ttu-id="4f698-111">除非已使用 [**Fetch**](view-fetch.md)方法取得結果集的所有資料列，否則必須在 [**View**](view-object.md)物件上再次呼叫 [**Execute**](view-execute.md)方法之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="4f698-111">This method must be called before the [**Execute**](view-execute.md) method is called again on the [**View**](view-object.md) object unless all rows of the result set have been obtained with the [**Fetch**](view-fetch.md) method.</span></span> <span data-ttu-id="4f698-112">當視圖終結時，它會在內部呼叫。</span><span class="sxs-lookup"><span data-stu-id="4f698-112">It is called internally when the view is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f698-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f698-113">Requirements</span></span>



| <span data-ttu-id="4f698-114">需求</span><span class="sxs-lookup"><span data-stu-id="4f698-114">Requirement</span></span> | <span data-ttu-id="4f698-115">值</span><span class="sxs-lookup"><span data-stu-id="4f698-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f698-116">版本</span><span class="sxs-lookup"><span data-stu-id="4f698-116">Version</span></span><br/> | <span data-ttu-id="4f698-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4f698-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4f698-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4f698-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4f698-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="4f698-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4f698-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4f698-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f698-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f698-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4f698-122">IID</span><span class="sxs-lookup"><span data-stu-id="4f698-122">IID</span></span><br/>     | <span data-ttu-id="4f698-123">IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4f698-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




