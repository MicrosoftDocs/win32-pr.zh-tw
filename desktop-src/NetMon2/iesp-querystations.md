---
description: QueryStations 方法會提供目前使用網路監視器來捕捉網路資料的所有電腦清單。
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: 'IESP：： QueryStations 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5287f472b2a0641eb29e4f1b37b6fe4e089dfa86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991986"
---
# <a name="iespquerystations-method"></a><span data-ttu-id="eb9ad-103">IESP：： QueryStations 方法</span><span class="sxs-lookup"><span data-stu-id="eb9ad-103">IESP::QueryStations method</span></span>

<span data-ttu-id="eb9ad-104">**QueryStations** 方法會提供目前使用網路監視器來捕捉網路資料的所有電腦清單。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-104">The **QueryStations** method provides a list of all computers that currently use Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb9ad-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="eb9ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb9ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9ad-107">*lpQueryTable* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="eb9ad-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9ad-108">指向 [[工作]](querytable.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="eb9ad-109">在輸入時，此結構必須包含您想要網路監視器傳回的電腦數目上限，以及 [STATIONQUERY](stationquery.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="eb9ad-110">在輸出時，此結構會傳回每一部電腦的捕獲資料和 [STATIONQUERY](stationquery.md) 結構的電腦數目。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="eb9ad-111">請注意，此總計可能包括使用早2.0 版的網路監視器版本的電腦。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-111">Note that this total may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9ad-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb9ad-112">Return value</span></span>

<span data-ttu-id="eb9ad-113">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="eb9ad-114">如果此方法不成功，則傳回值會是下列錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="eb9ad-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="eb9ad-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eb9ad-115">Return code</span></span>                                                                                           | <span data-ttu-id="eb9ad-116">Description</span><span class="sxs-lookup"><span data-stu-id="eb9ad-116">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb9ad-117"><dt>**NMERR \_ \_ 記憶體不足 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb9ad-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="eb9ad-118">無法使用處理此查詢所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-118">The memory needed to process this query was unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb9ad-119">備註</span><span class="sxs-lookup"><span data-stu-id="eb9ad-119">Remarks</span></span>

<span data-ttu-id="eb9ad-120">呼叫 [CreateNPPInterface](createnppinterface.md) 方法之後，隨時都可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-120">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="eb9ad-121">呼叫這個方法是同步呼叫，這可能需要幾秒鐘的時間才能完成，因為網路監視器等候遠端電腦回應查詢。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="eb9ad-122">只有本機子網上的電腦可以進行查詢。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="eb9ad-123">您必須負責為 [資料表結構配置](querytable.md) 記憶體，並在不再需要資料表之後釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="eb9ad-124">這項需求包括用於查看 [STATIONQUERY](stationquery.md) 陣列所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="eb9ad-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9ad-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb9ad-125">Requirements</span></span>



| <span data-ttu-id="eb9ad-126">需求</span><span class="sxs-lookup"><span data-stu-id="eb9ad-126">Requirement</span></span> | <span data-ttu-id="eb9ad-127">值</span><span class="sxs-lookup"><span data-stu-id="eb9ad-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9ad-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb9ad-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9ad-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb9ad-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="eb9ad-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb9ad-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9ad-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb9ad-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="eb9ad-132">標頭</span><span class="sxs-lookup"><span data-stu-id="eb9ad-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb9ad-133"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="eb9ad-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="eb9ad-134">DLL</span><span class="sxs-lookup"><span data-stu-id="eb9ad-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb9ad-135"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9ad-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb9ad-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb9ad-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9ad-137">IESP</span><span class="sxs-lookup"><span data-stu-id="eb9ad-137">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="eb9ad-138">透視</span><span class="sxs-lookup"><span data-stu-id="eb9ad-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="eb9ad-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="eb9ad-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




