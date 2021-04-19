---
description: 瞭解 CMediaPosition. CMediaPosition (Ctlutil .h) 的方法。 這個方法會使用 ' pName '、' pUnk ' 和 ' phr ' 參數。
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: 'CMediaPosition. CMediaPosition (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106982246"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a><span data-ttu-id="425b1-104">CMediaPosition. CMediaPosition (Ctlutil .h) -pName、pUnk、phr 參數</span><span class="sxs-lookup"><span data-stu-id="425b1-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk, phr parameters</span></span>

<span data-ttu-id="425b1-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="425b1-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="425b1-106">語法</span><span class="sxs-lookup"><span data-stu-id="425b1-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="425b1-107">參數</span><span class="sxs-lookup"><span data-stu-id="425b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="425b1-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="425b1-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="425b1-109">物件名稱的指標，用於偵測用途。</span><span class="sxs-lookup"><span data-stu-id="425b1-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="425b1-110">在靜態記憶體中配置此參數。</span><span class="sxs-lookup"><span data-stu-id="425b1-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="425b1-111">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="425b1-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="425b1-112">這個物件之擁有者的指標，如果物件不是匯總，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="425b1-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> <dt>

<span data-ttu-id="425b1-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="425b1-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="425b1-114">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="425b1-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="425b1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="425b1-115">Requirements</span></span>

| <span data-ttu-id="425b1-116">需求</span><span class="sxs-lookup"><span data-stu-id="425b1-116">Requirement</span></span> | <span data-ttu-id="425b1-117">值</span><span class="sxs-lookup"><span data-stu-id="425b1-117">Value</span></span> |
|-|-|
| <span data-ttu-id="425b1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="425b1-118">Header</span></span> | <span data-ttu-id="425b1-119">Ctlutil (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="425b1-119">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="425b1-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="425b1-120">Library</span></span>| <span data-ttu-id="425b1-121"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="425b1-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="425b1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="425b1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425b1-123">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="425b1-123">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




