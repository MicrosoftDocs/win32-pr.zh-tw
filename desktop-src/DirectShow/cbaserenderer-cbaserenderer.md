---
description: CBaseRenderer。 CBaseRenderer 函式-函數方法。
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: 'CBaseRenderer. CBaseRenderer (Renbase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 68ebc6255456f0fcbb4bf732a91dce981d0f78ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119906"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="e56a6-103">CBaseRenderer. CBaseRenderer 函數</span><span class="sxs-lookup"><span data-stu-id="e56a6-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="e56a6-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="e56a6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56a6-105">語法</span><span class="sxs-lookup"><span data-stu-id="e56a6-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="e56a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="e56a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56a6-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="e56a6-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="e56a6-108">轉譯器的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="e56a6-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="e56a6-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="e56a6-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e56a6-110">包含篩選名稱之字串的指標，用於進行調試。</span><span class="sxs-lookup"><span data-stu-id="e56a6-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="e56a6-111">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="e56a6-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e56a6-112">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="e56a6-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="e56a6-113">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="e56a6-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="e56a6-114">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e56a6-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e56a6-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="e56a6-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e56a6-116">接收 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e56a6-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="e56a6-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="e56a6-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="e56a6-118">計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="e56a6-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e56a6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e56a6-119">Requirements</span></span>



| <span data-ttu-id="e56a6-120">需求</span><span class="sxs-lookup"><span data-stu-id="e56a6-120">Requirement</span></span> | <span data-ttu-id="e56a6-121">值</span><span class="sxs-lookup"><span data-stu-id="e56a6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e56a6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e56a6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e56a6-123"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e56a6-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e56a6-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="e56a6-124">Library</span></span><br/> | <dl> <span data-ttu-id="e56a6-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e56a6-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56a6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e56a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56a6-127">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="e56a6-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




