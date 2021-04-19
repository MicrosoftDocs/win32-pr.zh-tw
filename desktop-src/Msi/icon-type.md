---
description: 語義類型的圖示類型是其中一種主要格式類型。 此類型是由使用者提供的圖示表格中的索引鍵所組成。
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: 圖示類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970646"
---
# <a name="icon-type"></a><span data-ttu-id="1da79-104">圖示類型</span><span class="sxs-lookup"><span data-stu-id="1da79-104">Icon Type</span></span>

<span data-ttu-id="1da79-105">[語義類型](semantic-types.md)的圖示類型是其中一種[主要格式類型](key-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="1da79-105">The Icon Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="1da79-106">此類型是由使用者提供的 [圖示表格](icon-table.md) 中的索引鍵所組成。</span><span class="sxs-lookup"><span data-stu-id="1da79-106">This type consists of a key into the [Icon table](icon-table.md) provided by the user.</span></span>

<span data-ttu-id="1da79-107">合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。</span><span class="sxs-lookup"><span data-stu-id="1da79-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="1da79-108">Mergemod.dll 不會強制執行這項限制，而是由合併工具所組成，以確保使用者在圖示表格中提供有效的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1da79-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Icon table.</span></span>

<span data-ttu-id="1da79-109">除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。</span><span class="sxs-lookup"><span data-stu-id="1da79-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="1da79-110">二進位類型可搭配下列種類的 CoNtextData 使用。</span><span class="sxs-lookup"><span data-stu-id="1da79-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="1da79-111">**ShortcutIcon CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="1da79-111">**ShortcutIcon ContextData**</span></span>

<span data-ttu-id="1da79-112">可設定的合併模組可以使用此型別，讓使用者在 [圖示資料表](icon-table.md) 中提供一個資料列的外鍵，其中包含適合用來做為快捷方式圖示的影像。</span><span class="sxs-lookup"><span data-stu-id="1da79-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the [Icon Table](icon-table.md) that contains an image suitable for use as a shortcut icon.</span></span> <span data-ttu-id="1da79-113">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Icon"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "ShorcutIcon"。</span><span class="sxs-lookup"><span data-stu-id="1da79-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Icon" into the Type column, and enter "ShorcutIcon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="1da79-114">此類型不適合在使用者介面資料表中使用。</span><span class="sxs-lookup"><span data-stu-id="1da79-114">This type is not appropriate for use in a user interface table.</span></span> <span data-ttu-id="1da79-115">若要將索引鍵修改為這些資料表中的圖示表格，請參閱 [ [二進位類型](binary-type.md)] 下的圖示 CoNtextData。</span><span class="sxs-lookup"><span data-stu-id="1da79-115">To modify a key to the Icon table in these tables see Icon ContextData under [Binary Type](binary-type.md).</span></span>

 

 



