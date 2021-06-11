---
description: 深入瞭解 IAMFilterData 介面，這會將篩選資訊轉換成封裝的二進位資料。 這個介面已被取代。
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
ms.openlocfilehash: 1e43e0f16ddfdee596f0dc6bd736ed86fc6fa37d
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989433"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="fba4f-104">IAMFilterData 介面</span><span class="sxs-lookup"><span data-stu-id="fba4f-104">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="fba4f-105">這個介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="fba4f-105">This interface has been deprecated.</span></span> <span data-ttu-id="fba4f-106">新的應用程式應該改用 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 介面。</span><span class="sxs-lookup"><span data-stu-id="fba4f-106">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="fba4f-107">`IAMFilterData`介面會將篩選資訊轉換成封裝的二進位資料，而這些資料可以儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="fba4f-107">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="fba4f-108">篩選對應程式物件會公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="fba4f-108">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="fba4f-109">成員</span><span class="sxs-lookup"><span data-stu-id="fba4f-109">Members</span></span>

<span data-ttu-id="fba4f-110">**IAMFilterData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fba4f-110">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fba4f-111">**IAMFilterData** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fba4f-111">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="fba4f-112">方法</span><span class="sxs-lookup"><span data-stu-id="fba4f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fba4f-113">方法</span><span class="sxs-lookup"><span data-stu-id="fba4f-113">Methods</span></span>

<span data-ttu-id="fba4f-114">**IAMFilterData** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fba4f-114">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="fba4f-115">方法</span><span class="sxs-lookup"><span data-stu-id="fba4f-115">Method</span></span>                                                     | <span data-ttu-id="fba4f-116">描述</span><span class="sxs-lookup"><span data-stu-id="fba4f-116">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="fba4f-117">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="fba4f-117">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="fba4f-118">建立篩選的二進位登錄資料。</span><span class="sxs-lookup"><span data-stu-id="fba4f-118">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="fba4f-119">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="fba4f-119">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="fba4f-120">解壓縮篩選的二進位登錄資料。</span><span class="sxs-lookup"><span data-stu-id="fba4f-120">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fba4f-121">備註</span><span class="sxs-lookup"><span data-stu-id="fba4f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fba4f-122">標頭 Fil \_ data .h 位於 Windows SDK 的對應工具 [範例](mapper-sample.md) 目錄中。</span><span class="sxs-lookup"><span data-stu-id="fba4f-122">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fba4f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fba4f-123">Requirements</span></span>



| <span data-ttu-id="fba4f-124">需求</span><span class="sxs-lookup"><span data-stu-id="fba4f-124">Requirement</span></span> | <span data-ttu-id="fba4f-125">值</span><span class="sxs-lookup"><span data-stu-id="fba4f-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fba4f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="fba4f-126">Header</span></span><br/> | <dl> <span data-ttu-id="fba4f-127"><dt>Fil \_ 資料。h</dt></span><span class="sxs-lookup"><span data-stu-id="fba4f-127"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba4f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fba4f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba4f-129">已淘汰的介面</span><span class="sxs-lookup"><span data-stu-id="fba4f-129">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
