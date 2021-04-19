---
description: 請注意，此介面已被取代。
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: 'IAMFilterData：:P arseFilterData 方法 (Fil \_ data .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976026"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="ef1ed-103">IAMFilterData：:P arseFilterData 方法</span><span class="sxs-lookup"><span data-stu-id="ef1ed-103">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="ef1ed-104">這個介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-104">This interface has been deprecated.</span></span> <span data-ttu-id="ef1ed-105">新的應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-105">New applications should not use it.</span></span>

 

<span data-ttu-id="ef1ed-106">`ParseFilterData`方法會解壓縮篩選的二進位登錄資料。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-106">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="ef1ed-107">應用程式通常不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-107">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="ef1ed-108">[**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)方法提供更方便的方式來存取篩選登錄資料。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-108">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1ed-109">語法</span><span class="sxs-lookup"><span data-stu-id="ef1ed-109">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="ef1ed-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef1ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1ed-111">*rgbFilterData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef1ed-111">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1ed-112">二進位登錄資料的指標。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-112">Pointer to the binary registry data.</span></span> <span data-ttu-id="ef1ed-113">您可以從篩選器的標記中抓取 "FilterData" 屬性來取得此資料。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-113">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="ef1ed-114">資料會儲存為位元組的 **SAFEARRAY** (vt \_ UI1 \| vt \_ 陣列) 。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-114">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="ef1ed-115">*cb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef1ed-115">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1ed-116">指定二進位資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-116">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ef1ed-117">*prgbRegFilter2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ef1ed-117">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1ed-118">接收已解壓縮資料指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-118">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="ef1ed-119">當方法傳回時，將這個指標轉換成 [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) 類型以存取篩選資料。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-119">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="ef1ed-120">呼叫端必須藉由呼叫 **CoTaskMemFree** 方法來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-120">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1ed-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef1ed-121">Return value</span></span>

<span data-ttu-id="ef1ed-122">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ef1ed-123">如果方法失敗，則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1ed-124">備註</span><span class="sxs-lookup"><span data-stu-id="ef1ed-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ef1ed-125">標頭 Fil \_ data .h 位於 Windows SDK 的對應工具 [範例](mapper-sample.md) 目錄中。</span><span class="sxs-lookup"><span data-stu-id="ef1ed-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef1ed-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef1ed-126">Requirements</span></span>



| <span data-ttu-id="ef1ed-127">需求</span><span class="sxs-lookup"><span data-stu-id="ef1ed-127">Requirement</span></span> | <span data-ttu-id="ef1ed-128">值</span><span class="sxs-lookup"><span data-stu-id="ef1ed-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1ed-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ef1ed-129">Header</span></span><br/> | <dl> <span data-ttu-id="ef1ed-130"><dt>Fil \_ 資料。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1ed-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="ef1ed-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1ed-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="ef1ed-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1ed-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ef1ed-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef1ed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1ed-134">**IAMFilterData 介面**</span><span class="sxs-lookup"><span data-stu-id="ef1ed-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




