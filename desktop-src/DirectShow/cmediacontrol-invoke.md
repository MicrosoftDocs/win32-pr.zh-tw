---
description: 提供物件所公開的屬性和方法的存取權。
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: 'CMediaControl： Invoke 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b9a29d163180ffc609ca44f2bbbfb2870c5faef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993366"
---
# <a name="cmediacontrolinvoke-method"></a><span data-ttu-id="b87ee-103">CMediaControl 方法</span><span class="sxs-lookup"><span data-stu-id="b87ee-103">CMediaControl.Invoke method</span></span>

<span data-ttu-id="b87ee-104">提供物件所公開的屬性和方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="b87ee-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b87ee-105">語法</span><span class="sxs-lookup"><span data-stu-id="b87ee-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="b87ee-106">參數</span><span class="sxs-lookup"><span data-stu-id="b87ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b87ee-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="b87ee-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-108">成員的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b87ee-108">Identifier of the member.</span></span> <span data-ttu-id="b87ee-109">使用 [**CMediaControl：： GetIDsOfNames**](cmediacontrol-getidsofnames.md) 或物件的檔以取得分派識別碼。</span><span class="sxs-lookup"><span data-stu-id="b87ee-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b87ee-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="b87ee-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-111">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="b87ee-111">Reserved for future use.</span></span> <span data-ttu-id="b87ee-112">必須是 IID \_ Null。</span><span class="sxs-lookup"><span data-stu-id="b87ee-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="b87ee-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="b87ee-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-114">要在其中解讀引數的地區設定內容。</span><span class="sxs-lookup"><span data-stu-id="b87ee-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="b87ee-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="b87ee-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-116">描述呼叫內容的旗標 `CMediaControl::Invoke` 。</span><span class="sxs-lookup"><span data-stu-id="b87ee-116">Flags describing the context of the `CMediaControl::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="b87ee-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="b87ee-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-118">結構的指標，此結構包含引數陣列、具名引數的引數分派識別碼陣列，以及陣列中專案數目的計數。</span><span class="sxs-lookup"><span data-stu-id="b87ee-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="b87ee-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="b87ee-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-120">要儲存結果之位置的指標，如果呼叫端預期沒有任何結果，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b87ee-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="b87ee-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="b87ee-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-122">包含例外狀況資訊之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b87ee-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="b87ee-123">*>puargerr*</span><span class="sxs-lookup"><span data-stu-id="b87ee-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="b87ee-124">在 **DISPPARAMS** 結構的 **>rgvarg** 陣列中，第一個引數索引的指標，其發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b87ee-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="b87ee-125">如需 **DISPPARAMS** 的詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="b87ee-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b87ee-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="b87ee-126">Return value</span></span>

<span data-ttu-id="b87ee-127">\_ \_ 如果 *RIID* 不是 IID Null，則會傳回 \_ 空的 E UNKNOWNINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="b87ee-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="b87ee-128">如果呼叫失敗，則從 [**CMediaControl：： GetTypeInfo**](cmediacontrol-gettypeinfo.md) 傳回其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b87ee-128">Returns one of the error codes from [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="b87ee-129">否則，會從呼叫 **IDispatch：： Invoke** 傳回 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="b87ee-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b87ee-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b87ee-130">Requirements</span></span>



| <span data-ttu-id="b87ee-131">需求</span><span class="sxs-lookup"><span data-stu-id="b87ee-131">Requirement</span></span> | <span data-ttu-id="b87ee-132">值</span><span class="sxs-lookup"><span data-stu-id="b87ee-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b87ee-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b87ee-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b87ee-134"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b87ee-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b87ee-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="b87ee-135">Library</span></span><br/> | <dl> <span data-ttu-id="b87ee-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b87ee-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b87ee-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b87ee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b87ee-138">**CMediaControl 類別**</span><span class="sxs-lookup"><span data-stu-id="b87ee-138">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




