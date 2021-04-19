---
title: DownloadItem. cancel 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Cancel 方法會取消下載。
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- cancel 方法 Windows Media Player
- cancel 方法 Windows Media Player，DownloadItem 類別
- DownloadItem 類別 Windows Media Player，cancel 方法
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991161"
---
# <a name="downloaditemcancel-method"></a><span data-ttu-id="48d88-108">DownloadItem. cancel 方法</span><span class="sxs-lookup"><span data-stu-id="48d88-108">DownloadItem.cancel method</span></span>

> [!Note]  
> <span data-ttu-id="48d88-109">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="48d88-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="48d88-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="48d88-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="48d88-111">**Cancel** 方法會取消下載。</span><span class="sxs-lookup"><span data-stu-id="48d88-111">The **cancel** method cancels the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d88-112">語法</span><span class="sxs-lookup"><span data-stu-id="48d88-112">Syntax</span></span>


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a><span data-ttu-id="48d88-113">參數</span><span class="sxs-lookup"><span data-stu-id="48d88-113">Parameters</span></span>

<span data-ttu-id="48d88-114">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="48d88-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48d88-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="48d88-115">Return value</span></span>

<span data-ttu-id="48d88-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="48d88-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48d88-117">備註</span><span class="sxs-lookup"><span data-stu-id="48d88-117">Remarks</span></span>

<span data-ttu-id="48d88-118">取消的專案不會從下載集合中移除。</span><span class="sxs-lookup"><span data-stu-id="48d88-118">Cancelled items are not removed from the download collection.</span></span> <span data-ttu-id="48d88-119">取消的專案會傳回 **downloadState** 值 4 (取消的) 。</span><span class="sxs-lookup"><span data-stu-id="48d88-119">Cancelled items return a **downloadState** value of 4 (canceled).</span></span>

## <a name="requirements"></a><span data-ttu-id="48d88-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="48d88-120">Requirements</span></span>



| <span data-ttu-id="48d88-121">需求</span><span class="sxs-lookup"><span data-stu-id="48d88-121">Requirement</span></span> | <span data-ttu-id="48d88-122">值</span><span class="sxs-lookup"><span data-stu-id="48d88-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48d88-123">版本</span><span class="sxs-lookup"><span data-stu-id="48d88-123">Version</span></span><br/> | <span data-ttu-id="48d88-124">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="48d88-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="48d88-125">DLL</span><span class="sxs-lookup"><span data-stu-id="48d88-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="48d88-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48d88-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48d88-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48d88-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d88-128">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="48d88-128">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="48d88-129">**DownloadItem.downloadState**</span><span class="sxs-lookup"><span data-stu-id="48d88-129">**DownloadItem.downloadState**</span></span>](downloaditem-downloadstate.md)
</dt> </dl>

 

 





