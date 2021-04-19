---
description: 函式方法。
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: 'CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990644"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="70923-103">CBaseVideoRenderer. CBaseVideoRenderer 函數</span><span class="sxs-lookup"><span data-stu-id="70923-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="70923-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="70923-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="70923-105">語法</span><span class="sxs-lookup"><span data-stu-id="70923-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="70923-106">參數</span><span class="sxs-lookup"><span data-stu-id="70923-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70923-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="70923-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="70923-108">此轉譯器的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="70923-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="70923-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="70923-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="70923-110">用於偵錯工具之描述的指標。</span><span class="sxs-lookup"><span data-stu-id="70923-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="70923-111">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="70923-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="70923-112">匯總的擁有者物件的指標。</span><span class="sxs-lookup"><span data-stu-id="70923-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="70923-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="70923-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="70923-114">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="70923-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70923-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="70923-115">Requirements</span></span>



| <span data-ttu-id="70923-116">需求</span><span class="sxs-lookup"><span data-stu-id="70923-116">Requirement</span></span> | <span data-ttu-id="70923-117">值</span><span class="sxs-lookup"><span data-stu-id="70923-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70923-118">標頭</span><span class="sxs-lookup"><span data-stu-id="70923-118">Header</span></span><br/>  | <dl> <span data-ttu-id="70923-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="70923-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="70923-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="70923-120">Library</span></span><br/> | <dl> <span data-ttu-id="70923-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="70923-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70923-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70923-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70923-123">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="70923-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




