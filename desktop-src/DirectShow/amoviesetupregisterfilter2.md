---
description: AMovieSetupRegisterFilter2 函式會使用 IFilterMapper2 介面，在登錄中註冊篩選器的業績、釘選和媒體類型。
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: 'AMovieSetupRegisterFilter2 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976210"
---
# <a name="amoviesetupregisterfilter2-function"></a><span data-ttu-id="9fb68-103">AMovieSetupRegisterFilter2 函式</span><span class="sxs-lookup"><span data-stu-id="9fb68-103">AMovieSetupRegisterFilter2 function</span></span>

<span data-ttu-id="9fb68-104">**AMovieSetupRegisterFilter2** 函式會使用 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)介面，在登錄中註冊篩選器的業績、釘選和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9fb68-104">The **AMovieSetupRegisterFilter2** function registers a filter's merit, pins, and media types in the registry using the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb68-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fb68-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="9fb68-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fb68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb68-107">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="9fb68-107">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb68-108">[**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md)資料的指標。</span><span class="sxs-lookup"><span data-stu-id="9fb68-108">Pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="9fb68-109">*pIFM2*</span><span class="sxs-lookup"><span data-stu-id="9fb68-109">*pIFM2*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb68-110">[**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9fb68-110">Pointer to [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9fb68-111">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="9fb68-111">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb68-112">指出是否要註冊篩選準則的值。 **TRUE** 表示註冊篩選準則， **FALSE** 表示將其取消註冊。</span><span class="sxs-lookup"><span data-stu-id="9fb68-112">Value indicating whether to register the filter; **TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb68-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fb68-113">Return value</span></span>

<span data-ttu-id="9fb68-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9fb68-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9fb68-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9fb68-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb68-116">備註</span><span class="sxs-lookup"><span data-stu-id="9fb68-116">Remarks</span></span>

<span data-ttu-id="9fb68-117">[**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)函式會在註冊 COM 伺服器之後，呼叫此 helper 函式以註冊篩選。</span><span class="sxs-lookup"><span data-stu-id="9fb68-117">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function calls this helper function to register a filter after the COM server has been registered.</span></span>

<span data-ttu-id="9fb68-118">一般而言，篩選準則會使用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) ，且不會直接呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="9fb68-118">Typically, a filter will use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) and will not call this function directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb68-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fb68-119">Requirements</span></span>



| <span data-ttu-id="9fb68-120">需求</span><span class="sxs-lookup"><span data-stu-id="9fb68-120">Requirement</span></span> | <span data-ttu-id="9fb68-121">值</span><span class="sxs-lookup"><span data-stu-id="9fb68-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb68-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9fb68-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9fb68-123"><dt>Dllsetup (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9fb68-123"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9fb68-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9fb68-124">Library</span></span><br/> | <dl> <span data-ttu-id="9fb68-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9fb68-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb68-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fb68-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb68-127">**DLL 安裝函式**</span><span class="sxs-lookup"><span data-stu-id="9fb68-127">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




