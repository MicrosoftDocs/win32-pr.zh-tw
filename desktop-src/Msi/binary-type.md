---
description: 語義類型的二進位類型是其中一種主要格式類型。 此類型是由使用者提供的二進位資料表中的索引鍵所組成。
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: 二進位類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513233"
---
# <a name="binary-type"></a><span data-ttu-id="094eb-104">二進位類型</span><span class="sxs-lookup"><span data-stu-id="094eb-104">Binary Type</span></span>

<span data-ttu-id="094eb-105">[語義類型](semantic-types.md)的二進位類型是其中一種[主要格式類型](key-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="094eb-105">The Binary Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="094eb-106">此類型是由使用者提供的 [二進位資料表](binary-table.md) 中的索引鍵所組成。</span><span class="sxs-lookup"><span data-stu-id="094eb-106">This type consists of a key into the [Binary table](binary-table.md) provided by the user.</span></span>

<span data-ttu-id="094eb-107">合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。</span><span class="sxs-lookup"><span data-stu-id="094eb-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="094eb-108">Mergemod.dll 不會強制執行這項限制，而是由「合併」工具組成，以確保使用者在二進位資料表中提供有效的金鑰。</span><span class="sxs-lookup"><span data-stu-id="094eb-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Binary table.</span></span>

<span data-ttu-id="094eb-109">除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。</span><span class="sxs-lookup"><span data-stu-id="094eb-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="094eb-110">二進位類型可搭配下列種類的 CoNtextData 使用。</span><span class="sxs-lookup"><span data-stu-id="094eb-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="094eb-111">**點陣圖 CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="094eb-111">**Bitmap ContextData**</span></span>

<span data-ttu-id="094eb-112">可設定的合併模組可以使用此型別，讓使用者在包含點陣圖影像的二進位資料表中，提供資料列的外鍵。</span><span class="sxs-lookup"><span data-stu-id="094eb-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the Binary Table that contains a bitmap image.</span></span> <span data-ttu-id="094eb-113">Mergmod.dll 不保證任何特定大小或點陣圖類型，而且合併工具必須確定資料是有效的影像。</span><span class="sxs-lookup"><span data-stu-id="094eb-113">Mergmod.dll does not guarantee any specific size or type of bitmap and the merge tool must ensure that the data is a valid image.</span></span> <span data-ttu-id="094eb-114">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "Bitmap"。</span><span class="sxs-lookup"><span data-stu-id="094eb-114">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Binary" into the Type column, and enter "Bitmap" into the ContextData column of the ModuleConfiguration table.</span></span>

<span data-ttu-id="094eb-115">**圖示 CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="094eb-115">**Icon ContextData**</span></span>

<span data-ttu-id="094eb-116">可設定的合併模組可以使用此型別，讓使用者在包含圖示影像的二進位資料表中，提供一個資料列的外鍵。</span><span class="sxs-lookup"><span data-stu-id="094eb-116">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the Binary Table that contains an icon image.</span></span> <span data-ttu-id="094eb-117">Mergmod.dll 不保證任何特定大小或類型的圖示，且合併工具必須確定資料是有效的影像。</span><span class="sxs-lookup"><span data-stu-id="094eb-117">Mergmod.dll does not guarantee any specific size or type of icon and the merge tool must ensure that the data is a valid image.</span></span> <span data-ttu-id="094eb-118">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "Icon"。</span><span class="sxs-lookup"><span data-stu-id="094eb-118">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Binary" into the Type column, and enter "Icon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="094eb-119">這種類型不適合用在公告資料表中。</span><span class="sxs-lookup"><span data-stu-id="094eb-119">This type is not appropriate for use in an advertisement table.</span></span>

<span data-ttu-id="094eb-120">**EXE CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="094eb-120">**EXE ContextData**</span></span>

<span data-ttu-id="094eb-121">可設定的合併模組可以使用此型別，讓使用者在包含32位可執行檔映射的二進位資料表中，提供資料列的外鍵。</span><span class="sxs-lookup"><span data-stu-id="094eb-121">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the Binary Table that contains a 32-bit executable image.</span></span> <span data-ttu-id="094eb-122">Mergmod.dll 不會驗證資料是否有效，且合併工具必須確定資料是有效的 PE 檔案。</span><span class="sxs-lookup"><span data-stu-id="094eb-122">Mergmod.dll does not validate the data is valid and the merge tool must ensure that the data is a valid PE file.</span></span> <span data-ttu-id="094eb-123">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "EXE"。</span><span class="sxs-lookup"><span data-stu-id="094eb-123">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Binary" into the Type column, and enter "EXE" into the ContextData column of the ModuleConfiguration table.</span></span>

<span data-ttu-id="094eb-124">**EXE64 CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="094eb-124">**EXE64 ContextData**</span></span>

<span data-ttu-id="094eb-125">可設定的合併模組可以使用此型別，讓使用者可以在包含32位或64位可執行檔映射的二進位資料表中，提供資料列的外鍵。</span><span class="sxs-lookup"><span data-stu-id="094eb-125">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the Binary Table that contains either a 32-bit or 64-bit executable image.</span></span> <span data-ttu-id="094eb-126">Mergmod.dll 不會驗證資料是否有效，且合併工具必須確定資料是有效的 PE 檔案。</span><span class="sxs-lookup"><span data-stu-id="094eb-126">Mergmod.dll does not validate the data is valid and the merge tool must ensure that the data is a valid PE file.</span></span> <span data-ttu-id="094eb-127">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在類型資料行中輸入 "Binary"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "EXE64"。</span><span class="sxs-lookup"><span data-stu-id="094eb-127">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Binary" into the Type column, and enter "EXE64" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



