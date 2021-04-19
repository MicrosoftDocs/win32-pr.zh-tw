---
title: DownloadCollection 計數
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Count 屬性會抓取集合中的暫止下載數目。
ms.assetid: 8f9245aa-6d92-4dd3-9b45-97ee37de680d
keywords:
- DownloadCollection Windows Media Player 計數
topic_type:
- apiref
api_name:
- DownloadCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95f161143cf599dcfbc71b2e55764009ec5d4e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995673"
---
# <a name="downloadcollectioncount"></a><span data-ttu-id="d4cb1-106">DownloadCollection 計數</span><span class="sxs-lookup"><span data-stu-id="d4cb1-106">DownloadCollection.count</span></span>

> [!Note]  
> <span data-ttu-id="d4cb1-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="d4cb1-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d4cb1-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="d4cb1-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d4cb1-109">**Count** 屬性會抓取集合中的暫止下載數目。</span><span class="sxs-lookup"><span data-stu-id="d4cb1-109">The **count** property retrieves the number of pending downloads in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4cb1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4cb1-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).count
      
```

## <a name="possible-values"></a><span data-ttu-id="d4cb1-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="d4cb1-111">Possible Values</span></span>

<span data-ttu-id="d4cb1-112">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="d4cb1-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4cb1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4cb1-113">Requirements</span></span>



| <span data-ttu-id="d4cb1-114">需求</span><span class="sxs-lookup"><span data-stu-id="d4cb1-114">Requirement</span></span> | <span data-ttu-id="d4cb1-115">值</span><span class="sxs-lookup"><span data-stu-id="d4cb1-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cb1-116">版本</span><span class="sxs-lookup"><span data-stu-id="d4cb1-116">Version</span></span><br/> | <span data-ttu-id="d4cb1-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d4cb1-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="d4cb1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d4cb1-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4cb1-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4cb1-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4cb1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4cb1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4cb1-121">**DownloadCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="d4cb1-121">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





