---
description: '>advanced.field.settype 方法會指定主要型別。'
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: 'CMediaType. >advanced.field.settype 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997790"
---
# <a name="cmediatypesettype-method"></a><span data-ttu-id="76fa6-103">CMediaType. >advanced.field.settype 方法</span><span class="sxs-lookup"><span data-stu-id="76fa6-103">CMediaType.SetType method</span></span>

<span data-ttu-id="76fa6-104">`SetType`方法會指定主要型別。</span><span class="sxs-lookup"><span data-stu-id="76fa6-104">The `SetType` method specifies the major type.</span></span>

## <a name="syntax"></a><span data-ttu-id="76fa6-105">語法</span><span class="sxs-lookup"><span data-stu-id="76fa6-105">Syntax</span></span>


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a><span data-ttu-id="76fa6-106">參數</span><span class="sxs-lookup"><span data-stu-id="76fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76fa6-107">*ptype*</span><span class="sxs-lookup"><span data-stu-id="76fa6-107">*ptype*</span></span> 
</dt> <dd>

<span data-ttu-id="76fa6-108">指定主要類型之 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="76fa6-108">Pointer to a **GUID** that specifies the major type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76fa6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="76fa6-109">Return value</span></span>

<span data-ttu-id="76fa6-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="76fa6-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76fa6-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="76fa6-111">Requirements</span></span>



| <span data-ttu-id="76fa6-112">需求</span><span class="sxs-lookup"><span data-stu-id="76fa6-112">Requirement</span></span> | <span data-ttu-id="76fa6-113">值</span><span class="sxs-lookup"><span data-stu-id="76fa6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76fa6-114">標頭</span><span class="sxs-lookup"><span data-stu-id="76fa6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="76fa6-115"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="76fa6-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="76fa6-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="76fa6-116">Library</span></span><br/> | <dl> <span data-ttu-id="76fa6-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="76fa6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76fa6-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76fa6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fa6-119">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="76fa6-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




