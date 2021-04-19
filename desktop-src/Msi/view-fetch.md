---
description: 如果結果集中有多個資料列，則 View 物件的 Fetch 方法會抓取資料行資料的下一個資料列，否則會是 Null。 呼叫 Fetch 方法之前的 Execute 方法。
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. Fetch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992793"
---
# <a name="viewfetch-method"></a><span data-ttu-id="4b080-104">View. Fetch 方法</span><span class="sxs-lookup"><span data-stu-id="4b080-104">View.Fetch method</span></span>

<span data-ttu-id="4b080-105">如果結果集中有多個資料列，則 [**View**](view-object.md)物件的 Fetch 方法會 **抓取** 資料行資料的下一個資料列，否則會是 Null。</span><span class="sxs-lookup"><span data-stu-id="4b080-105">The **Fetch** method of the [**View**](view-object.md) object retrieves the next row of column data if more rows are available in the result set, otherwise it is Null.</span></span> <span data-ttu-id="4b080-106">呼叫 **Fetch** 方法之前的 [**Execute**](view-execute.md)方法。</span><span class="sxs-lookup"><span data-stu-id="4b080-106">Call the [**Execute**](view-execute.md) method before the **Fetch** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b080-107">語法</span><span class="sxs-lookup"><span data-stu-id="4b080-107">Syntax</span></span>


```JScript
View.Fetch()
```



## <a name="parameters"></a><span data-ttu-id="4b080-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b080-108">Parameters</span></span>

<span data-ttu-id="4b080-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4b080-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b080-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b080-110">Return value</span></span>

<span data-ttu-id="4b080-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4b080-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b080-112">備註</span><span class="sxs-lookup"><span data-stu-id="4b080-112">Remarks</span></span>

<span data-ttu-id="4b080-113">您應該使用相同的 [**記錄**](record-object.md) 物件來取出多個資料列中的資料，否則物件應移出範圍以外的方式釋出。</span><span class="sxs-lookup"><span data-stu-id="4b080-113">The same [**Record**](record-object.md) object should be used to retrieve the data in multiple rows, or else the object should be released by going out of scope.</span></span> <span data-ttu-id="4b080-114">您可以使用「如果 FetchRecord 為 Nothing」語法來測試結果集結尾的記錄。</span><span class="sxs-lookup"><span data-stu-id="4b080-114">The record can be tested for the end of the result set using the syntax "If FetchRecord Is Nothing".</span></span>

## <a name="requirements"></a><span data-ttu-id="4b080-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b080-115">Requirements</span></span>



| <span data-ttu-id="4b080-116">需求</span><span class="sxs-lookup"><span data-stu-id="4b080-116">Requirement</span></span> | <span data-ttu-id="4b080-117">值</span><span class="sxs-lookup"><span data-stu-id="4b080-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b080-118">版本</span><span class="sxs-lookup"><span data-stu-id="4b080-118">Version</span></span><br/> | <span data-ttu-id="4b080-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4b080-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4b080-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4b080-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4b080-121">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="4b080-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4b080-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4b080-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4b080-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b080-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4b080-124">IID</span><span class="sxs-lookup"><span data-stu-id="4b080-124">IID</span></span><br/>     | <span data-ttu-id="4b080-125">IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4b080-125">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




