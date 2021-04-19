---
description: ProductLanguage 屬性必須更新為新語言 (LANGID) 的數值語言識別項。
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: 更新 ProductLanguage 和 ProductCode 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979389"
---
# <a name="updating-productlanguage-and-productcode-properties"></a><span data-ttu-id="fa90c-103">更新 ProductLanguage 和 ProductCode 屬性</span><span class="sxs-lookup"><span data-stu-id="fa90c-103">Updating ProductLanguage and ProductCode Properties</span></span>

<span data-ttu-id="fa90c-104">[**ProductLanguage**](productlanguage.md)屬性必須更新為新語言 (LANGID) 的數值語言識別項。</span><span class="sxs-lookup"><span data-stu-id="fa90c-104">The [**ProductLanguage**](productlanguage.md) property must be updated to the numeric language identifier (LANGID) for the new language.</span></span> <span data-ttu-id="fa90c-105">在當地語系化範例的情況下， **ProductLanguage** 屬性的值必須從 LANGID for 英文 (1033) 變更為 [屬性資料表](property-table.md)中法文 (1036) 的 LANGID。</span><span class="sxs-lookup"><span data-stu-id="fa90c-105">In the case of the localization example, the value of the **ProductLanguage** property must be changed from the LANGID for English (1033) to the LANGID for French (1036) in the [Property table](property-table.md).</span></span>

<span data-ttu-id="fa90c-106">當地語系化資料庫時，[屬性資料表](property-table.md)中的 [ [**ProductCode**](productcode.md) ] 屬性值必須變更為新的唯一值，因為當地語系化的產品會視為不同的產品。</span><span class="sxs-lookup"><span data-stu-id="fa90c-106">The value of the [**ProductCode**](productcode.md) property in the [Property table](property-table.md) must be changed to a new, unique value when localizing a database because a localized product is considered a different product.</span></span> <span data-ttu-id="fa90c-107">例如，應用程式的德文和英文版會視為兩個不同的產品，而且必須具有不同的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="fa90c-107">For example, the German and English versions of an application are considered two different products and must have different product codes.</span></span> <span data-ttu-id="fa90c-108">請參閱 [產品代碼](product-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="fa90c-108">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="fa90c-109">您可以使用資料庫資料表編輯器來更新屬性工作表中的 [ProductCode] 和 [ProductLanguage] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fa90c-109">Use your database table editor to update the values of the ProductCode and ProductLanguage properties in the Property table.</span></span> <span data-ttu-id="fa90c-110">如果您複製此範例，請不要重複使用顯示的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fa90c-110">Do not reuse the GUID shown if you copy this example.</span></span>

[<span data-ttu-id="fa90c-111">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="fa90c-111">Property Table</span></span>](property-table.md)



| <span data-ttu-id="fa90c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fa90c-112">Property</span></span>                                   | <span data-ttu-id="fa90c-113">值</span><span class="sxs-lookup"><span data-stu-id="fa90c-113">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="fa90c-114">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="fa90c-114">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="fa90c-115">{EE389960-E426-4EEA-B669-AD8129249881}</span><span class="sxs-lookup"><span data-stu-id="fa90c-115">{EE389960-E426-4EEA-B669-AD8129249881}</span></span> |
| [<span data-ttu-id="fa90c-116">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="fa90c-116">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="fa90c-117">1036</span><span class="sxs-lookup"><span data-stu-id="fa90c-117">1036</span></span>                                   |



 

[<span data-ttu-id="fa90c-118">繼續</span><span class="sxs-lookup"><span data-stu-id="fa90c-118">Continue</span></span>](updating-a-summary-information-stream.md)

 

 



