---
title: DownloadItem 大小
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Size 屬性會抓取下載的大小。
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem 大小 Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997703"
---
# <a name="downloaditemsize"></a><span data-ttu-id="3b748-106">DownloadItem 大小</span><span class="sxs-lookup"><span data-stu-id="3b748-106">DownloadItem.size</span></span>

> [!Note]  
> <span data-ttu-id="3b748-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="3b748-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3b748-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="3b748-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3b748-109">**Size** 屬性會抓取下載的大小。</span><span class="sxs-lookup"><span data-stu-id="3b748-109">The **size** property retrieves the size of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b748-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b748-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a><span data-ttu-id="3b748-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="3b748-111">Possible Values</span></span>

<span data-ttu-id="3b748-112">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="3b748-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b748-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b748-113">Requirements</span></span>



| <span data-ttu-id="3b748-114">需求</span><span class="sxs-lookup"><span data-stu-id="3b748-114">Requirement</span></span> | <span data-ttu-id="3b748-115">值</span><span class="sxs-lookup"><span data-stu-id="3b748-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b748-116">版本</span><span class="sxs-lookup"><span data-stu-id="3b748-116">Version</span></span><br/> | <span data-ttu-id="3b748-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="3b748-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="3b748-118">DLL</span><span class="sxs-lookup"><span data-stu-id="3b748-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b748-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b748-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b748-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b748-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b748-121">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="3b748-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="3b748-122">**DownloadItem。進度**</span><span class="sxs-lookup"><span data-stu-id="3b748-122">**DownloadItem.progress**</span></span>](downloaditem-progress.md)
</dt> </dl>

 

 





