---
title: DownloadItem。進度
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 進度屬性會取得下載的進度（以位元組為單位）。
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- DownloadItem 進度 Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994636"
---
# <a name="downloaditemprogress"></a><span data-ttu-id="4cc02-106">DownloadItem。進度</span><span class="sxs-lookup"><span data-stu-id="4cc02-106">DownloadItem.progress</span></span>

> [!Note]  
> <span data-ttu-id="4cc02-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="4cc02-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4cc02-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="4cc02-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4cc02-109">**進度** 屬性會取得下載的進度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4cc02-109">The **progress** property retrieves the progress of the download in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc02-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cc02-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a><span data-ttu-id="4cc02-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="4cc02-111">Possible Values</span></span>

<span data-ttu-id="4cc02-112">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="4cc02-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc02-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cc02-113">Requirements</span></span>



| <span data-ttu-id="4cc02-114">需求</span><span class="sxs-lookup"><span data-stu-id="4cc02-114">Requirement</span></span> | <span data-ttu-id="4cc02-115">值</span><span class="sxs-lookup"><span data-stu-id="4cc02-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc02-116">版本</span><span class="sxs-lookup"><span data-stu-id="4cc02-116">Version</span></span><br/> | <span data-ttu-id="4cc02-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4cc02-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="4cc02-118">DLL</span><span class="sxs-lookup"><span data-stu-id="4cc02-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="4cc02-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cc02-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc02-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cc02-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc02-121">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="4cc02-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="4cc02-122">**DownloadItem 大小**</span><span class="sxs-lookup"><span data-stu-id="4cc02-122">**DownloadItem.size**</span></span>](downloaditem-size.md)
</dt> </dl>

 

 





