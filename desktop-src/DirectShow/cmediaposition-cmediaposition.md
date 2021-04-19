---
description: 瞭解 CMediaPosition. CMediaPosition (Ctlutil .h) 的方法。 這個方法會使用 ' pName ' 和 ' pUnk ' 參數。
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: CMediaPosition. CMediaPosition (Ctlutil .h) -pName，pUnk 參數
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "107001488"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a><span data-ttu-id="c0d15-104">CMediaPosition. CMediaPosition (Ctlutil .h) -pName，pUnk 參數</span><span class="sxs-lookup"><span data-stu-id="c0d15-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk parameters</span></span>

<span data-ttu-id="c0d15-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="c0d15-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d15-106">語法</span><span class="sxs-lookup"><span data-stu-id="c0d15-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="c0d15-107">參數</span><span class="sxs-lookup"><span data-stu-id="c0d15-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0d15-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="c0d15-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c0d15-109">物件名稱的指標，用於偵測用途。</span><span class="sxs-lookup"><span data-stu-id="c0d15-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="c0d15-110">在靜態記憶體中配置此參數。</span><span class="sxs-lookup"><span data-stu-id="c0d15-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="c0d15-111">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="c0d15-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c0d15-112">這個物件之擁有者的指標，如果物件不是匯總，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c0d15-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0d15-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0d15-113">Requirements</span></span>

| <span data-ttu-id="c0d15-114">需求</span><span class="sxs-lookup"><span data-stu-id="c0d15-114">Requirement</span></span> | <span data-ttu-id="c0d15-115">值</span><span class="sxs-lookup"><span data-stu-id="c0d15-115">Value</span></span> |
|-|-|
| <span data-ttu-id="c0d15-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c0d15-116">Header</span></span> | <span data-ttu-id="c0d15-117">Ctlutil (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="c0d15-117">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="c0d15-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c0d15-118">Library</span></span>| <span data-ttu-id="c0d15-119"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="c0d15-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c0d15-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0d15-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d15-121">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="c0d15-121">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




