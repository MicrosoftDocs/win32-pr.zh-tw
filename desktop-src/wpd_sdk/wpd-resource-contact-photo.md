---
description: 指定代表 contact 物件中所參考之個別相片的影像。
ms.assetid: e26487d8-cd21-4d4a-ba68-ae915eff1304
title: WPD_RESOURCE_CONTACT_PHOTO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ee8a283492eba61989eca3f3bfa96bdba2f0ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972201"
---
# <a name="wpd_resource_contact_photo"></a><span data-ttu-id="2c143-103">WPD \_ 資源 \_ 連絡人 \_ 相片</span><span class="sxs-lookup"><span data-stu-id="2c143-103">WPD\_RESOURCE\_CONTACT\_PHOTO</span></span>

<span data-ttu-id="2c143-104">指定代表 contact 物件中所參考之個別相片的影像。</span><span class="sxs-lookup"><span data-stu-id="2c143-104">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>

<span data-ttu-id="2c143-105">這種類型的資源必須支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2c143-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="2c143-106">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="2c143-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="2c143-107">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="2c143-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="2c143-108">WPD \_ 媒體 \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="2c143-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="2c143-109">必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-109">Required.</span></span>                                              |
| [<span data-ttu-id="2c143-110">WPD \_ 媒體 \_ 高度</span><span class="sxs-lookup"><span data-stu-id="2c143-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="2c143-111">必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-111">Required.</span></span>                                              |
| [<span data-ttu-id="2c143-112">WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2c143-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="2c143-113">必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-113">Required.</span></span>                                              |
| [<span data-ttu-id="2c143-114">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="2c143-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="2c143-115">如果用戶端可以讀取此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="2c143-116">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="2c143-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="2c143-117">如果用戶端可以寫入此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="2c143-118">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="2c143-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="2c143-119">如果用戶端可以刪除此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="2c143-120">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2c143-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="2c143-121">如果用戶端擁有資源的讀取權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="2c143-122">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 寫入 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2c143-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="2c143-123">如果用戶端具有資源的寫入權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="2c143-124">WPD \_ 資源 \_ 屬性 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="2c143-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="2c143-125">必要。</span><span class="sxs-lookup"><span data-stu-id="2c143-125">Required.</span></span>                                              |
| [<span data-ttu-id="2c143-126">WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="2c143-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="2c143-127">建議使用。</span><span class="sxs-lookup"><span data-stu-id="2c143-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="2c143-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c143-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c143-129">**資源的需求**</span><span class="sxs-lookup"><span data-stu-id="2c143-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



