---
description: CBaseControlVideo。 CBaseControlVideo 函式-函數方法。
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: 'CBaseControlVideo. CBaseControlVideo (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096346"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="563e5-103">CBaseControlVideo. CBaseControlVideo 函數</span><span class="sxs-lookup"><span data-stu-id="563e5-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="563e5-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="563e5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="563e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="563e5-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="563e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="563e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="563e5-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="563e5-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="563e5-108">擁有媒體篩選物件的指標。</span><span class="sxs-lookup"><span data-stu-id="563e5-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="563e5-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="563e5-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="563e5-110">要用於鎖定的重要區段指標。</span><span class="sxs-lookup"><span data-stu-id="563e5-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="563e5-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="563e5-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="563e5-112">物件描述的指標。</span><span class="sxs-lookup"><span data-stu-id="563e5-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="563e5-113">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="563e5-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="563e5-114">如果物件是匯總的一部分，則為控制 **IUnknown** 介面的指標;否則，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="563e5-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="563e5-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="563e5-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="563e5-116">變數的指標，此變數會接收 HRESULT 值，指出函式方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="563e5-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="563e5-117">備註</span><span class="sxs-lookup"><span data-stu-id="563e5-117">Remarks</span></span>

<span data-ttu-id="563e5-118">物件會實 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 控制項介面。</span><span class="sxs-lookup"><span data-stu-id="563e5-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="563e5-119">[**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)中這個類別所執行的所有介面方法都需要正確連接篩選。</span><span class="sxs-lookup"><span data-stu-id="563e5-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="563e5-120">基於這個理由，類別會傳遞給與其進行同步處理的 pin。</span><span class="sxs-lookup"><span data-stu-id="563e5-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="563e5-121">每當呼叫介面方法時，物件就會判斷該釘選仍連接。</span><span class="sxs-lookup"><span data-stu-id="563e5-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="563e5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="563e5-122">Requirements</span></span>



| <span data-ttu-id="563e5-123">需求</span><span class="sxs-lookup"><span data-stu-id="563e5-123">Requirement</span></span> | <span data-ttu-id="563e5-124">值</span><span class="sxs-lookup"><span data-stu-id="563e5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="563e5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="563e5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="563e5-126"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="563e5-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="563e5-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="563e5-127">Library</span></span><br/> | <dl> <span data-ttu-id="563e5-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="563e5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="563e5-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="563e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563e5-130">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="563e5-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




