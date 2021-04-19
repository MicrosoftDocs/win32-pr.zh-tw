---
description: '\_ \_ 從篩選圖形移除篩選時，JoinFilterGraph 方法會傳送 EC 視窗終結事件通知。'
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: 'CBaseVideoRenderer. JoinFilterGraph 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984330"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a><span data-ttu-id="33f89-103">CBaseVideoRenderer. JoinFilterGraph 方法</span><span class="sxs-lookup"><span data-stu-id="33f89-103">CBaseVideoRenderer.JoinFilterGraph method</span></span>

<span data-ttu-id="33f89-104">`JoinFilterGraph`從篩選圖形中移除篩選時，方法會傳送 [**EC \_ 視窗 \_**](ec-window-destroyed.md)終結事件通知。</span><span class="sxs-lookup"><span data-stu-id="33f89-104">The `JoinFilterGraph` method sends [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification when a filter is removed from the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f89-105">語法</span><span class="sxs-lookup"><span data-stu-id="33f89-105">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="33f89-106">參數</span><span class="sxs-lookup"><span data-stu-id="33f89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f89-107">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="33f89-107">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="33f89-108">要加入之篩選圖形的指標。</span><span class="sxs-lookup"><span data-stu-id="33f89-108">Pointer to the filter graph to join.</span></span>

</dd> <dt>

<span data-ttu-id="33f89-109">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33f89-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33f89-110">要加入之篩選器名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="33f89-110">Pointer to the name of the filter being added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f89-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="33f89-111">Return value</span></span>

<span data-ttu-id="33f89-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="33f89-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33f89-113">備註</span><span class="sxs-lookup"><span data-stu-id="33f89-113">Remarks</span></span>

<span data-ttu-id="33f89-114">此成員函式會覆寫 [**CBaseFilter：： JoinFilterGraph**](cbasefilter-joinfiltergraph.md) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="33f89-114">This member function overrides the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) member function.</span></span> <span data-ttu-id="33f89-115">如果篩選準則離開篩選圖形 (*pGraph* 為 **Null**) ，它會傳送 [**EC \_ 視窗 \_**](ec-window-destroyed.md) 終結事件通知，讓資源管理員不會以焦點物件的形式來保存轉譯器。</span><span class="sxs-lookup"><span data-stu-id="33f89-115">If the filter is leaving the filter graph (*pGraph* is **NULL**), it sends an [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification so that the resource manager does not hold on to the renderer as a focus object.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f89-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="33f89-116">Requirements</span></span>



| <span data-ttu-id="33f89-117">需求</span><span class="sxs-lookup"><span data-stu-id="33f89-117">Requirement</span></span> | <span data-ttu-id="33f89-118">值</span><span class="sxs-lookup"><span data-stu-id="33f89-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f89-119">標頭</span><span class="sxs-lookup"><span data-stu-id="33f89-119">Header</span></span><br/>  | <dl> <span data-ttu-id="33f89-120"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="33f89-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="33f89-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="33f89-121">Library</span></span><br/> | <dl> <span data-ttu-id="33f89-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="33f89-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f89-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33f89-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f89-124">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="33f89-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




