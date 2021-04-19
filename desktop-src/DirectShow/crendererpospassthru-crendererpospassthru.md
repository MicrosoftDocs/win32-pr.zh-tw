---
description: 函式方法。
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: 'CRendererPosPassThru. CRendererPosPassThru (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97b21ba3ad9438189f97c3e0bb9f011b210a0195
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994792"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="224e3-103">CRendererPosPassThru. CRendererPosPassThru 函數</span><span class="sxs-lookup"><span data-stu-id="224e3-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="224e3-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="224e3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="224e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="224e3-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="224e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="224e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224e3-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="224e3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="224e3-108">物件名稱的指標，用於偵測用途。</span><span class="sxs-lookup"><span data-stu-id="224e3-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="224e3-109">在靜態記憶體中配置此參數。</span><span class="sxs-lookup"><span data-stu-id="224e3-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="224e3-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="224e3-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="224e3-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="224e3-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="224e3-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="224e3-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="224e3-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="224e3-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="224e3-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="224e3-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="224e3-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="224e3-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="224e3-116">忽略。</span><span class="sxs-lookup"><span data-stu-id="224e3-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="224e3-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="224e3-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="224e3-118">篩選器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="224e3-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="224e3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="224e3-119">Requirements</span></span>



| <span data-ttu-id="224e3-120">需求</span><span class="sxs-lookup"><span data-stu-id="224e3-120">Requirement</span></span> | <span data-ttu-id="224e3-121">值</span><span class="sxs-lookup"><span data-stu-id="224e3-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="224e3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="224e3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="224e3-123"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="224e3-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="224e3-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="224e3-124">Library</span></span><br/> | <dl> <span data-ttu-id="224e3-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="224e3-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




