---
title: DownloadCollection. removeItem 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 RemoveItem 方法會從下載集合中移除下載專案。
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- removeItem 方法 Windows Media Player
- removeItem 方法 Windows Media Player，DownloadCollection 類別
- DownloadCollection 類別 Windows Media Player，removeItem 方法
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991029"
---
# <a name="downloadcollectionremoveitem-method"></a><span data-ttu-id="aa5ad-108">DownloadCollection. removeItem 方法</span><span class="sxs-lookup"><span data-stu-id="aa5ad-108">DownloadCollection.removeItem method</span></span>

> [!Note]  
> <span data-ttu-id="aa5ad-109">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="aa5ad-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="aa5ad-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="aa5ad-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="aa5ad-111">**RemoveItem** 方法會從下載集合中移除下載專案。</span><span class="sxs-lookup"><span data-stu-id="aa5ad-111">The **removeItem** method removes a download item from a download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5ad-112">語法</span><span class="sxs-lookup"><span data-stu-id="aa5ad-112">Syntax</span></span>


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a><span data-ttu-id="aa5ad-113">參數</span><span class="sxs-lookup"><span data-stu-id="aa5ad-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa5ad-114">*itemID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa5ad-114">*itemID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5ad-115">**數值** (**long**) 指定要移除之 **DownloadItem** 的索引。</span><span class="sxs-lookup"><span data-stu-id="aa5ad-115">**Number** (**long**) specifying the index of the **DownloadItem** to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa5ad-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa5ad-116">Return value</span></span>

<span data-ttu-id="aa5ad-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa5ad-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa5ad-118">備註</span><span class="sxs-lookup"><span data-stu-id="aa5ad-118">Remarks</span></span>

<span data-ttu-id="aa5ad-119">如果 *itemID* 所表示的下載正在進行中，此方法會取消下載。</span><span class="sxs-lookup"><span data-stu-id="aa5ad-119">If the download represented by *itemID* is in progress, this method cancels the download.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5ad-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa5ad-120">Requirements</span></span>



| <span data-ttu-id="aa5ad-121">需求</span><span class="sxs-lookup"><span data-stu-id="aa5ad-121">Requirement</span></span> | <span data-ttu-id="aa5ad-122">值</span><span class="sxs-lookup"><span data-stu-id="aa5ad-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5ad-123">版本</span><span class="sxs-lookup"><span data-stu-id="aa5ad-123">Version</span></span><br/> | <span data-ttu-id="aa5ad-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="aa5ad-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="aa5ad-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5ad-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa5ad-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa5ad-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5ad-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa5ad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5ad-128">**DownloadCollection 專案**</span><span class="sxs-lookup"><span data-stu-id="aa5ad-128">**DownloadCollection.item**</span></span>](downloadcollection-item.md)
</dt> <dt>

[<span data-ttu-id="aa5ad-129">**DownloadCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="aa5ad-129">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





