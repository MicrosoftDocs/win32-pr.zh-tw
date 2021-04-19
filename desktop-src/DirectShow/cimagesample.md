---
description: CImageSample 類別會執行媒體範例，以管理與 GDI 裝置無關的點陣圖 (DIB) 。
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: 'CImageSample 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994179"
---
# <a name="cimagesample-class"></a><span data-ttu-id="90084-103">CImageSample 類別</span><span class="sxs-lookup"><span data-stu-id="90084-103">CImageSample class</span></span>

![cimagesample 類別階層](images/wutil03.png)

<span data-ttu-id="90084-105">`CImageSample`類別會執行媒體範例，以管理與 GDI 裝置無關的點陣圖 (DIB) 。</span><span class="sxs-lookup"><span data-stu-id="90084-105">The `CImageSample` class implements a media sample that manages a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="90084-106">這個類別衍生自 [**CMediaSample**](cmediasample.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="90084-106">This class derives from the [**CMediaSample**](cmediasample.md) class.</span></span> <span data-ttu-id="90084-107">其目的是要搭配 [**CImageAllocator**](cimageallocator.md) 類別使用。</span><span class="sxs-lookup"><span data-stu-id="90084-107">It is intended to be used with the [**CImageAllocator**](cimageallocator.md) class.</span></span> <span data-ttu-id="90084-108">**CImageAllocator** 類別會提供可建立物件的配置器 `CImageSample` 。</span><span class="sxs-lookup"><span data-stu-id="90084-108">The **CImageAllocator** class provides an allocator that creates `CImageSample` objects.</span></span>



| <span data-ttu-id="90084-109">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="90084-109">Protected Member Variables</span></span>                        | <span data-ttu-id="90084-110">Description</span><span class="sxs-lookup"><span data-stu-id="90084-110">Description</span></span>                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="90084-111">**m \_ DibData**</span><span class="sxs-lookup"><span data-stu-id="90084-111">**m\_DibData**</span></span>](cimagesample-m-dibdata.md)      | <span data-ttu-id="90084-112">包含此物件正在管理之 DIB 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90084-112">Contains information about the DIB that this object is managing.</span></span>  |
| [<span data-ttu-id="90084-113">**m \_ bInit**</span><span class="sxs-lookup"><span data-stu-id="90084-113">**m\_bInit**</span></span>](cimagesample-m-binit.md)          | <span data-ttu-id="90084-114">指出物件是否已初始化。</span><span class="sxs-lookup"><span data-stu-id="90084-114">Indicates whether the object has been initialized.</span></span>                |
| <span data-ttu-id="90084-115">公用方法</span><span class="sxs-lookup"><span data-stu-id="90084-115">Public Methods</span></span>                                    | <span data-ttu-id="90084-116">Description</span><span class="sxs-lookup"><span data-stu-id="90084-116">Description</span></span>                                                       |
| [<span data-ttu-id="90084-117">**CImageSample**</span><span class="sxs-lookup"><span data-stu-id="90084-117">**CImageSample**</span></span>](cimagesample-cimagesample.md) | <span data-ttu-id="90084-118">函式方法。</span><span class="sxs-lookup"><span data-stu-id="90084-118">Constructor method.</span></span>                                               |
| [<span data-ttu-id="90084-119">**GetDIBData**</span><span class="sxs-lookup"><span data-stu-id="90084-119">**GetDIBData**</span></span>](cimagesample-getdibdata.md)     | <span data-ttu-id="90084-120">抓取此物件正在管理的 DIB 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90084-120">Retrieves information about the DIB that this object is managing.</span></span> |
| [<span data-ttu-id="90084-121">**SetDIBData**</span><span class="sxs-lookup"><span data-stu-id="90084-121">**SetDIBData**</span></span>](cimagesample-setdibdata.md)     | <span data-ttu-id="90084-122">設定此物件正在管理的 DIB 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90084-122">Sets information about the DIB that this object is managing.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="90084-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="90084-123">Requirements</span></span>



| <span data-ttu-id="90084-124">需求</span><span class="sxs-lookup"><span data-stu-id="90084-124">Requirement</span></span> | <span data-ttu-id="90084-125">值</span><span class="sxs-lookup"><span data-stu-id="90084-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90084-126">標頭</span><span class="sxs-lookup"><span data-stu-id="90084-126">Header</span></span><br/>  | <dl> <span data-ttu-id="90084-127"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="90084-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="90084-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="90084-128">Library</span></span><br/> | <dl> <span data-ttu-id="90084-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="90084-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




