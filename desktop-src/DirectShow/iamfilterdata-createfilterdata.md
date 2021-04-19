---
description: 請注意，此介面已被取代。
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'IAMFilterData：： CreateFilterData 方法 (Fil \_ data .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982575"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="7b8a3-103">IAMFilterData：： CreateFilterData 方法</span><span class="sxs-lookup"><span data-stu-id="7b8a3-103">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="7b8a3-104">這個介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-104">This interface has been deprecated.</span></span> <span data-ttu-id="7b8a3-105">新的應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-105">New applications should not use it.</span></span>

 

<span data-ttu-id="7b8a3-106">`CreateFilterData`方法會建立篩選的二進位登錄資料。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-106">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="7b8a3-107">您可以 \_ 在篩選器的 CLSID 機碼底下，將此資料寫入登錄中作為名為 FilterData 的 REG 二進位子機碼。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-107">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="7b8a3-108">應用程式通常不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="7b8a3-109">[**IFilterMapper2：： RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter)方法會自動建立二進位資料，並將它新增至登錄中的正確位置。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-109">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="7b8a3-110">如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-110">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8a3-111">語法</span><span class="sxs-lookup"><span data-stu-id="7b8a3-111">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="7b8a3-112">參數</span><span class="sxs-lookup"><span data-stu-id="7b8a3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b8a3-113">*prf2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b8a3-113">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b8a3-114">包含篩選資訊之 [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-114">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="7b8a3-115">*prgbFilterData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7b8a3-115">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b8a3-116">接收二進位資料指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-116">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="7b8a3-117">方法會配置資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-117">The method allocates the memory for the data.</span></span> <span data-ttu-id="7b8a3-118">呼叫端必須藉由呼叫 **CoTaskMemFree** 方法來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-118">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="7b8a3-119">*pcb* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7b8a3-119">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b8a3-120">變數的指標，此變數會接收二進位資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-120">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b8a3-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b8a3-121">Return value</span></span>

<span data-ttu-id="7b8a3-122">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="7b8a3-123">如果方法失敗，則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b8a3-124">備註</span><span class="sxs-lookup"><span data-stu-id="7b8a3-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b8a3-125">標頭 Fil \_ data .h 位於 Windows SDK 的對應工具 [範例](mapper-sample.md) 目錄中。</span><span class="sxs-lookup"><span data-stu-id="7b8a3-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b8a3-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b8a3-126">Requirements</span></span>



| <span data-ttu-id="7b8a3-127">需求</span><span class="sxs-lookup"><span data-stu-id="7b8a3-127">Requirement</span></span> | <span data-ttu-id="7b8a3-128">值</span><span class="sxs-lookup"><span data-stu-id="7b8a3-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8a3-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7b8a3-129">Header</span></span><br/> | <dl> <span data-ttu-id="7b8a3-130"><dt>Fil \_ 資料。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b8a3-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="7b8a3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7b8a3-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="7b8a3-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b8a3-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7b8a3-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b8a3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b8a3-134">**IAMFilterData 介面**</span><span class="sxs-lookup"><span data-stu-id="7b8a3-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




