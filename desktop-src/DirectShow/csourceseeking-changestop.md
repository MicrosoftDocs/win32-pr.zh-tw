---
description: 當停止位置變更時，會呼叫 ChangeStop 方法。
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: 'CSourceSeeking. ChangeStop 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994055"
---
# <a name="csourceseekingchangestop-method"></a><span data-ttu-id="8fa8f-103">CSourceSeeking. ChangeStop 方法</span><span class="sxs-lookup"><span data-stu-id="8fa8f-103">CSourceSeeking.ChangeStop method</span></span>

<span data-ttu-id="8fa8f-104">`ChangeStop`當停止位置變更時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="8fa8f-104">The `ChangeStop` method is called when the stop position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa8f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fa8f-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a><span data-ttu-id="8fa8f-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fa8f-106">Parameters</span></span>

<span data-ttu-id="8fa8f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8fa8f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fa8f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fa8f-108">Return value</span></span>

<span data-ttu-id="8fa8f-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8fa8f-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fa8f-110">備註</span><span class="sxs-lookup"><span data-stu-id="8fa8f-110">Remarks</span></span>

<span data-ttu-id="8fa8f-111">如果停止位置變更， [**CSourceSeeking：： SetPositions**](csourceseeking-setpositions.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8fa8f-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the stop position changes.</span></span> <span data-ttu-id="8fa8f-112">這個方法是純虛擬的;衍生的類別必須加以執行。</span><span class="sxs-lookup"><span data-stu-id="8fa8f-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="8fa8f-113">下列範例顯示可能的實作為：</span><span class="sxs-lookup"><span data-stu-id="8fa8f-113">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="8fa8f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fa8f-114">Requirements</span></span>



| <span data-ttu-id="8fa8f-115">需求</span><span class="sxs-lookup"><span data-stu-id="8fa8f-115">Requirement</span></span> | <span data-ttu-id="8fa8f-116">值</span><span class="sxs-lookup"><span data-stu-id="8fa8f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa8f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8fa8f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8fa8f-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8fa8f-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8fa8f-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8fa8f-119">Library</span></span><br/> | <dl> <span data-ttu-id="8fa8f-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8fa8f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fa8f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fa8f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa8f-122">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="8fa8f-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




