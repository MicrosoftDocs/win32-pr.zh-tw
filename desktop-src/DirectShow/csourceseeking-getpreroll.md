---
description: GetPreroll 方法會捕獲預先進行的時間。 這個方法會實 IMediaSeeking：： GetPreroll 方法。
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: 'CSourceSeeking. GetPreroll 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994759"
---
# <a name="csourceseekinggetpreroll-method"></a><span data-ttu-id="8ca14-104">CSourceSeeking. GetPreroll 方法</span><span class="sxs-lookup"><span data-stu-id="8ca14-104">CSourceSeeking.GetPreroll method</span></span>

<span data-ttu-id="8ca14-105">方法會取出預先進行 `GetPreroll` 的時間。</span><span class="sxs-lookup"><span data-stu-id="8ca14-105">The `GetPreroll` method retrieves the preroll time.</span></span> <span data-ttu-id="8ca14-106">這個方法會實 [**IMediaSeeking：： GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) 方法。</span><span class="sxs-lookup"><span data-stu-id="8ca14-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca14-107">語法</span><span class="sxs-lookup"><span data-stu-id="8ca14-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="8ca14-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ca14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca14-109">*pPreroll*</span><span class="sxs-lookup"><span data-stu-id="8ca14-109">*pPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="8ca14-110">接收預先提供時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="8ca14-110">Pointer to a variable that receives the preroll time.</span></span> <span data-ttu-id="8ca14-111">值設定為零。</span><span class="sxs-lookup"><span data-stu-id="8ca14-111">The value is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca14-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ca14-112">Return value</span></span>

<span data-ttu-id="8ca14-113">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8ca14-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="8ca14-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8ca14-114">Return code</span></span>                                                                               | <span data-ttu-id="8ca14-115">Description</span><span class="sxs-lookup"><span data-stu-id="8ca14-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="8ca14-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca14-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8ca14-117">Success</span><span class="sxs-lookup"><span data-stu-id="8ca14-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="8ca14-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca14-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8ca14-119">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="8ca14-119">**NULL** pointer value</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ca14-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ca14-120">Requirements</span></span>



| <span data-ttu-id="8ca14-121">需求</span><span class="sxs-lookup"><span data-stu-id="8ca14-121">Requirement</span></span> | <span data-ttu-id="8ca14-122">值</span><span class="sxs-lookup"><span data-stu-id="8ca14-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca14-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8ca14-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8ca14-124"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8ca14-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ca14-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ca14-125">Library</span></span><br/> | <dl> <span data-ttu-id="8ca14-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8ca14-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca14-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ca14-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca14-128">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="8ca14-128">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




