---
title: DownloadItem。類型
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Type 屬性會抓取下載的型別。
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem 輸入 Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987029"
---
# <a name="downloaditemtype"></a><span data-ttu-id="3723d-106">DownloadItem。類型</span><span class="sxs-lookup"><span data-stu-id="3723d-106">DownloadItem.type</span></span>

> [!Note]  
> <span data-ttu-id="3723d-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="3723d-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3723d-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="3723d-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3723d-109">**Type** 屬性會抓取下載的型別。</span><span class="sxs-lookup"><span data-stu-id="3723d-109">The **type** property retrieves the type of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="3723d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3723d-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a><span data-ttu-id="3723d-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="3723d-111">Possible Values</span></span>

<span data-ttu-id="3723d-112">這個屬性是唯讀 **字串** ，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3723d-112">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="3723d-113">值</span><span class="sxs-lookup"><span data-stu-id="3723d-113">Value</span></span>      | <span data-ttu-id="3723d-114">描述</span><span class="sxs-lookup"><span data-stu-id="3723d-114">Description</span></span>                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3723d-115">背景資訊</span><span class="sxs-lookup"><span data-stu-id="3723d-115">background</span></span> | <span data-ttu-id="3723d-116">僅 (Windows XP。 ) 下載會在處理器時間變成可用時，作為背景程式進行。</span><span class="sxs-lookup"><span data-stu-id="3723d-116">(Windows XP only.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="3723d-117">即使在 Windows Media Player 或 Windows XP 關閉時，下載狀態仍會保存。</span><span class="sxs-lookup"><span data-stu-id="3723d-117">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="3723d-118">即時</span><span class="sxs-lookup"><span data-stu-id="3723d-118">real time</span></span>  | <span data-ttu-id="3723d-119"> (所有支援的作業系統。 ) 下載會一次完成。</span><span class="sxs-lookup"><span data-stu-id="3723d-119">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="3723d-120">會話之間不會保存任何下載狀態。</span><span class="sxs-lookup"><span data-stu-id="3723d-120">No download states persist between sessions.</span></span>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="3723d-121">備註</span><span class="sxs-lookup"><span data-stu-id="3723d-121">Remarks</span></span>

<span data-ttu-id="3723d-122">每種類型的下載都有其優點和缺點。</span><span class="sxs-lookup"><span data-stu-id="3723d-122">Each type of download has advantages and disadvantages.</span></span> <span data-ttu-id="3723d-123">背景下載可讓使用者繼續進行其他工作，甚至重新開機 Windows 而不需要取消下載，但要花更多時間才能完成下載，而且只支援 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="3723d-123">Background downloading allows the user to proceed to other tasks and even restart Windows without cancelling the download, but takes more time overall to complete the download and is only supported for Windows XP.</span></span> <span data-ttu-id="3723d-124">即時下載需要較少的時間才能完成，但會要求使用者在關閉 Windows Media Player 之前完成下載。</span><span class="sxs-lookup"><span data-stu-id="3723d-124">Real-time downloading takes less time to complete, but requires the user to finish all downloading before closing Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="3723d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3723d-125">Requirements</span></span>



| <span data-ttu-id="3723d-126">需求</span><span class="sxs-lookup"><span data-stu-id="3723d-126">Requirement</span></span> | <span data-ttu-id="3723d-127">值</span><span class="sxs-lookup"><span data-stu-id="3723d-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3723d-128">版本</span><span class="sxs-lookup"><span data-stu-id="3723d-128">Version</span></span><br/> | <span data-ttu-id="3723d-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="3723d-129">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="3723d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3723d-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="3723d-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3723d-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3723d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3723d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3723d-133">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="3723d-133">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





