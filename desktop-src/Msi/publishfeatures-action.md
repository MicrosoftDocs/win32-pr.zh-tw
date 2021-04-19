---
description: PublishFeatures 動作會將每個功能的狀態寫入系統登錄。
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: PublishFeatures 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986921"
---
# <a name="publishfeatures-action"></a><span data-ttu-id="bf0de-103">PublishFeatures 動作</span><span class="sxs-lookup"><span data-stu-id="bf0de-103">PublishFeatures Action</span></span>

<span data-ttu-id="bf0de-104">PublishFeatures 動作會將每個功能的狀態寫入系統登錄。</span><span class="sxs-lookup"><span data-stu-id="bf0de-104">The PublishFeatures action writes each feature's state into the system registry.</span></span> <span data-ttu-id="bf0de-105">功能狀態可能是不存在、已公告或已安裝。</span><span class="sxs-lookup"><span data-stu-id="bf0de-105">The feature state may be either absent, advertised, or installed.</span></span> <span data-ttu-id="bf0de-106">PublishFeatures 動作也會針對每個已安裝的功能，將功能元件對應寫入系統登錄。</span><span class="sxs-lookup"><span data-stu-id="bf0de-106">The PublishFeatures action also writes the feature-component mapping into the system registry for each installed feature.</span></span>

<span data-ttu-id="bf0de-107">PublishFeatures 動作會查詢 [FeatureComponents 資料表](featurecomponents-table.md)、 [功能資料表](feature-table.md)和 [元件資料表](component-table.md)。</span><span class="sxs-lookup"><span data-stu-id="bf0de-107">The PublishFeatures action queries the [FeatureComponents table](featurecomponents-table.md), [Feature table](feature-table.md), and [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bf0de-108">順序限制</span><span class="sxs-lookup"><span data-stu-id="bf0de-108">Sequence Restrictions</span></span>

<span data-ttu-id="bf0de-109">PublishFeatures 動作必須在 [PublishProduct](publishproduct-action.md)之前。</span><span class="sxs-lookup"><span data-stu-id="bf0de-109">The PublishFeatures action must come before [PublishProduct](publishproduct-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bf0de-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="bf0de-110">ActionData Messages</span></span>



| <span data-ttu-id="bf0de-111">欄位</span><span class="sxs-lookup"><span data-stu-id="bf0de-111">Field</span></span> | <span data-ttu-id="bf0de-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="bf0de-112">Description of action data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="bf0de-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="bf0de-113">\[1\]</span></span> | <span data-ttu-id="bf0de-114">已公告功能的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf0de-114">Identifier of advertised feature.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bf0de-115">備註</span><span class="sxs-lookup"><span data-stu-id="bf0de-115">Remarks</span></span>

<span data-ttu-id="bf0de-116">PublishFeatures 動作會發佈所有已選取要公告或安裝的功能組合。</span><span class="sxs-lookup"><span data-stu-id="bf0de-116">The PublishFeatures action publishes the composition of all features that are selected to be advertised or installed.</span></span>

 

 



