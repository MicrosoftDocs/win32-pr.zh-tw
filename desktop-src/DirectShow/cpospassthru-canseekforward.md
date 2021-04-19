---
description: CanSeekForward 方法會判斷是否可以向前 seeked 資料流程。 這個方法會實 IMediaPosition：： CanSeekForward 方法。
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: 'CPosPassThru. CanSeekForward 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994352"
---
# <a name="cpospassthrucanseekforward-method"></a><span data-ttu-id="d213b-104">CPosPassThru. CanSeekForward 方法</span><span class="sxs-lookup"><span data-stu-id="d213b-104">CPosPassThru.CanSeekForward method</span></span>

<span data-ttu-id="d213b-105">`CanSeekForward`方法會判斷資料流程是否可以向前 seeked。</span><span class="sxs-lookup"><span data-stu-id="d213b-105">The `CanSeekForward` method determines whether the stream can be seeked forward.</span></span> <span data-ttu-id="d213b-106">這個方法會實 [**IMediaPosition：： CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) 方法。</span><span class="sxs-lookup"><span data-stu-id="d213b-106">This method implements the [**IMediaPosition::CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d213b-107">語法</span><span class="sxs-lookup"><span data-stu-id="d213b-107">Syntax</span></span>


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a><span data-ttu-id="d213b-108">參數</span><span class="sxs-lookup"><span data-stu-id="d213b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d213b-109">*pCanSeekForward*</span><span class="sxs-lookup"><span data-stu-id="d213b-109">*pCanSeekForward*</span></span> 
</dt> <dd>

<span data-ttu-id="d213b-110">如果篩選準則可以向前搜尋，則為收到值 OATRUE 之變數的指標，否則為 OAFALSE。</span><span class="sxs-lookup"><span data-stu-id="d213b-110">Pointer to a variable that receives the value OATRUE if the filter can seek forward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d213b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d213b-111">Return value</span></span>

<span data-ttu-id="d213b-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d213b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d213b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d213b-113">Requirements</span></span>



| <span data-ttu-id="d213b-114">需求</span><span class="sxs-lookup"><span data-stu-id="d213b-114">Requirement</span></span> | <span data-ttu-id="d213b-115">值</span><span class="sxs-lookup"><span data-stu-id="d213b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d213b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="d213b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d213b-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d213b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d213b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="d213b-118">Library</span></span><br/> | <dl> <span data-ttu-id="d213b-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d213b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d213b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d213b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d213b-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="d213b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




