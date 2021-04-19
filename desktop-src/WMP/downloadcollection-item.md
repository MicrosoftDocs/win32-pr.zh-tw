---
title: DownloadCollection 專案方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Item 方法會抓取暫止的下載物件。
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，DownloadCollection 類別
- DownloadCollection 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999461"
---
# <a name="downloadcollectionitem-method"></a><span data-ttu-id="363f5-108">DownloadCollection 專案方法</span><span class="sxs-lookup"><span data-stu-id="363f5-108">DownloadCollection.item method</span></span>

> [!Note]  
> <span data-ttu-id="363f5-109">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="363f5-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="363f5-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="363f5-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="363f5-111">**Item** 方法會抓取暫止的下載物件。</span><span class="sxs-lookup"><span data-stu-id="363f5-111">The **item** method retrieves a pending download object.</span></span>

## <a name="syntax"></a><span data-ttu-id="363f5-112">語法</span><span class="sxs-lookup"><span data-stu-id="363f5-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a><span data-ttu-id="363f5-113">參數</span><span class="sxs-lookup"><span data-stu-id="363f5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="363f5-114">*itemId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="363f5-114">*itemId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363f5-115">**(** **long**) 指定要取出的 **DownloadItem** 索引。</span><span class="sxs-lookup"><span data-stu-id="363f5-115">**Number** (**long**) specifying the index of the **DownloadItem** to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="363f5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="363f5-116">Return value</span></span>

<span data-ttu-id="363f5-117">這個方法會傳回 **DownloadItem** 物件。</span><span class="sxs-lookup"><span data-stu-id="363f5-117">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="363f5-118">備註</span><span class="sxs-lookup"><span data-stu-id="363f5-118">Remarks</span></span>

<span data-ttu-id="363f5-119">*ItemID* 值以零為基底。</span><span class="sxs-lookup"><span data-stu-id="363f5-119">The *itemID* value is zero-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="363f5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="363f5-120">Requirements</span></span>



| <span data-ttu-id="363f5-121">需求</span><span class="sxs-lookup"><span data-stu-id="363f5-121">Requirement</span></span> | <span data-ttu-id="363f5-122">值</span><span class="sxs-lookup"><span data-stu-id="363f5-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="363f5-123">版本</span><span class="sxs-lookup"><span data-stu-id="363f5-123">Version</span></span><br/> | <span data-ttu-id="363f5-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="363f5-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="363f5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="363f5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="363f5-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="363f5-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363f5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="363f5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363f5-128">**DownloadCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="363f5-128">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="363f5-129">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="363f5-129">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





