---
description: OnRenderStart 方法會設定轉譯的資訊。
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: 'CBaseVideoRenderer. OnRenderStart 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995629"
---
# <a name="cbasevideorendereronrenderstart-method"></a><span data-ttu-id="dacac-103">CBaseVideoRenderer. OnRenderStart 方法</span><span class="sxs-lookup"><span data-stu-id="dacac-103">CBaseVideoRenderer.OnRenderStart method</span></span>

<span data-ttu-id="dacac-104">`OnRenderStart`方法會設定轉譯的資訊。</span><span class="sxs-lookup"><span data-stu-id="dacac-104">The `OnRenderStart` method sets information for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="dacac-105">語法</span><span class="sxs-lookup"><span data-stu-id="dacac-105">Syntax</span></span>


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="dacac-106">參數</span><span class="sxs-lookup"><span data-stu-id="dacac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dacac-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="dacac-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="dacac-108">媒體範例的指標。</span><span class="sxs-lookup"><span data-stu-id="dacac-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dacac-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="dacac-109">Return value</span></span>

<span data-ttu-id="dacac-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dacac-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dacac-111">備註</span><span class="sxs-lookup"><span data-stu-id="dacac-111">Remarks</span></span>

<span data-ttu-id="dacac-112">此成員函式會從系統抓取目前的時鐘時間，並將它儲存在繪圖完成時要使用的成員變數中。</span><span class="sxs-lookup"><span data-stu-id="dacac-112">This member function retrieves the current clock time from the system and stores it in a member variable to be used when the drawing is complete.</span></span> <span data-ttu-id="dacac-113">函數也會執行效能記錄。</span><span class="sxs-lookup"><span data-stu-id="dacac-113">The function also performs performance logging.</span></span> <span data-ttu-id="dacac-114">此成員函式應該只在開始繪製之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="dacac-114">This member function should be called just before drawing starts.</span></span>

<span data-ttu-id="dacac-115">此成員函式會覆寫 [**CBaseRenderer：： OnRenderStart**](cbaserenderer-onrenderstart.md)。</span><span class="sxs-lookup"><span data-stu-id="dacac-115">This member function overrides [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dacac-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dacac-116">Requirements</span></span>



| <span data-ttu-id="dacac-117">需求</span><span class="sxs-lookup"><span data-stu-id="dacac-117">Requirement</span></span> | <span data-ttu-id="dacac-118">值</span><span class="sxs-lookup"><span data-stu-id="dacac-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dacac-119">標頭</span><span class="sxs-lookup"><span data-stu-id="dacac-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dacac-120"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dacac-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dacac-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="dacac-121">Library</span></span><br/> | <dl> <span data-ttu-id="dacac-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dacac-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dacac-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dacac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dacac-124">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="dacac-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




