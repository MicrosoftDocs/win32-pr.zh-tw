---
description: CBaseVideoRenderer。 CBaseVideoRenderer 函式-函數方法。
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
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095836"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="80480-103">CBaseVideoRenderer. CBaseVideoRenderer 函數</span><span class="sxs-lookup"><span data-stu-id="80480-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="80480-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="80480-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80480-105">語法</span><span class="sxs-lookup"><span data-stu-id="80480-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="80480-106">參數</span><span class="sxs-lookup"><span data-stu-id="80480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80480-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="80480-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="80480-108">此轉譯器的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="80480-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="80480-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="80480-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="80480-110">用於偵錯工具之描述的指標。</span><span class="sxs-lookup"><span data-stu-id="80480-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="80480-111">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="80480-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="80480-112">匯總的擁有者物件的指標。</span><span class="sxs-lookup"><span data-stu-id="80480-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="80480-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="80480-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="80480-114">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="80480-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80480-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="80480-115">Requirements</span></span>



| <span data-ttu-id="80480-116">需求</span><span class="sxs-lookup"><span data-stu-id="80480-116">Requirement</span></span> | <span data-ttu-id="80480-117">值</span><span class="sxs-lookup"><span data-stu-id="80480-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80480-118">標頭</span><span class="sxs-lookup"><span data-stu-id="80480-118">Header</span></span><br/>  | <dl> <span data-ttu-id="80480-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="80480-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80480-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="80480-120">Library</span></span><br/> | <dl> <span data-ttu-id="80480-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="80480-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80480-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80480-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80480-123">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="80480-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




