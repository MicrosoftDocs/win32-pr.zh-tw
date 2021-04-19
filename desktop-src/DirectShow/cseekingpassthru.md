---
description: CSeekingPassThru 類別是建立 CPosPassThru 和 CRendererPosPassThru 物件的 helper 物件。
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: 'CSeekingPassThru 類別 (Seekpt) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990030"
---
# <a name="cseekingpassthru-class"></a><span data-ttu-id="35c2a-103">CSeekingPassThru 類別</span><span class="sxs-lookup"><span data-stu-id="35c2a-103">CSeekingPassThru class</span></span>

<span data-ttu-id="35c2a-104">`CSeekingPassThru`類別是可建立 [**CPosPassThru**](cpospassthru.md)和 [**CRendererPosPassThru**](crendererpospassthru.md)物件的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="35c2a-104">The `CSeekingPassThru` class is a helper object that creates [**CPosPassThru**](cpospassthru.md) and [**CRendererPosPassThru**](crendererpospassthru.md) objects.</span></span>

<span data-ttu-id="35c2a-105">**CPosPassThru** 和 **CRendererPosPassThru** 類別是通過上游搜尋命令的協助程式物件，因此 `CSeekingPassThru` 類別是用來建立 helper 物件的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="35c2a-105">The **CPosPassThru** and **CRendererPosPassThru** classes are helper objects that pass seeking commands upstream, so the `CSeekingPassThru` class is a helper object for creating helper objects.</span></span>

<span data-ttu-id="35c2a-106">不需要直接使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="35c2a-106">It is not necessary to use this class directly.</span></span> <span data-ttu-id="35c2a-107">相反地，請使用 [**CreatePosPassThru**](createpospassthru.md) 函式，此函式會處理所有使用這個類別的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="35c2a-107">Instead, use the [**CreatePosPassThru**](createpospassthru.md) function, which handles all of the details of using this class.</span></span> <span data-ttu-id="35c2a-108">它有更多從 Quartz.dll 載入物件的優點，這會稍微減少篩選的程式碼大小。</span><span class="sxs-lookup"><span data-stu-id="35c2a-108">It has the further advantage of loading the object from Quartz.dll, which reduces the code size of your filter somewhat.</span></span> <span data-ttu-id="35c2a-109">如需詳細資訊，請參閱 [**CPosPassThru**](cpospassthru.md)。</span><span class="sxs-lookup"><span data-stu-id="35c2a-109">For more information, see [**CPosPassThru**](cpospassthru.md).</span></span>

<span data-ttu-id="35c2a-110">`CSeekingPassThru`類別會公開 [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru)介面。</span><span class="sxs-lookup"><span data-stu-id="35c2a-110">The `CSeekingPassThru` class exposes the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface.</span></span> <span data-ttu-id="35c2a-111">[**ISeekingPassThru：： Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init)方法會初始化物件。</span><span class="sxs-lookup"><span data-stu-id="35c2a-111">The [**ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) method initializes the object.</span></span> <span data-ttu-id="35c2a-112">物件初始化之後，篩選可以針對 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 和 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面進行查詢。</span><span class="sxs-lookup"><span data-stu-id="35c2a-112">After the object is initialized, the filter can query it for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interfaces.</span></span>



| <span data-ttu-id="35c2a-113">公用方法</span><span class="sxs-lookup"><span data-stu-id="35c2a-113">Public Methods</span></span>                                                  | <span data-ttu-id="35c2a-114">Description</span><span class="sxs-lookup"><span data-stu-id="35c2a-114">Description</span></span>                        |
|-----------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="35c2a-115">**CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="35c2a-115">**CSeekingPassThru**</span></span>](cseekingpassthru-cseekingpassthru.md)   | <span data-ttu-id="35c2a-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="35c2a-116">Constructor method.</span></span>                |
| [<span data-ttu-id="35c2a-117">**~ CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="35c2a-117">**~CSeekingPassThru**</span></span>](cseekingpassthru--cseekingpassthru.md) | <span data-ttu-id="35c2a-118">函式方法。</span><span class="sxs-lookup"><span data-stu-id="35c2a-118">Destructor method.</span></span>                 |
| [<span data-ttu-id="35c2a-119">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="35c2a-119">**CreateInstance**</span></span>](cseekingpassthru-createinstance.md)       | <span data-ttu-id="35c2a-120">建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="35c2a-120">Creates an instance of the object.</span></span> |
| <span data-ttu-id="35c2a-121">ISeekingPassThru 方法</span><span class="sxs-lookup"><span data-stu-id="35c2a-121">ISeekingPassThru Methods</span></span>                                        | <span data-ttu-id="35c2a-122">Description</span><span class="sxs-lookup"><span data-stu-id="35c2a-122">Description</span></span>                        |
| [<span data-ttu-id="35c2a-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="35c2a-123">**Init**</span></span>](cseekingpassthru-init.md)                           | <span data-ttu-id="35c2a-124">初始化物件。</span><span class="sxs-lookup"><span data-stu-id="35c2a-124">Initializes the object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="35c2a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="35c2a-125">Requirements</span></span>



| <span data-ttu-id="35c2a-126">需求</span><span class="sxs-lookup"><span data-stu-id="35c2a-126">Requirement</span></span> | <span data-ttu-id="35c2a-127">值</span><span class="sxs-lookup"><span data-stu-id="35c2a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c2a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="35c2a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="35c2a-129"><dt>Seekpt (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="35c2a-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="35c2a-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="35c2a-130">Library</span></span><br/> | <dl> <span data-ttu-id="35c2a-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="35c2a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




