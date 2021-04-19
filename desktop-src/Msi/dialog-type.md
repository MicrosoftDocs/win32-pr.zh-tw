---
description: 語義類型的對話類型是其中一種主要格式類型。 此類型是由使用者提供的對話方塊資料表中的外鍵所組成。
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: 對話方塊類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984580"
---
# <a name="dialog-type"></a><span data-ttu-id="c6fbd-104">對話方塊類型</span><span class="sxs-lookup"><span data-stu-id="c6fbd-104">Dialog Type</span></span>

<span data-ttu-id="c6fbd-105">[語義類型](semantic-types.md)的對話類型是其中一種[主要格式類型](key-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-105">The Dialog Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="c6fbd-106">此類型是由使用者提供的 [對話方塊資料表](dialog-table.md) 中的外鍵所組成。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-106">This type consists of a foreign key into the [Dialog table](dialog-table.md) provided by the user.</span></span>

<span data-ttu-id="c6fbd-107">合併工具必須將有效的 Windows Installer [識別碼](identifier.md) 取代為此類型的專案。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="c6fbd-108">Mergemod.dll 不會強制執行這項限制，而是由「合併」工具組成，以確保使用者在對話方塊資料表中提供有效的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Dialog table.</span></span>

<span data-ttu-id="c6fbd-109">除非 msmConfigItemNonNullable 已包含在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 [屬性] 欄位中，否則 Null 對此型別是有效的值。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="c6fbd-110">對話方塊類型可與下列種類的 CoNtextData 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-110">The Dialog type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="c6fbd-111">**DialogNext CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-111">**DialogNext ContextData**</span></span>

<span data-ttu-id="c6fbd-112">可設定的合併模組可以使用此類型，讓使用者在對話方塊資料表中提供外鍵。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-112">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="c6fbd-113">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Dialog"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入 "DialogNext"。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogNext" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="c6fbd-114">**DialogPrev CoNtextData**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-114">**DialogPrev ContextData**</span></span>

<span data-ttu-id="c6fbd-115">可設定的合併模組可以使用此類型，讓使用者在對話方塊資料表中提供外鍵。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-115">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="c6fbd-116">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入可設定專案的名稱，在 [格式] 資料行中輸入 "1"，在 [類型] 資料行中輸入 "Dialog"，然後在 ModuleConfiguration 資料表的 CoNtextData 資料行中輸入 "DialogPrev"。</span><span class="sxs-lookup"><span data-stu-id="c6fbd-116">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogPrev" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



