---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: 功能與選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866cead02021b8d933ca03483e77de832d8d094a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992118"
---
# <a name="features-and-options"></a><span data-ttu-id="fed00-104">功能與選項</span><span class="sxs-lookup"><span data-stu-id="fed00-104">Features and Options</span></span>

<span data-ttu-id="fed00-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="fed00-105">This topic is not current.</span></span> <span data-ttu-id="fed00-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="fed00-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fed00-107">功能/選項和參數結構會在 PrintCapabilities 檔中用來代表構成裝置設定定義的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="fed00-107">Feature/Option and parameter constructs are used in a PrintCapabilities document to represent device attributes that contribute to the definition of the device configuration.</span></span> <span data-ttu-id="fed00-108">如需功能/選項結構的範例，請考慮能夠以數種解析度列印的列印裝置。</span><span class="sxs-lookup"><span data-stu-id="fed00-108">For an example of a Feature/Option construct, consider a printing device that is capable of printing in several resolutions.</span></span> <span data-ttu-id="fed00-109">定義解析的裝置屬性可以表示為功能實例，其中每個可能的輸出解析度值都表示為個別的選項實例。</span><span class="sxs-lookup"><span data-stu-id="fed00-109">The device attribute that defines the resolution can be represented as a Feature instance, with each of the possible output resolution values represented as an individual Option instance.</span></span> <span data-ttu-id="fed00-110">其中一個選項實例可以代表 300 DPI 的解析度，另一個則代表 600 DPI 的解析度等等。</span><span class="sxs-lookup"><span data-stu-id="fed00-110">One Option instance can represent a resolution of 300 dpi, another can represent a resolution of 600 dpi, and so on.</span></span>

<span data-ttu-id="fed00-111">請注意，列印架構要求每個 PrintCapabilities 檔中報告的功能、選項和 ParameterDef 實例清單必須保持不變，而不受設定影響。</span><span class="sxs-lookup"><span data-stu-id="fed00-111">It should be noted that the Print Schema requires that the list of Feature, Option, and ParameterDef instances reported in each PrintCapabilities document must remain constant, independent of the configuration.</span></span> <span data-ttu-id="fed00-112">這可讓您以明確的方式表示設定的設定和相依性。</span><span class="sxs-lookup"><span data-stu-id="fed00-112">This allows configurations and dependencies on configurations to be expressed in an unambiguous way.</span></span> <span data-ttu-id="fed00-113">這項需求的含意是，不論任何其他功能或 subfeature 的設定為何，每個功能和 subfeature 都必須有妥善定義的設定。</span><span class="sxs-lookup"><span data-stu-id="fed00-113">The implication of this requirement is that every Feature and subfeature must have a well-defined setting, regardless of the setting of any other Feature or subfeature.</span></span> <span data-ttu-id="fed00-114">因此，每個 subfeature 都必須有相當於無 op ([關閉]、[已停用] 或 [無] 設定) 的選項，當使用者在父功能中選取 [無操作] 選項時，就會自動為所有子功能選取。</span><span class="sxs-lookup"><span data-stu-id="fed00-114">Therefore, each subfeature must have an Option that is equivalent to a no-op (an Off, Disabled, or None setting), that is automatically selected for all subfeatures when the user selects the no-op Option in the parent Feature.</span></span> <span data-ttu-id="fed00-115">相反地，當其中一個子功能設定為啟用的選項時，也會啟用父功能和其他相關聯的子功能。</span><span class="sxs-lookup"><span data-stu-id="fed00-115">Conversely, when one of the subfeatures is set to an enabled Option, the parent Feature and other associated subfeatures are also enabled.</span></span> <span data-ttu-id="fed00-116">在此同時，PrintTicket 提供者必須確保在 PrintTicket) 驗證期間 (，因為所有功能和 subfeature 實例的設定都已定義，無論裝置設定為何，以及 subfeature 設定與父功能的設定一致。</span><span class="sxs-lookup"><span data-stu-id="fed00-116">In the meantime, the PrintTicket provider must ensure (during PrintTicket validation) that settings for all Feature and subfeature instances are defined, regardless of the device configuration, and that the subfeature settings are consistent with the settings of the parent Feature.</span></span> <span data-ttu-id="fed00-117">這樣可確保裝置不會有不一致的 PrintTicket，其中某些子功能表示已啟用裝訂，但其他子功能表示已停用裝訂。</span><span class="sxs-lookup"><span data-stu-id="fed00-117">This ensures that the device is not given an inconsistent PrintTicket where some subfeatures indicate that, for example, stapling is enabled, but other subfeatures indicate that stapling is disabled.</span></span>

<span data-ttu-id="fed00-118">請注意，PrintCapabilities 作者不需要利用功能元素的嵌套功能。</span><span class="sxs-lookup"><span data-stu-id="fed00-118">Note that PrintCapabilities authors are not required to utilize the nesting capabilities of Feature elements.</span></span> <span data-ttu-id="fed00-119">如果您想要的話，可以將所有的功能實例呈現為一般結構，作為彼此的同級。</span><span class="sxs-lookup"><span data-stu-id="fed00-119">If they prefer, they can present all Feature instances in a flat structure, as siblings of each other.</span></span> <span data-ttu-id="fed00-120">另外也請注意，只要將所有子功能移至根層級，就可以壓平合併功能實例的集合。</span><span class="sxs-lookup"><span data-stu-id="fed00-120">Note also that a nested collection of Feature instances can be flattened simply by moving all of the subfeatures out to the root level.</span></span> <span data-ttu-id="fed00-121">唯一必須採取的預防措施是確保這些功能實例的名稱屬性是唯一的。</span><span class="sxs-lookup"><span data-stu-id="fed00-121">The only precaution that must be taken is to ensure that the name attributes of these Feature instances are unique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fed00-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="fed00-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fed00-123">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="fed00-123">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



