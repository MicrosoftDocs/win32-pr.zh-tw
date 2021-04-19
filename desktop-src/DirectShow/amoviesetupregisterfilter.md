---
description: 已過時。 請改用 AMovieSetupRegisterFilter2。
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: 'AMovieSetupRegisterFilter 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998857"
---
# <a name="amoviesetupregisterfilter-function"></a><span data-ttu-id="7f384-104">AMovieSetupRegisterFilter 函式</span><span class="sxs-lookup"><span data-stu-id="7f384-104">AMovieSetupRegisterFilter function</span></span>

<span data-ttu-id="7f384-105">已過時。</span><span class="sxs-lookup"><span data-stu-id="7f384-105">Obsolete.</span></span> <span data-ttu-id="7f384-106">請改用 [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) 。</span><span class="sxs-lookup"><span data-stu-id="7f384-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f384-107">語法</span><span class="sxs-lookup"><span data-stu-id="7f384-107">Syntax</span></span>


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="7f384-108">參數</span><span class="sxs-lookup"><span data-stu-id="7f384-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f384-109">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="7f384-109">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="7f384-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="7f384-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7f384-111">*pIFM*</span><span class="sxs-lookup"><span data-stu-id="7f384-111">*pIFM*</span></span> 
</dt> <dd>

<span data-ttu-id="7f384-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="7f384-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7f384-113">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="7f384-113">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="7f384-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="7f384-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f384-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f384-115">Return value</span></span>

<span data-ttu-id="7f384-116">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7f384-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f384-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7f384-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f384-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f384-118">Requirements</span></span>



| <span data-ttu-id="7f384-119">需求</span><span class="sxs-lookup"><span data-stu-id="7f384-119">Requirement</span></span> | <span data-ttu-id="7f384-120">值</span><span class="sxs-lookup"><span data-stu-id="7f384-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f384-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7f384-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7f384-122"><dt>Dllsetup (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f384-122"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7f384-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f384-123">Library</span></span><br/> | <dl> <span data-ttu-id="7f384-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7f384-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f384-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f384-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f384-126">**DLL 安裝函式**</span><span class="sxs-lookup"><span data-stu-id="7f384-126">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




