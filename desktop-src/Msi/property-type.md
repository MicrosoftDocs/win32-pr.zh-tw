---
description: 語義類型的屬性類型是其中一種主要格式類型。 此類型是由使用者提供的屬性資料表中的外鍵所組成。
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: 屬性類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026724"
---
# <a name="property-type"></a><span data-ttu-id="f7bac-104">屬性類型</span><span class="sxs-lookup"><span data-stu-id="f7bac-104">Property Type</span></span>

<span data-ttu-id="f7bac-105">[語義類型](semantic-types.md)的屬性類型是其中一種[主要格式類型](key-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f7bac-105">The Property Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="f7bac-106">此類型是由使用者提供的 [屬性資料表](property-table.md) 中的外鍵所組成。</span><span class="sxs-lookup"><span data-stu-id="f7bac-106">This type consists of a foreign key into the [Property table](property-table.md) provided by the user.</span></span>

<span data-ttu-id="f7bac-107">合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。</span><span class="sxs-lookup"><span data-stu-id="f7bac-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="f7bac-108">Mergemod.dll 不會強制執行這項限制，而是由合併工具所組成，以確保使用者在屬性工作表中提供有效的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f7bac-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Property table.</span></span> <span data-ttu-id="f7bac-109">屬性工作表的主要索引鍵是屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="f7bac-109">The primary keys of the Property table are the property names.</span></span>

<span data-ttu-id="f7bac-110">除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。</span><span class="sxs-lookup"><span data-stu-id="f7bac-110">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="f7bac-111">屬性類型可與下列種類的 CoNtextData 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="f7bac-111">The Property type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="f7bac-112">**Null CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="f7bac-112">**Null ContextData**</span></span>

<span data-ttu-id="f7bac-113">可設定的合併模組可以使用此類型，讓使用者能夠提供屬性名稱給模組中的資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="f7bac-113">A configurable merge module may use this type to enable the user to provide a property name to a database table in the module.</span></span> <span data-ttu-id="f7bac-114">合併工具會將屬性的識別碼取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中的範本。</span><span class="sxs-lookup"><span data-stu-id="f7bac-114">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="f7bac-115">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Property"，然後將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行保留空白。</span><span class="sxs-lookup"><span data-stu-id="f7bac-115">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="f7bac-116">**公用 CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="f7bac-116">**Public ContextData**</span></span>

<span data-ttu-id="f7bac-117">可設定的合併模組可以使用此類型，讓使用者能夠將 [公用屬性](public-properties.md) 的名稱提供給模組中的資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="f7bac-117">A configurable merge module may use this type to enable the user to provide the name of a [public property](public-properties.md) to a database table in the module.</span></span> <span data-ttu-id="f7bac-118">合併工具會將屬性的識別碼取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中的範本。</span><span class="sxs-lookup"><span data-stu-id="f7bac-118">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="f7bac-119">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Property"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "Public"。</span><span class="sxs-lookup"><span data-stu-id="f7bac-119">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and enter "Public" into the ContextData column of the ModuleConfiguration table.</span></span>

<span data-ttu-id="f7bac-120">**私用 CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="f7bac-120">**Private ContextData**</span></span>

<span data-ttu-id="f7bac-121">可設定的合併模組可以使用此類型，讓使用者能夠將 [私用屬性](private-properties.md) 的名稱提供給模組中的資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="f7bac-121">A configurable merge module may use this type to enable the user to provide the name of a [private property](private-properties.md) to a database table in the module.</span></span> <span data-ttu-id="f7bac-122">合併工具會將屬性的識別碼取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中的範本。</span><span class="sxs-lookup"><span data-stu-id="f7bac-122">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="f7bac-123">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Property"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入「私用」。</span><span class="sxs-lookup"><span data-stu-id="f7bac-123">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and enter "Private" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



