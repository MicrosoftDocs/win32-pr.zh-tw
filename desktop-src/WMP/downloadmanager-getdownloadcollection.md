---
title: DownloadManager. getDownloadCollection 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 GetDownloadCollection 方法會抓取指定的下載集合。
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- getDownloadCollection 方法 Windows Media Player
- getDownloadCollection 方法 Windows Media Player，DownloadManager 類別
- DownloadManager 類別 Windows Media Player，getDownloadCollection 方法
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000002"
---
# <a name="downloadmanagergetdownloadcollection-method"></a><span data-ttu-id="84f29-108">DownloadManager. getDownloadCollection 方法</span><span class="sxs-lookup"><span data-stu-id="84f29-108">DownloadManager.getDownloadCollection method</span></span>

> [!Note]  
> <span data-ttu-id="84f29-109">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="84f29-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="84f29-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="84f29-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="84f29-111">**GetDownloadCollection** 方法會抓取指定的下載集合。</span><span class="sxs-lookup"><span data-stu-id="84f29-111">The **getDownloadCollection** method retrieves the specified download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f29-112">語法</span><span class="sxs-lookup"><span data-stu-id="84f29-112">Syntax</span></span>


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a><span data-ttu-id="84f29-113">參數</span><span class="sxs-lookup"><span data-stu-id="84f29-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f29-114">*collectionId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84f29-114">*collectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f29-115">**Number** (**long**) 指定要抓取之下載集合的識別碼。</span><span class="sxs-lookup"><span data-stu-id="84f29-115">**Number** (**long**) specifying the ID of the download collection to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f29-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="84f29-116">Return value</span></span>

<span data-ttu-id="84f29-117">這個方法會傳回 **DownloadCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="84f29-117">This method returns a **DownloadCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f29-118">備註</span><span class="sxs-lookup"><span data-stu-id="84f29-118">Remarks</span></span>

<span data-ttu-id="84f29-119">您必須先呼叫 *DownloadManager*。**createDownloadCollection** 建立新的集合，並取出其識別碼值。</span><span class="sxs-lookup"><span data-stu-id="84f29-119">You must first call *DownloadManager*.**createDownloadCollection** to create a new collection and retrieve its ID value.</span></span>

<span data-ttu-id="84f29-120">現有的下載集合可能包含已標示為已取消的專案。</span><span class="sxs-lookup"><span data-stu-id="84f29-120">An existing download collection may contain items that have been marked as cancelled.</span></span>

<span data-ttu-id="84f29-121">未在前一個會話中完成的即時下載專案，將不會被視為集合的一部分。</span><span class="sxs-lookup"><span data-stu-id="84f29-121">Real-time download items not completed in a prior session are not retrieved as part of the collection.</span></span> <span data-ttu-id="84f29-122">在目前會話之前完成的背景下載會保留在下載集合中，直到移除為止。</span><span class="sxs-lookup"><span data-stu-id="84f29-122">Background downloads that were completed prior to the current session remain in the download collection until removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f29-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="84f29-123">Requirements</span></span>



| <span data-ttu-id="84f29-124">需求</span><span class="sxs-lookup"><span data-stu-id="84f29-124">Requirement</span></span> | <span data-ttu-id="84f29-125">值</span><span class="sxs-lookup"><span data-stu-id="84f29-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84f29-126">版本</span><span class="sxs-lookup"><span data-stu-id="84f29-126">Version</span></span><br/> | <span data-ttu-id="84f29-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="84f29-127">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="84f29-128">DLL</span><span class="sxs-lookup"><span data-stu-id="84f29-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="84f29-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f29-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f29-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84f29-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f29-131">**DownloadManager 物件**</span><span class="sxs-lookup"><span data-stu-id="84f29-131">**DownloadManager Object**</span></span>](downloadmanager-object.md)
</dt> <dt>

[<span data-ttu-id="84f29-132">**DownloadManager.createDownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="84f29-132">**DownloadManager. createDownloadCollection**</span></span>](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="84f29-133">**DownloadCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="84f29-133">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





