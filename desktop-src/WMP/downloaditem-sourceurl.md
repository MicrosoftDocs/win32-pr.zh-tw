---
title: DownloadItem.sourceURL
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 SourceURL 屬性會抓取下載的來源 URL。
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- DownloadItem. sourceURL Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001563"
---
# <a name="downloaditemsourceurl"></a><span data-ttu-id="ede7e-106">DownloadItem.sourceURL</span><span class="sxs-lookup"><span data-stu-id="ede7e-106">DownloadItem.sourceURL</span></span>

> [!Note]  
> <span data-ttu-id="ede7e-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="ede7e-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ede7e-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="ede7e-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ede7e-109">**SourceURL** 屬性會抓取下載的來源 URL。</span><span class="sxs-lookup"><span data-stu-id="ede7e-109">The **sourceURL** property retrieves the source URL of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede7e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ede7e-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a><span data-ttu-id="ede7e-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="ede7e-111">Possible Values</span></span>

<span data-ttu-id="ede7e-112">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="ede7e-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede7e-113">備註</span><span class="sxs-lookup"><span data-stu-id="ede7e-113">Remarks</span></span>

<span data-ttu-id="ede7e-114">只有下列數位媒體格式可供下載：</span><span class="sxs-lookup"><span data-stu-id="ede7e-114">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="ede7e-115">進階系統格式 (ASF)</span><span class="sxs-lookup"><span data-stu-id="ede7e-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="ede7e-116">MP3</span><span class="sxs-lookup"><span data-stu-id="ede7e-116">MP3</span></span>
-   <span data-ttu-id="ede7e-117">Windows Media 音訊 (WMA)</span><span class="sxs-lookup"><span data-stu-id="ede7e-117">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="ede7e-118">Windows Media 視訊 (WMV)</span><span class="sxs-lookup"><span data-stu-id="ede7e-118">Windows Media Video (WMV)</span></span>

## <a name="requirements"></a><span data-ttu-id="ede7e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ede7e-119">Requirements</span></span>



| <span data-ttu-id="ede7e-120">需求</span><span class="sxs-lookup"><span data-stu-id="ede7e-120">Requirement</span></span> | <span data-ttu-id="ede7e-121">值</span><span class="sxs-lookup"><span data-stu-id="ede7e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ede7e-122">版本</span><span class="sxs-lookup"><span data-stu-id="ede7e-122">Version</span></span><br/> | <span data-ttu-id="ede7e-123">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="ede7e-123">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ede7e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ede7e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="ede7e-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ede7e-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede7e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ede7e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede7e-127">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="ede7e-127">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





