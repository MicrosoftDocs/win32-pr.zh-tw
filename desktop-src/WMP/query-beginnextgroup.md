---
title: BeginNextGroup 方法
description: BeginNextGroup 方法會開始新的條件群組。 |BeginNextGroup 方法
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- beginNextGroup 方法 Windows Media Player
- beginNextGroup 方法 Windows Media Player，查詢類別
- 查詢類別 Windows Media Player，beginNextGroup 方法
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993595"
---
# <a name="querybeginnextgroup-method"></a><span data-ttu-id="afc2f-107">BeginNextGroup 方法</span><span class="sxs-lookup"><span data-stu-id="afc2f-107">Query.beginNextGroup method</span></span>

<span data-ttu-id="afc2f-108">**BeginNextGroup** 方法會開始新的條件群組。</span><span class="sxs-lookup"><span data-stu-id="afc2f-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc2f-109">語法</span><span class="sxs-lookup"><span data-stu-id="afc2f-109">Syntax</span></span>


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a><span data-ttu-id="afc2f-110">參數</span><span class="sxs-lookup"><span data-stu-id="afc2f-110">Parameters</span></span>

<span data-ttu-id="afc2f-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="afc2f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afc2f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="afc2f-112">Return value</span></span>

<span data-ttu-id="afc2f-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="afc2f-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc2f-114">備註</span><span class="sxs-lookup"><span data-stu-id="afc2f-114">Remarks</span></span>

<span data-ttu-id="afc2f-115">開始新的條件群組即表示您已完成目前的條件群組。</span><span class="sxs-lookup"><span data-stu-id="afc2f-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="afc2f-116">新的條件群組一律會使用或邏輯串連至先前的條件群組。</span><span class="sxs-lookup"><span data-stu-id="afc2f-116">The new condition group is always concatenated to the previous condition group using OR logic.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc2f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="afc2f-117">Requirements</span></span>



| <span data-ttu-id="afc2f-118">需求</span><span class="sxs-lookup"><span data-stu-id="afc2f-118">Requirement</span></span> | <span data-ttu-id="afc2f-119">值</span><span class="sxs-lookup"><span data-stu-id="afc2f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afc2f-120">版本</span><span class="sxs-lookup"><span data-stu-id="afc2f-120">Version</span></span><br/> | <span data-ttu-id="afc2f-121">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="afc2f-121">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="afc2f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="afc2f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="afc2f-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc2f-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc2f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afc2f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc2f-125">**MediaCollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="afc2f-125">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="afc2f-126">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="afc2f-126">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="afc2f-127">**MediaCollection.getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="afc2f-127">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="afc2f-128">**Query 物件**</span><span class="sxs-lookup"><span data-stu-id="afc2f-128">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="afc2f-129">**AddCondition**</span><span class="sxs-lookup"><span data-stu-id="afc2f-129">**Query.addCondition**</span></span>](query-addcondition.md)
</dt> </dl>

 

 





