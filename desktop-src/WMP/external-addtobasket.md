---
title: AddToBasket 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |AddToBasket 方法
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- addToBasket 方法 Windows Media Player
- addToBasket 方法 Windows Media Player、External 類別
- External class Windows Media Player，addToBasket 方法
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984130"
---
# <a name="externaladdtobasket-method"></a><span data-ttu-id="42012-107">AddToBasket 方法</span><span class="sxs-lookup"><span data-stu-id="42012-107">External.addToBasket method</span></span>

> [!Note]  
> <span data-ttu-id="42012-108">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="42012-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="42012-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="42012-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="42012-110">**AddToBasket** 方法會將媒體專案新增至 [清單] 窗格 (也稱為 Windows Media Player 中的購物籃) 。</span><span class="sxs-lookup"><span data-stu-id="42012-110">The **addToBasket** method adds media items to the list pane (also called the basket) in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="42012-111">語法</span><span class="sxs-lookup"><span data-stu-id="42012-111">Syntax</span></span>


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="42012-112">參數</span><span class="sxs-lookup"><span data-stu-id="42012-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42012-113">*ViewType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42012-113">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42012-114">**字串** ，指定要加入至 [清單] 窗格的專案類型。</span><span class="sxs-lookup"><span data-stu-id="42012-114">**String** that specifies the type of item being added to the list pane.</span></span> <span data-ttu-id="42012-115">呼叫端必須將此參數設定為下列其中一個連結 [庫位置常數](library-location-constants.md)：</span><span class="sxs-lookup"><span data-stu-id="42012-115">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="42012-116">CPListID</span><span class="sxs-lookup"><span data-stu-id="42012-116">CPListID</span></span>

<span data-ttu-id="42012-117">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="42012-117">CPTrackID</span></span>

<span data-ttu-id="42012-118">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="42012-118">CPAlbumID</span></span>

<span data-ttu-id="42012-119">CPArtist</span><span class="sxs-lookup"><span data-stu-id="42012-119">CPArtist</span></span>

<span data-ttu-id="42012-120">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="42012-120">CPGenreID</span></span>

<span data-ttu-id="42012-121">CPAlbumSubGenreID</span><span class="sxs-lookup"><span data-stu-id="42012-121">CPAlbumSubGenreID</span></span>

<span data-ttu-id="42012-122">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="42012-122">CPRadioID</span></span>

</dd> <dt>

<span data-ttu-id="42012-123">*Viewid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42012-123">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42012-124">**字串** ，包含要加入至清單窗格之專案的識別碼（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="42012-124">**String** containing the IDs, delimited by semicolons, of the items to be added to the list pane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42012-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="42012-125">Return value</span></span>

<span data-ttu-id="42012-126">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="42012-126">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="42012-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="42012-127">Requirements</span></span>



| <span data-ttu-id="42012-128">需求</span><span class="sxs-lookup"><span data-stu-id="42012-128">Requirement</span></span> | <span data-ttu-id="42012-129">值</span><span class="sxs-lookup"><span data-stu-id="42012-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42012-130">版本</span><span class="sxs-lookup"><span data-stu-id="42012-130">Version</span></span><br/> | <span data-ttu-id="42012-131">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="42012-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="42012-132">DLL</span><span class="sxs-lookup"><span data-stu-id="42012-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="42012-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42012-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42012-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42012-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42012-135">**類型1線上商店的 ExternalObject**</span><span class="sxs-lookup"><span data-stu-id="42012-135">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="42012-136">**BasketTitle**</span><span class="sxs-lookup"><span data-stu-id="42012-136">**External.basketTitle**</span></span>](external-baskettitle.md)
</dt> </dl>

 

 





