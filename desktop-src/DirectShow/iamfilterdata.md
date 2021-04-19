---
description: 請注意，此介面已被取代。
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: 'IAMFilterData 介面 (Fil \_ data .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989557"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="30070-103">IAMFilterData 介面</span><span class="sxs-lookup"><span data-stu-id="30070-103">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="30070-104">這個介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="30070-104">This interface has been deprecated.</span></span> <span data-ttu-id="30070-105">新的應用程式應該改用 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 介面。</span><span class="sxs-lookup"><span data-stu-id="30070-105">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="30070-106">`IAMFilterData`介面會將篩選資訊轉換成封裝的二進位資料，而這些資料可以儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="30070-106">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="30070-107">篩選對應程式物件會公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="30070-107">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="30070-108">成員</span><span class="sxs-lookup"><span data-stu-id="30070-108">Members</span></span>

<span data-ttu-id="30070-109">**IAMFilterData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="30070-109">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="30070-110">**IAMFilterData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="30070-110">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="30070-111">方法</span><span class="sxs-lookup"><span data-stu-id="30070-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="30070-112">方法</span><span class="sxs-lookup"><span data-stu-id="30070-112">Methods</span></span>

<span data-ttu-id="30070-113">**IAMFilterData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="30070-113">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="30070-114">方法</span><span class="sxs-lookup"><span data-stu-id="30070-114">Method</span></span>                                                     | <span data-ttu-id="30070-115">描述</span><span class="sxs-lookup"><span data-stu-id="30070-115">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="30070-116">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="30070-116">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="30070-117">建立篩選的二進位登錄資料。</span><span class="sxs-lookup"><span data-stu-id="30070-117">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="30070-118">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="30070-118">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="30070-119">解壓縮篩選的二進位登錄資料。</span><span class="sxs-lookup"><span data-stu-id="30070-119">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30070-120">備註</span><span class="sxs-lookup"><span data-stu-id="30070-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30070-121">標頭 Fil \_ data .h 位於 Windows SDK 的對應工具 [範例](mapper-sample.md) 目錄中。</span><span class="sxs-lookup"><span data-stu-id="30070-121">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30070-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="30070-122">Requirements</span></span>



| <span data-ttu-id="30070-123">需求</span><span class="sxs-lookup"><span data-stu-id="30070-123">Requirement</span></span> | <span data-ttu-id="30070-124">值</span><span class="sxs-lookup"><span data-stu-id="30070-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30070-125">標頭</span><span class="sxs-lookup"><span data-stu-id="30070-125">Header</span></span><br/> | <dl> <span data-ttu-id="30070-126"><dt>Fil \_ 資料。h</dt></span><span class="sxs-lookup"><span data-stu-id="30070-126"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30070-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30070-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30070-128">已淘汰的介面</span><span class="sxs-lookup"><span data-stu-id="30070-128">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
