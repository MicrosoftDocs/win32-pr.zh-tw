---
description: 將單一成員函式和一組選擇性的參數對應至一組對應的整數分派識別碼 (Dispid) ，可在後續呼叫 CMediaControl：： Invoke 成員函式時使用。
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: 'CMediaControl. GetIDsOfNames 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f906db9540f0429e1e7831284e55edf8c29b6a03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000813"
---
# <a name="cmediacontrolgetidsofnames-method"></a><span data-ttu-id="71ef2-103">CMediaControl. GetIDsOfNames 方法</span><span class="sxs-lookup"><span data-stu-id="71ef2-103">CMediaControl.GetIDsOfNames method</span></span>

<span data-ttu-id="71ef2-104">將單一成員函式和一組選擇性的參數對應至一組對應的整數分派識別碼 (Dispid) ，可在後續呼叫 [**CMediaControl：： Invoke**](cmediacontrol-invoke.md) 成員函式時使用。</span><span class="sxs-lookup"><span data-stu-id="71ef2-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used upon subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ef2-105">語法</span><span class="sxs-lookup"><span data-stu-id="71ef2-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="71ef2-106">參數</span><span class="sxs-lookup"><span data-stu-id="71ef2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ef2-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="71ef2-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="71ef2-108">參考識別碼。</span><span class="sxs-lookup"><span data-stu-id="71ef2-108">Reference identifier.</span></span> <span data-ttu-id="71ef2-109">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="71ef2-109">Reserved for future use.</span></span> <span data-ttu-id="71ef2-110">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="71ef2-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="71ef2-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="71ef2-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="71ef2-112">要對應之名稱陣列的指標位址。</span><span class="sxs-lookup"><span data-stu-id="71ef2-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="71ef2-113">*Cname*</span><span class="sxs-lookup"><span data-stu-id="71ef2-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="71ef2-114">要對應的名稱計數。</span><span class="sxs-lookup"><span data-stu-id="71ef2-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="71ef2-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="71ef2-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="71ef2-116">要在其中解讀名稱的地區設定內容。</span><span class="sxs-lookup"><span data-stu-id="71ef2-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="71ef2-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="71ef2-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="71ef2-118">呼叫端配置陣列的指標，其中的每個專案都包含對應至 *rgszNames* 陣列中傳遞之其中一個名稱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71ef2-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="71ef2-119">第一個元素代表成員名稱;後續的元素代表每個成員的參數。</span><span class="sxs-lookup"><span data-stu-id="71ef2-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ef2-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="71ef2-120">Return value</span></span>

<span data-ttu-id="71ef2-121">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="71ef2-121">Returns one of the following values.</span></span>



| <span data-ttu-id="71ef2-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="71ef2-122">Return code</span></span>                                                                                            | <span data-ttu-id="71ef2-123">Description</span><span class="sxs-lookup"><span data-stu-id="71ef2-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71ef2-124"><dt>**以 \_ 電子 \_ 不明 \_ CLSID**</dt></span><span class="sxs-lookup"><span data-stu-id="71ef2-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="71ef2-125">無法辨識 CLSID。</span><span class="sxs-lookup"><span data-stu-id="71ef2-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="71ef2-126"><dt>**將 \_ 電子 \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="71ef2-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="71ef2-127">一或多個名稱未知。</span><span class="sxs-lookup"><span data-stu-id="71ef2-127">One or more of the names were not known.</span></span> <span data-ttu-id="71ef2-128">傳回的 Dispid 包含 \_ 每個對應至未知名稱之專案的 dispid 未知。</span><span class="sxs-lookup"><span data-stu-id="71ef2-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="71ef2-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="71ef2-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="71ef2-130">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="71ef2-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="71ef2-131"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="71ef2-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="71ef2-132">成功。</span><span class="sxs-lookup"><span data-stu-id="71ef2-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="71ef2-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="71ef2-133">Requirements</span></span>



| <span data-ttu-id="71ef2-134">需求</span><span class="sxs-lookup"><span data-stu-id="71ef2-134">Requirement</span></span> | <span data-ttu-id="71ef2-135">值</span><span class="sxs-lookup"><span data-stu-id="71ef2-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ef2-136">標頭</span><span class="sxs-lookup"><span data-stu-id="71ef2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="71ef2-137"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="71ef2-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71ef2-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="71ef2-138">Library</span></span><br/> | <dl> <span data-ttu-id="71ef2-139"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="71ef2-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ef2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71ef2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ef2-141">**CMediaControl 類別**</span><span class="sxs-lookup"><span data-stu-id="71ef2-141">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




