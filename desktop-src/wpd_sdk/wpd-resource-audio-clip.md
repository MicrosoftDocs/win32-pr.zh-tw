---
description: 指定物件的音訊剪輯。
ms.assetid: 24c15df0-4190-4c75-b89b-0c73d645c9ca
title: WPD_RESOURCE_AUDIO_CLIP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7013fb59670c92903f89509f720f7c597ef916fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978320"
---
# <a name="wpd_resource_audio_clip"></a><span data-ttu-id="18ba8-103">WPD \_ 資源 \_ 音訊 \_ 剪輯</span><span class="sxs-lookup"><span data-stu-id="18ba8-103">WPD\_RESOURCE\_AUDIO\_CLIP</span></span>

<span data-ttu-id="18ba8-104">指定物件的音訊剪輯。</span><span class="sxs-lookup"><span data-stu-id="18ba8-104">Specifies an audio clip for the object.</span></span>

<span data-ttu-id="18ba8-105">這種類型的資源必須支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="18ba8-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="18ba8-106">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="18ba8-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="18ba8-107">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="18ba8-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="18ba8-108">WPD \_ 音訊 \_ 位元速率</span><span class="sxs-lookup"><span data-stu-id="18ba8-108">WPD\_AUDIO\_BITRATE</span></span>](audio-properties.md)                                                             | <span data-ttu-id="18ba8-109">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ba8-109">Recommended.</span></span>                                           |
| [<span data-ttu-id="18ba8-110">WPD \_ 音訊 \_ 頻道 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="18ba8-110">WPD\_AUDIO\_CHANNEL\_COUNT</span></span>](audio-properties.md)                                                | <span data-ttu-id="18ba8-111">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ba8-111">Optional.</span></span>                                              |
| [<span data-ttu-id="18ba8-112">WPD \_ 音訊 \_ 格式 \_ 代碼</span><span class="sxs-lookup"><span data-stu-id="18ba8-112">WPD\_AUDIO\_FORMAT\_CODE</span></span>](audio-properties.md)                                                    | <span data-ttu-id="18ba8-113">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ba8-113">Optional.</span></span>                                              |
| [<span data-ttu-id="18ba8-114">WPD \_ 音訊 \_ 位 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="18ba8-114">WPD\_AUDIO\_BIT\_DEPTH</span></span>](audio-properties.md)                                                        | <span data-ttu-id="18ba8-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ba8-115">Optional.</span></span>                                              |
| [<span data-ttu-id="18ba8-116">WPD \_ 音訊 \_ 區塊 \_ 對齊</span><span class="sxs-lookup"><span data-stu-id="18ba8-116">WPD\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](audio-properties.md)                                            | <span data-ttu-id="18ba8-117">選擇性。</span><span class="sxs-lookup"><span data-stu-id="18ba8-117">Optional.</span></span>                                              |
| [<span data-ttu-id="18ba8-118">WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ba8-118">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="18ba8-119">必要。</span><span class="sxs-lookup"><span data-stu-id="18ba8-119">Required.</span></span>                                              |
| [<span data-ttu-id="18ba8-120">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="18ba8-120">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="18ba8-121">如果用戶端可以讀取此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ba8-121">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="18ba8-122">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="18ba8-122">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="18ba8-123">如果用戶端可以寫入此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ba8-123">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="18ba8-124">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="18ba8-124">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="18ba8-125">如果用戶端可以刪除此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ba8-125">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="18ba8-126">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ba8-126">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="18ba8-127">如果用戶端擁有資源的讀取權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ba8-127">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="18ba8-128">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 寫入 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="18ba8-128">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="18ba8-129">如果用戶端具有資源的寫入權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="18ba8-129">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="18ba8-130">WPD \_ 資源 \_ 屬性 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="18ba8-130">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="18ba8-131">必要。</span><span class="sxs-lookup"><span data-stu-id="18ba8-131">Required.</span></span>                                              |
| [<span data-ttu-id="18ba8-132">WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="18ba8-132">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="18ba8-133">建議使用。</span><span class="sxs-lookup"><span data-stu-id="18ba8-133">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="18ba8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18ba8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ba8-135">**資源的需求**</span><span class="sxs-lookup"><span data-stu-id="18ba8-135">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



