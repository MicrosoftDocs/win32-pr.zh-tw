---
description: 指定 Windows 可攜式裝置未以其他方式定義的資源類型。
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112832"
---
# <a name="wpd_resource_generic"></a><span data-ttu-id="a2d5c-103">WPD \_ 資源 \_ 泛型</span><span class="sxs-lookup"><span data-stu-id="a2d5c-103">WPD\_RESOURCE\_GENERIC</span></span>

<span data-ttu-id="a2d5c-104">指定 Windows 可攜式裝置未以其他方式定義的資源類型。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-104">Specifies a resource type not otherwise defined by Windows Portable Devices.</span></span> <span data-ttu-id="a2d5c-105">您可以定義自己的自訂資源，以支援任何自訂或 Windows 便攜裝置定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-105">You can define your own custom resources that support any custom or Windows Portable Devices-defined attributes.</span></span> <span data-ttu-id="a2d5c-106">不過，您所建立的任何資源都必須支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-106">However, any resource you create must support the following attributes.</span></span>



| <span data-ttu-id="a2d5c-107">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="a2d5c-107">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="a2d5c-108">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="a2d5c-108">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="a2d5c-109">WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="a2d5c-109">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="a2d5c-110">必要。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-110">Required.</span></span>                                              |
| [<span data-ttu-id="a2d5c-111">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="a2d5c-111">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="a2d5c-112">如果用戶端可以讀取此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-112">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="a2d5c-113">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="a2d5c-113">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="a2d5c-114">如果用戶端可以寫入此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-114">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="a2d5c-115">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="a2d5c-115">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="a2d5c-116">如果用戶端可以刪除此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-116">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="a2d5c-117">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="a2d5c-117">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="a2d5c-118">如果用戶端擁有資源的讀取權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-118">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="a2d5c-119">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 寫入 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="a2d5c-119">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="a2d5c-120">如果用戶端具有資源的寫入權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-120">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="a2d5c-121">WPD \_ 資源 \_ 屬性 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="a2d5c-121">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="a2d5c-122">必要。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-122">Required.</span></span>                                              |
| [<span data-ttu-id="a2d5c-123">WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="a2d5c-123">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="a2d5c-124">建議使用。</span><span class="sxs-lookup"><span data-stu-id="a2d5c-124">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="a2d5c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2d5c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d5c-126">**資源的需求**</span><span class="sxs-lookup"><span data-stu-id="a2d5c-126">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



