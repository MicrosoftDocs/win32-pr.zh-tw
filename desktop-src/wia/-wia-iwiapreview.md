---
description: IWiaPreview 介面會在內部快取未篩選的影像，並透過影像處理篩選器來傳遞它們。
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: 'IWiaPreview 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191399"
---
# <a name="iwiapreview-interface"></a><span data-ttu-id="acde5-103">IWiaPreview 介面</span><span class="sxs-lookup"><span data-stu-id="acde5-103">IWiaPreview interface</span></span>

<span data-ttu-id="acde5-104">**IWiaPreview** 介面會在內部快取未篩選的影像，並透過影像處理篩選器來傳遞它們。</span><span class="sxs-lookup"><span data-stu-id="acde5-104">The **IWiaPreview** interface caches unfiltered images internally and passes them through image processing filters.</span></span>

## <a name="members"></a><span data-ttu-id="acde5-105">成員</span><span class="sxs-lookup"><span data-stu-id="acde5-105">Members</span></span>

<span data-ttu-id="acde5-106">**IWiaPreview** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="acde5-106">The **IWiaPreview** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="acde5-107">**IWiaPreview** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="acde5-107">**IWiaPreview** also has these types of members:</span></span>

-   [<span data-ttu-id="acde5-108">方法</span><span class="sxs-lookup"><span data-stu-id="acde5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="acde5-109">方法</span><span class="sxs-lookup"><span data-stu-id="acde5-109">Methods</span></span>

<span data-ttu-id="acde5-110">**IWiaPreview** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="acde5-110">The **IWiaPreview** interface has these methods.</span></span>



| <span data-ttu-id="acde5-111">方法</span><span class="sxs-lookup"><span data-stu-id="acde5-111">Method</span></span>                                                  | <span data-ttu-id="acde5-112">描述</span><span class="sxs-lookup"><span data-stu-id="acde5-112">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acde5-113">**清楚**</span><span class="sxs-lookup"><span data-stu-id="acde5-113">**Clear**</span></span>](-wia-iwiapreview-clear.md)                 | <span data-ttu-id="acde5-114">釋放 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法所快取的未篩選映射。</span><span class="sxs-lookup"><span data-stu-id="acde5-114">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="acde5-115">它也會釋放影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="acde5-115">It also releases the image processing filter.</span></span> <br/>          |
| [<span data-ttu-id="acde5-116">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="acde5-116">**DetectRegions**</span></span>](-wia-iwiapreview-detectregions.md) | <span data-ttu-id="acde5-117">叫用驅動程式分割篩選，並將 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像傳遞至篩選。</span><span class="sxs-lookup"><span data-stu-id="acde5-117">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span> <br/> |
| [<span data-ttu-id="acde5-118">**GetNewPreview**</span><span class="sxs-lookup"><span data-stu-id="acde5-118">**GetNewPreview**</span></span>](-wia-iwiapreview-getnewpreview.md) | <span data-ttu-id="acde5-119">在內部快取從驅動程式傳回之未篩選的映射。</span><span class="sxs-lookup"><span data-stu-id="acde5-119">Caches internally the unfiltered image returned from the driver.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="acde5-120">**UpdatePreview**</span><span class="sxs-lookup"><span data-stu-id="acde5-120">**UpdatePreview**</span></span>](-wia-iwiapreview-updatepreview.md) | <span data-ttu-id="acde5-121">取得 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像。</span><span class="sxs-lookup"><span data-stu-id="acde5-121">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="acde5-122">備註</span><span class="sxs-lookup"><span data-stu-id="acde5-122">Remarks</span></span>

<span data-ttu-id="acde5-123">[**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md)方法會自動呼叫此篩選器。</span><span class="sxs-lookup"><span data-stu-id="acde5-123">This filter is called automatically by the [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) method.</span></span>

<span data-ttu-id="acde5-124">**IWiaPreview** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。</span><span class="sxs-lookup"><span data-stu-id="acde5-124">The **IWiaPreview** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="acde5-125">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="acde5-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="acde5-126">Description</span><span class="sxs-lookup"><span data-stu-id="acde5-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="acde5-127">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="acde5-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="acde5-128">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="acde5-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="acde5-129">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="acde5-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="acde5-130">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="acde5-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="acde5-131">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="acde5-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="acde5-132">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="acde5-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="acde5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="acde5-133">Requirements</span></span>



| <span data-ttu-id="acde5-134">需求</span><span class="sxs-lookup"><span data-stu-id="acde5-134">Requirement</span></span> | <span data-ttu-id="acde5-135">值</span><span class="sxs-lookup"><span data-stu-id="acde5-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="acde5-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acde5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="acde5-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acde5-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="acde5-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acde5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="acde5-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acde5-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="acde5-140">標頭</span><span class="sxs-lookup"><span data-stu-id="acde5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="acde5-141"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="acde5-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="acde5-142">Idl</span><span class="sxs-lookup"><span data-stu-id="acde5-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="acde5-143"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="acde5-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
