---
description: Session 物件的 ComponentRequestState 屬性會取得或要求元件資料表中資料列的動作狀態變更。
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: ComponentRequestState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983073"
---
# <a name="sessioncomponentrequeststate-property"></a><span data-ttu-id="e9523-103">ComponentRequestState 屬性</span><span class="sxs-lookup"><span data-stu-id="e9523-103">Session.ComponentRequestState property</span></span>

<span data-ttu-id="e9523-104">[**Session**](session-object.md)物件的 **ComponentRequestState** 屬性會取得或要求 [元件資料表](component-table.md)中資料列的動作狀態變更。</span><span class="sxs-lookup"><span data-stu-id="e9523-104">The **ComponentRequestState** property of the [**Session**](session-object.md) object obtains or requests a change in the Action state of a row in the [Component table](component-table.md).</span></span>

<span data-ttu-id="e9523-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e9523-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9523-106">語法</span><span class="sxs-lookup"><span data-stu-id="e9523-106">Syntax</span></span>


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a><span data-ttu-id="e9523-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="e9523-107">Property value</span></span>

<span data-ttu-id="e9523-108">元件專案的必要字串名稱、元件資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e9523-108">Required string name of the component item, primary key of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9523-109">備註</span><span class="sxs-lookup"><span data-stu-id="e9523-109">Remarks</span></span>



| <span data-ttu-id="e9523-110">選取狀態</span><span class="sxs-lookup"><span data-stu-id="e9523-110">Selection state</span></span>        | <span data-ttu-id="e9523-111">值</span><span class="sxs-lookup"><span data-stu-id="e9523-111">Value</span></span> | <span data-ttu-id="e9523-112">描述</span><span class="sxs-lookup"><span data-stu-id="e9523-112">Description</span></span>                                                    |
|------------------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="e9523-113">Null</span><span class="sxs-lookup"><span data-stu-id="e9523-113">Null</span></span>                   | <span data-ttu-id="e9523-114">Null</span><span class="sxs-lookup"><span data-stu-id="e9523-114">Null</span></span>  | <span data-ttu-id="e9523-115">要求不對此專案採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="e9523-115">Requests that no action be taken for this item.</span></span>                |
| <span data-ttu-id="e9523-116">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="e9523-116">msiInstallStateAbsent</span></span>  | <span data-ttu-id="e9523-117">2</span><span class="sxs-lookup"><span data-stu-id="e9523-117">2</span></span>     | <span data-ttu-id="e9523-118">要移除的專案。</span><span class="sxs-lookup"><span data-stu-id="e9523-118">Item is to be removed.</span></span>                                         |
| <span data-ttu-id="e9523-119">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="e9523-119">msiInstallStateLocal</span></span>   | <span data-ttu-id="e9523-120">3</span><span class="sxs-lookup"><span data-stu-id="e9523-120">3</span></span>     | <span data-ttu-id="e9523-121">專案要安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="e9523-121">Item is to be installed locally.</span></span>                               |
| <span data-ttu-id="e9523-122">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="e9523-122">msiInstallStateSource</span></span>  | <span data-ttu-id="e9523-123">4</span><span class="sxs-lookup"><span data-stu-id="e9523-123">4</span></span>     | <span data-ttu-id="e9523-124">專案會從來源媒體安裝和執行。</span><span class="sxs-lookup"><span data-stu-id="e9523-124">Item is to be installed and run from the source media.</span></span>         |
| <span data-ttu-id="e9523-125">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="e9523-125">msiInstallStateDefault</span></span> | <span data-ttu-id="e9523-126">5</span><span class="sxs-lookup"><span data-stu-id="e9523-126">5</span></span>     | <span data-ttu-id="e9523-127">如果已安裝，則會以相同的狀態重新安裝專案。</span><span class="sxs-lookup"><span data-stu-id="e9523-127">If installed, the item is to be reinstalled in the same state.</span></span> |



 

<span data-ttu-id="e9523-128">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="e9523-128">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9523-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9523-129">Requirements</span></span>



| <span data-ttu-id="e9523-130">需求</span><span class="sxs-lookup"><span data-stu-id="e9523-130">Requirement</span></span> | <span data-ttu-id="e9523-131">值</span><span class="sxs-lookup"><span data-stu-id="e9523-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9523-132">版本</span><span class="sxs-lookup"><span data-stu-id="e9523-132">Version</span></span><br/> | <span data-ttu-id="e9523-133">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e9523-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e9523-134">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e9523-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e9523-135">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e9523-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e9523-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e9523-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="e9523-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9523-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e9523-138">IID</span><span class="sxs-lookup"><span data-stu-id="e9523-138">IID</span></span><br/>     | <span data-ttu-id="e9523-139">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e9523-139">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




