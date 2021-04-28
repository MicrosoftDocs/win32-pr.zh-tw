---
description: CSourceStream。 CSourceStream 函式-函數方法。
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: CSourceStream)  (Source .h 的函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085186"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="f176a-103">CSourceStream. CSourceStream 函數</span><span class="sxs-lookup"><span data-stu-id="f176a-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="f176a-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f176a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f176a-105">語法</span><span class="sxs-lookup"><span data-stu-id="f176a-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="f176a-106">參數</span><span class="sxs-lookup"><span data-stu-id="f176a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f176a-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="f176a-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="f176a-108">字串的指標，其中包含釘選的偵錯工具名稱。</span><span class="sxs-lookup"><span data-stu-id="f176a-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="f176a-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="f176a-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f176a-110">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="f176a-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="f176a-111">在建立物件之前，將值初始化為「 \_ 確定」。</span><span class="sxs-lookup"><span data-stu-id="f176a-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="f176a-112">只有在發生錯誤時，才會變更此值。</span><span class="sxs-lookup"><span data-stu-id="f176a-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="f176a-113">*Pms*</span><span class="sxs-lookup"><span data-stu-id="f176a-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="f176a-114">建立此釘選的 [**CSource**](csource.md) 篩選指標。</span><span class="sxs-lookup"><span data-stu-id="f176a-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="f176a-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="f176a-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f176a-116">包含釘選名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="f176a-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f176a-117">備註</span><span class="sxs-lookup"><span data-stu-id="f176a-117">Remarks</span></span>

<span data-ttu-id="f176a-118">*PObjectName* 參數中提供的字串僅供進行偵錯工具之用。</span><span class="sxs-lookup"><span data-stu-id="f176a-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="f176a-119">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="f176a-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="f176a-120">*PName* 參數中提供的字串是 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)方法所傳回的名稱。</span><span class="sxs-lookup"><span data-stu-id="f176a-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="f176a-121">`CSourceStream`此類別不會將此名稱用於 [**CSourceStream：： QueryId**](csourcestream-queryid.md)方法所傳回的 pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f176a-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="f176a-122">相反地， **QueryId** 會根據 pin 碼來計算 pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f176a-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="f176a-123"> (Pin 識別碼支援圖形持續性。</span><span class="sxs-lookup"><span data-stu-id="f176a-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="f176a-124">如需詳細資訊，請參閱 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)。 ) </span><span class="sxs-lookup"><span data-stu-id="f176a-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="f176a-125">此函式會藉由呼叫 [**CSource：： AddPin**](csource-addpin.md)，自動將釘選新增至擁有篩選準則。</span><span class="sxs-lookup"><span data-stu-id="f176a-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f176a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f176a-126">Requirements</span></span>



| <span data-ttu-id="f176a-127">需求</span><span class="sxs-lookup"><span data-stu-id="f176a-127">Requirement</span></span> | <span data-ttu-id="f176a-128">值</span><span class="sxs-lookup"><span data-stu-id="f176a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f176a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f176a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f176a-130"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="f176a-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f176a-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="f176a-131">Library</span></span><br/> | <dl> <span data-ttu-id="f176a-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f176a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f176a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f176a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f176a-134">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="f176a-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




