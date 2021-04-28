---
description: CTransformOutputPin. CompleteConnect 方法-CompleteConnect 方法會完成與另一個 pin 的連接。
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: 'CTransformOutputPin. CompleteConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094916"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="3bbea-103">CTransformOutputPin. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="3bbea-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="3bbea-104">`CompleteConnect`方法會完成與另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="3bbea-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbea-105">語法</span><span class="sxs-lookup"><span data-stu-id="3bbea-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="3bbea-106">參數</span><span class="sxs-lookup"><span data-stu-id="3bbea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbea-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="3bbea-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="3bbea-108">指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3bbea-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bbea-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bbea-109">Return value</span></span>

<span data-ttu-id="3bbea-110">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3bbea-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bbea-111">備註</span><span class="sxs-lookup"><span data-stu-id="3bbea-111">Remarks</span></span>

<span data-ttu-id="3bbea-112">這個方法會覆寫 [**CBaseOutputPin：： CompleteConnect**](cbaseoutputpin-completeconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3bbea-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="3bbea-113">它會呼叫篩選器的 [**CTransformFilter：： CompleteConnect**](ctransformfilter-completeconnect.md) 方法，它會 \_ 在基類中傳回 s OK。</span><span class="sxs-lookup"><span data-stu-id="3bbea-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="3bbea-114">衍生類別可以覆寫 **CTransformFilter：： CompleteConnect** 方法，以執行額外的檢查。</span><span class="sxs-lookup"><span data-stu-id="3bbea-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bbea-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bbea-115">Requirements</span></span>



| <span data-ttu-id="3bbea-116">需求</span><span class="sxs-lookup"><span data-stu-id="3bbea-116">Requirement</span></span> | <span data-ttu-id="3bbea-117">值</span><span class="sxs-lookup"><span data-stu-id="3bbea-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbea-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3bbea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3bbea-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3bbea-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3bbea-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="3bbea-120">Library</span></span><br/> | <dl> <span data-ttu-id="3bbea-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3bbea-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




