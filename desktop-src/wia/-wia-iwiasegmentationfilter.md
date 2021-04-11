---
description: IWiaSegmentationFilter 介面會偵測影像資料流程的子領域，並為每個區域建立個別的 IWiaItem2 專案。
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: 'IWiaSegmentationFilter 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848069"
---
# <a name="iwiasegmentationfilter-interface"></a><span data-ttu-id="90dbd-103">IWiaSegmentationFilter 介面</span><span class="sxs-lookup"><span data-stu-id="90dbd-103">IWiaSegmentationFilter interface</span></span>

<span data-ttu-id="90dbd-104">**IWiaSegmentationFilter** 介面會偵測影像資料流程的子領域，並為每個區域建立個別的 [**IWiaItem2**](-wia-iwiaitem2.md)專案。</span><span class="sxs-lookup"><span data-stu-id="90dbd-104">The **IWiaSegmentationFilter** interface detects sub-regions of an image stream and makes separate [**IWiaItem2**](-wia-iwiaitem2.md) items for each.</span></span>

## <a name="members"></a><span data-ttu-id="90dbd-105">成員</span><span class="sxs-lookup"><span data-stu-id="90dbd-105">Members</span></span>

<span data-ttu-id="90dbd-106">**IWiaSegmentationFilter** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="90dbd-106">The **IWiaSegmentationFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="90dbd-107">**IWiaSegmentationFilter** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="90dbd-107">**IWiaSegmentationFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="90dbd-108">方法</span><span class="sxs-lookup"><span data-stu-id="90dbd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="90dbd-109">方法</span><span class="sxs-lookup"><span data-stu-id="90dbd-109">Methods</span></span>

<span data-ttu-id="90dbd-110">**IWiaSegmentationFilter** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="90dbd-110">The **IWiaSegmentationFilter** interface has these methods.</span></span>



| <span data-ttu-id="90dbd-111">方法</span><span class="sxs-lookup"><span data-stu-id="90dbd-111">Method</span></span>                                                             | <span data-ttu-id="90dbd-112">描述</span><span class="sxs-lookup"><span data-stu-id="90dbd-112">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90dbd-113">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="90dbd-113">**DetectRegions**</span></span>](-wia-iwiasegmentationfilter-detectregions.md) | <span data-ttu-id="90dbd-114">決定影像的子領域，這些子領域會在平板玻璃上配置，讓每個子領域都可以取得個別的影像專案。</span><span class="sxs-lookup"><span data-stu-id="90dbd-114">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="90dbd-115">備註</span><span class="sxs-lookup"><span data-stu-id="90dbd-115">Remarks</span></span>

<span data-ttu-id="90dbd-116">應用程式應該使用 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 來建立分割篩選的新實例。</span><span class="sxs-lookup"><span data-stu-id="90dbd-116">An application should use [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) to create a new instance of the segmentation filter.</span></span> <span data-ttu-id="90dbd-117">應用程式通常會在顯示其預覽視窗之前呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="90dbd-117">An application typically calls this function before displaying its preview window.</span></span>

<span data-ttu-id="90dbd-118">在執行此篩選準則時，請使用 [**IWiaItem2：： CreateChildItem**](-wia-iwiaitem2-createchilditem.md) 來建立子專案。</span><span class="sxs-lookup"><span data-stu-id="90dbd-118">When implementing this filter, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) to create the child items.</span></span> <span data-ttu-id="90dbd-119">應用程式應該將 **複製 \_ 父 \_ 屬性 \_ 值** 傳遞給 *ICreationFlags* 參數，以確保在新建立的子系中的屬性（例如影像格式和解析度）相同，如同在父專案中一樣。</span><span class="sxs-lookup"><span data-stu-id="90dbd-119">The application should pass **COPY\_PARENT\_PROPERTY\_VALUES** to the *ICreationFlags* parameter to ensure that properties such as image format and resolution is the same in the newly created child as in the parent item.</span></span>

<span data-ttu-id="90dbd-120">分割篩選器必須支援與所用驅動程式搭配使用的所有影像格式。</span><span class="sxs-lookup"><span data-stu-id="90dbd-120">A segmentation filter must support all the image formats that the driver it is used with supports.</span></span> <span data-ttu-id="90dbd-121">Microsoft 提供的篩選支援點陣圖 (BMP) 、圖形交換格式 (GIF) 、JPEG、便攜網狀圖形 (PNG) ，以及標記的影像檔案格式 (TIFF) 。</span><span class="sxs-lookup"><span data-stu-id="90dbd-121">The Microsoft provided filter supports bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="90dbd-122">分割篩選器只能用於膠捲和平台掃描器專案。</span><span class="sxs-lookup"><span data-stu-id="90dbd-122">The segmentation filter should be used only on film and flatbed scanner items.</span></span> <span data-ttu-id="90dbd-123">針對膠捲掃描，掃描器通常會隨附固定的框架，在此情況下，驅動程式會建立子專案，而應用程式不應叫用分割篩選。</span><span class="sxs-lookup"><span data-stu-id="90dbd-123">For film scanning, a scanner often comes with fixed frames in which case the driver created the child items and the application should not invoke the segmentation filter.</span></span>

<span data-ttu-id="90dbd-124">**IWiaSegmentationFilter** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。</span><span class="sxs-lookup"><span data-stu-id="90dbd-124">The **IWiaSegmentationFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="90dbd-125">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="90dbd-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="90dbd-126">Description</span><span class="sxs-lookup"><span data-stu-id="90dbd-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="90dbd-127">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="90dbd-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="90dbd-128">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="90dbd-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="90dbd-129">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="90dbd-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="90dbd-130">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="90dbd-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="90dbd-131">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="90dbd-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="90dbd-132">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="90dbd-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="90dbd-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="90dbd-133">Requirements</span></span>



| <span data-ttu-id="90dbd-134">需求</span><span class="sxs-lookup"><span data-stu-id="90dbd-134">Requirement</span></span> | <span data-ttu-id="90dbd-135">值</span><span class="sxs-lookup"><span data-stu-id="90dbd-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90dbd-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90dbd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="90dbd-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90dbd-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="90dbd-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90dbd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="90dbd-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90dbd-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="90dbd-140">標頭</span><span class="sxs-lookup"><span data-stu-id="90dbd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="90dbd-141"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="90dbd-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="90dbd-142">Idl</span><span class="sxs-lookup"><span data-stu-id="90dbd-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90dbd-143"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="90dbd-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
