---
title: DownloadItem.downloadState
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 DownloadState 屬性會捕獲下載的狀態。
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem. downloadState Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997749"
---
# <a name="downloaditemdownloadstate"></a><span data-ttu-id="8d0ee-106">DownloadItem.downloadState</span><span class="sxs-lookup"><span data-stu-id="8d0ee-106">DownloadItem.downloadState</span></span>

> [!Note]  
> <span data-ttu-id="8d0ee-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="8d0ee-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8d0ee-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="8d0ee-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8d0ee-109">**DownloadState** 屬性會捕獲下載的狀態。</span><span class="sxs-lookup"><span data-stu-id="8d0ee-109">The **downloadState** property retrieves the state of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0ee-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d0ee-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a><span data-ttu-id="8d0ee-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="8d0ee-111">Possible Values</span></span>

<span data-ttu-id="8d0ee-112">這個屬性是唯讀的 **數位** ，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8d0ee-112">This property is a read-only **Number** containing one of the following values.</span></span>



| <span data-ttu-id="8d0ee-113">值</span><span class="sxs-lookup"><span data-stu-id="8d0ee-113">Value</span></span> | <span data-ttu-id="8d0ee-114">描述</span><span class="sxs-lookup"><span data-stu-id="8d0ee-114">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="8d0ee-115">0</span><span class="sxs-lookup"><span data-stu-id="8d0ee-115">0</span></span>     | <span data-ttu-id="8d0ee-116">正在下載</span><span class="sxs-lookup"><span data-stu-id="8d0ee-116">Downloading</span></span> |
| <span data-ttu-id="8d0ee-117">1</span><span class="sxs-lookup"><span data-stu-id="8d0ee-117">1</span></span>     | <span data-ttu-id="8d0ee-118">已暫停</span><span class="sxs-lookup"><span data-stu-id="8d0ee-118">Paused</span></span>      |
| <span data-ttu-id="8d0ee-119">2</span><span class="sxs-lookup"><span data-stu-id="8d0ee-119">2</span></span>     | <span data-ttu-id="8d0ee-120">Processing</span><span class="sxs-lookup"><span data-stu-id="8d0ee-120">Processing</span></span>  |
| <span data-ttu-id="8d0ee-121">3</span><span class="sxs-lookup"><span data-stu-id="8d0ee-121">3</span></span>     | <span data-ttu-id="8d0ee-122">已完成</span><span class="sxs-lookup"><span data-stu-id="8d0ee-122">Completed</span></span>   |
| <span data-ttu-id="8d0ee-123">4</span><span class="sxs-lookup"><span data-stu-id="8d0ee-123">4</span></span>     | <span data-ttu-id="8d0ee-124">已取消</span><span class="sxs-lookup"><span data-stu-id="8d0ee-124">Canceled</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="8d0ee-125">備註</span><span class="sxs-lookup"><span data-stu-id="8d0ee-125">Remarks</span></span>

<span data-ttu-id="8d0ee-126">下載狀態可能會以任何順序發生。</span><span class="sxs-lookup"><span data-stu-id="8d0ee-126">Download states can occur in any order.</span></span> <span data-ttu-id="8d0ee-127">請勿撰寫相依于任何特定下載狀態之出現位置的程式碼。</span><span class="sxs-lookup"><span data-stu-id="8d0ee-127">Do not write code that depends on the occurrence of any particular download state.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d0ee-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d0ee-128">Requirements</span></span>



| <span data-ttu-id="8d0ee-129">需求</span><span class="sxs-lookup"><span data-stu-id="8d0ee-129">Requirement</span></span> | <span data-ttu-id="8d0ee-130">值</span><span class="sxs-lookup"><span data-stu-id="8d0ee-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0ee-131">版本</span><span class="sxs-lookup"><span data-stu-id="8d0ee-131">Version</span></span><br/> | <span data-ttu-id="8d0ee-132">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8d0ee-132">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="8d0ee-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8d0ee-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d0ee-134"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d0ee-134"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d0ee-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d0ee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d0ee-136">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="8d0ee-136">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





