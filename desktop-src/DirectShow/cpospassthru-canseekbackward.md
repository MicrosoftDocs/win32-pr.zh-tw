---
description: CanSeekBackward 方法會判斷資料流程是否可反向 seeked。 這個方法會實 IMediaPosition：： CanSeekBackward 方法。
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: 'CPosPassThru. CanSeekBackward 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990535"
---
# <a name="cpospassthrucanseekbackward-method"></a><span data-ttu-id="c39fe-104">CPosPassThru. CanSeekBackward 方法</span><span class="sxs-lookup"><span data-stu-id="c39fe-104">CPosPassThru.CanSeekBackward method</span></span>

<span data-ttu-id="c39fe-105">`CanSeekBackward`方法會判斷資料流程是否可以向後 seeked。</span><span class="sxs-lookup"><span data-stu-id="c39fe-105">The `CanSeekBackward` method determines whether the stream can be seeked backward.</span></span> <span data-ttu-id="c39fe-106">這個方法會實 [**IMediaPosition：： CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) 方法。</span><span class="sxs-lookup"><span data-stu-id="c39fe-106">This method implements the [**IMediaPosition::CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c39fe-107">語法</span><span class="sxs-lookup"><span data-stu-id="c39fe-107">Syntax</span></span>


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a><span data-ttu-id="c39fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="c39fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c39fe-109">*pCanSeekBackward*</span><span class="sxs-lookup"><span data-stu-id="c39fe-109">*pCanSeekBackward*</span></span> 
</dt> <dd>

<span data-ttu-id="c39fe-110">如果篩選準則可以向前搜尋，則為收到值 OATRUE 之變數的指標，否則為 OAFALSE。</span><span class="sxs-lookup"><span data-stu-id="c39fe-110">Pointer to a variable that receives the value OATRUE if the filter can seek backward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c39fe-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c39fe-111">Return value</span></span>

<span data-ttu-id="c39fe-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c39fe-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c39fe-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c39fe-113">Requirements</span></span>



| <span data-ttu-id="c39fe-114">需求</span><span class="sxs-lookup"><span data-stu-id="c39fe-114">Requirement</span></span> | <span data-ttu-id="c39fe-115">值</span><span class="sxs-lookup"><span data-stu-id="c39fe-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c39fe-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c39fe-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c39fe-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c39fe-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c39fe-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c39fe-118">Library</span></span><br/> | <dl> <span data-ttu-id="c39fe-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c39fe-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c39fe-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c39fe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c39fe-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="c39fe-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




