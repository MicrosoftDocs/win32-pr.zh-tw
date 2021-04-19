---
description: GetConnected 方法會抓取連接至此釘選的 pin。
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: 'CBasePin. GetConnected 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995942"
---
# <a name="cbasepingetconnected-method"></a><span data-ttu-id="13587-103">CBasePin. GetConnected 方法</span><span class="sxs-lookup"><span data-stu-id="13587-103">CBasePin.GetConnected method</span></span>

<span data-ttu-id="13587-104">方法會抓取 `GetConnected` 連接至此 pin 的 pin。</span><span class="sxs-lookup"><span data-stu-id="13587-104">The `GetConnected` method retrieves the pin connected to this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="13587-105">語法</span><span class="sxs-lookup"><span data-stu-id="13587-105">Syntax</span></span>


```C++
IPin* GetConnected();
```



## <a name="parameters"></a><span data-ttu-id="13587-106">參數</span><span class="sxs-lookup"><span data-stu-id="13587-106">Parameters</span></span>

<span data-ttu-id="13587-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="13587-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13587-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="13587-108">Return value</span></span>

<span data-ttu-id="13587-109">傳回其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="13587-109">Returns a pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="13587-110">備註</span><span class="sxs-lookup"><span data-stu-id="13587-110">Remarks</span></span>

<span data-ttu-id="13587-111">如果未連接 pin，這個方法會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="13587-111">If the pin is not connected, this method returns **NULL**.</span></span> <span data-ttu-id="13587-112">呼叫 [**CBasePin：： IsConnected**](cbasepin-isconnected.md) 方法來判斷釘選是否已連接。</span><span class="sxs-lookup"><span data-stu-id="13587-112">Call the [**CBasePin::IsConnected**](cbasepin-isconnected.md) method to determine whether the pin is connected.</span></span>

<span data-ttu-id="13587-113">方法不會在 **IPin** 介面上呼叫 **AddRef** ，因此呼叫端不應該釋放介面。</span><span class="sxs-lookup"><span data-stu-id="13587-113">The method does not call **AddRef** on the **IPin** interface, so the caller should not release the interface.</span></span>

## <a name="examples"></a><span data-ttu-id="13587-114">範例</span><span class="sxs-lookup"><span data-stu-id="13587-114">Examples</span></span>

<span data-ttu-id="13587-115">因為傳回的指標上的參考計數不會遞增，所以您可以將方法呼叫串連在一起：</span><span class="sxs-lookup"><span data-stu-id="13587-115">Because the reference count is not incremented on the returned pointer, you can chain method calls together:</span></span>


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



<span data-ttu-id="13587-116">這種編碼模式非常方便;但如範例所示，當 pin 未連線時，您必須小心不要對 **Null** 指標進行取值。</span><span class="sxs-lookup"><span data-stu-id="13587-116">This coding pattern is very convenient; but as the example shows, you must be careful not to dereference a **NULL** pointer when the pin is unconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="13587-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="13587-117">Requirements</span></span>



| <span data-ttu-id="13587-118">需求</span><span class="sxs-lookup"><span data-stu-id="13587-118">Requirement</span></span> | <span data-ttu-id="13587-119">值</span><span class="sxs-lookup"><span data-stu-id="13587-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13587-120">標頭</span><span class="sxs-lookup"><span data-stu-id="13587-120">Header</span></span><br/>  | <dl> <span data-ttu-id="13587-121"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="13587-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="13587-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="13587-122">Library</span></span><br/> | <dl> <span data-ttu-id="13587-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="13587-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13587-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13587-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13587-125">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="13587-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




