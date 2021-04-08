---
description: 語義類型的目錄類型是其中一種主要格式類型，其中包含由使用者提供的目錄資料表中的外鍵。
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: 目錄類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850220"
---
# <a name="directory-type"></a><span data-ttu-id="4de57-103">目錄類型</span><span class="sxs-lookup"><span data-stu-id="4de57-103">Directory Type</span></span>

<span data-ttu-id="4de57-104">[語義類型](semantic-types.md)的目錄類型是其中一種[主要格式類型](key-format-types.md)，其中包含由使用者提供的[目錄資料表](directory-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="4de57-104">The Directory Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md), which consists of a foreign key into the [Directory table](directory-table.md) provided by the user.</span></span>

<span data-ttu-id="4de57-105">合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。</span><span class="sxs-lookup"><span data-stu-id="4de57-105">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="4de57-106">Mergemod.dll 不會強制執行這項限制，而是由「合併」工具組成，以確保使用者在目錄資料表中提供有效的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4de57-106">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Directory table.</span></span>

<span data-ttu-id="4de57-107">目錄類型的可設定專案只能修改安裝的目的地目錄，而不會修改來源映射。</span><span class="sxs-lookup"><span data-stu-id="4de57-107">A configurable item of the Directory type should only modify the destination directory of the installation and not modify the source image.</span></span> <span data-ttu-id="4de57-108">因此，此類型的可設定專案應只修改目錄資料表的外鍵，而不會直接修改目錄資料表。</span><span class="sxs-lookup"><span data-stu-id="4de57-108">A configurable item of this type should therefore only modify foreign keys to the Directory table and not modify the Directory table directly.</span></span>

<span data-ttu-id="4de57-109">因為 \_ [元件資料表](component-table.md) 的目錄資料行不可為 null，所以即使 msmConfigItemNonNullable 未在 [屬性] 資料行中設定，null 也是此類型的可設定專案的無效值。</span><span class="sxs-lookup"><span data-stu-id="4de57-109">Because the Directory\_ column of the [Component table](component-table.md) is non-nullable, null is an invalid value for a configurable item of this type even if the msmConfigItemNonNullable is not set in the Attributes column.</span></span>

<span data-ttu-id="4de57-110">目錄類型可搭配兩種 CoNtextData 使用。</span><span class="sxs-lookup"><span data-stu-id="4de57-110">The Directory type may be used with two kinds of ContextData.</span></span>

<span data-ttu-id="4de57-111">**IsolationDirectory CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="4de57-111">**IsolationDirectory ContextData**</span></span>

<span data-ttu-id="4de57-112">可設定的合併模組可以使用此類型，讓使用者能夠提供模組中檔案的目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="4de57-112">A configurable merge module may use this type to enable the user to provide a destination directory for files in the module.</span></span> <span data-ttu-id="4de57-113">合併工具會在 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中，將目錄的識別碼取代為範本。</span><span class="sxs-lookup"><span data-stu-id="4de57-113">The merge tool substitutes the directory's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="4de57-114">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入目錄的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Directory"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入 "IsolationDirectory"。</span><span class="sxs-lookup"><span data-stu-id="4de57-114">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "IsolationDirectory" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="4de57-115">**ShortcutLocation CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="4de57-115">**ShortcutLocation ContextData**</span></span>

<span data-ttu-id="4de57-116">可設定的合併模組可以使用此類型，讓使用者能夠提供模組中快捷方式的目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="4de57-116">A configurable merge module may use this type to enable the user to provide a destination directory for shortcuts in the module.</span></span> <span data-ttu-id="4de57-117">合併工具會在 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中，將快捷方式的識別碼取代為範本。</span><span class="sxs-lookup"><span data-stu-id="4de57-117">The merge tool substitutes the shortcut's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="4de57-118">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入目錄的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Directory"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入 "ShortcutLocation"。</span><span class="sxs-lookup"><span data-stu-id="4de57-118">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "ShortcutLocation" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



