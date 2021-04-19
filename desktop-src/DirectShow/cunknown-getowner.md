---
description: GetOwner 方法會抓取擁有元件的 IUnknown 介面指標。 針對匯總的元件，擁有者是外部元件。 否則，元件擁有本身。
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: 'CUnknown. GetOwner 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993221"
---
# <a name="cunknowngetowner-method"></a><span data-ttu-id="0e317-105">CUnknown. GetOwner 方法</span><span class="sxs-lookup"><span data-stu-id="0e317-105">CUnknown.GetOwner method</span></span>

<span data-ttu-id="0e317-106">方法會抓取 `GetOwner` 擁有元件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0e317-106">The `GetOwner` method retrieves a pointer to the **IUnknown** interface of the owning component.</span></span> <span data-ttu-id="0e317-107">針對匯總的元件，擁有者是外部元件。</span><span class="sxs-lookup"><span data-stu-id="0e317-107">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="0e317-108">否則，元件擁有本身。</span><span class="sxs-lookup"><span data-stu-id="0e317-108">Otherwise, the component owns itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e317-109">語法</span><span class="sxs-lookup"><span data-stu-id="0e317-109">Syntax</span></span>


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a><span data-ttu-id="0e317-110">參數</span><span class="sxs-lookup"><span data-stu-id="0e317-110">Parameters</span></span>

<span data-ttu-id="0e317-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0e317-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e317-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e317-112">Return value</span></span>

<span data-ttu-id="0e317-113">傳回控制 **IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0e317-113">Returns a pointer to the controlling **IUnknown** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e317-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e317-114">Requirements</span></span>



| <span data-ttu-id="0e317-115">需求</span><span class="sxs-lookup"><span data-stu-id="0e317-115">Requirement</span></span> | <span data-ttu-id="0e317-116">值</span><span class="sxs-lookup"><span data-stu-id="0e317-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e317-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0e317-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0e317-118"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0e317-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e317-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e317-119">Library</span></span><br/> | <dl> <span data-ttu-id="0e317-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0e317-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




