---
title: External. 購買方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 購買方法會起始一組媒體專案的購買。
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- 購買方法 Windows Media Player
- 購買方法 Windows Media Player，外部類別
- 外部類別 Windows Media Player，購買方法
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978743"
---
# <a name="externalbuy-method"></a><span data-ttu-id="cf21e-108">External. 購買方法</span><span class="sxs-lookup"><span data-stu-id="cf21e-108">External.buy method</span></span>

> [!Note]  
> <span data-ttu-id="cf21e-109">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="cf21e-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="cf21e-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="cf21e-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="cf21e-111">**購買** 方法會起始一組媒體專案的購買。</span><span class="sxs-lookup"><span data-stu-id="cf21e-111">The **buy** method initiates the purchase of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf21e-112">語法</span><span class="sxs-lookup"><span data-stu-id="cf21e-112">Syntax</span></span>


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="cf21e-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf21e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf21e-114">*ViewType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf21e-114">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf21e-115">**字串** ，指定要購買的專案類型。</span><span class="sxs-lookup"><span data-stu-id="cf21e-115">**String** that specifies the type of item to be purchased.</span></span> <span data-ttu-id="cf21e-116">呼叫端必須將此參數設定為下列其中一個連結 [庫位置常數](library-location-constants.md)：</span><span class="sxs-lookup"><span data-stu-id="cf21e-116">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="cf21e-117">CPListID</span><span class="sxs-lookup"><span data-stu-id="cf21e-117">CPListID</span></span>

<span data-ttu-id="cf21e-118">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="cf21e-118">CPTrackID</span></span>

<span data-ttu-id="cf21e-119">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="cf21e-119">CPAlbumID</span></span>

</dd> <dt>

<span data-ttu-id="cf21e-120">*Viewid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf21e-120">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf21e-121">**字串** ，包含要購買之專案的識別碼（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="cf21e-121">**String** containing the IDs, delimited by semicolons, of the items to be purchased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf21e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf21e-122">Return value</span></span>

<span data-ttu-id="cf21e-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cf21e-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf21e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf21e-124">Requirements</span></span>



| <span data-ttu-id="cf21e-125">需求</span><span class="sxs-lookup"><span data-stu-id="cf21e-125">Requirement</span></span> | <span data-ttu-id="cf21e-126">值</span><span class="sxs-lookup"><span data-stu-id="cf21e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf21e-127">版本</span><span class="sxs-lookup"><span data-stu-id="cf21e-127">Version</span></span><br/> | <span data-ttu-id="cf21e-128">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="cf21e-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="cf21e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cf21e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf21e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf21e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf21e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf21e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf21e-132">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="cf21e-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="cf21e-133">**External. 下載**</span><span class="sxs-lookup"><span data-stu-id="cf21e-133">**External.download**</span></span>](external-download.md)
</dt> <dt>

[<span data-ttu-id="cf21e-134">**IWMPContentPartner：：購買**</span><span class="sxs-lookup"><span data-stu-id="cf21e-134">**IWMPContentPartner::Buy**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[<span data-ttu-id="cf21e-135">**購買媒體內容**</span><span class="sxs-lookup"><span data-stu-id="cf21e-135">**Purchasing Media Content**</span></span>](purchasing-media-content.md)
</dt> </dl>

 

 





