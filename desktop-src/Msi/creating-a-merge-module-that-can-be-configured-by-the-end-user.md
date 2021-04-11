---
description: 若要建立合併模組，請使用「撰寫合併模組」主題中所述的一般方針。
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: 建立可由 End-User 設定的合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193503"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a><span data-ttu-id="a8671-103">建立可由 End-User 設定的合併模組</span><span class="sxs-lookup"><span data-stu-id="a8671-103">Creating a Merge Module that Can Be Configured by the End-User</span></span>

<span data-ttu-id="a8671-104">若要建立合併模組，請使用「 [撰寫合併模組](authoring-merge-modules.md) 」主題中所述的一般方針。</span><span class="sxs-lookup"><span data-stu-id="a8671-104">To create merge modules, use the general guidelines that are described in the [Authoring Merge Modules](authoring-merge-modules.md) topic.</span></span> <span data-ttu-id="a8671-105">此外，您必須執行下列動作，才能建立可由模組的終端使用者設定的合併模組：</span><span class="sxs-lookup"><span data-stu-id="a8671-105">In addition, you must do the following to create a merge module that may be configured by the end-user of the module:</span></span>

-   <span data-ttu-id="a8671-106">終端使用者必須有 Mergemod.dll 版本2.0 才能設定您的模組。</span><span class="sxs-lookup"><span data-stu-id="a8671-106">End-users need to have Mergemod.dll version 2.0 to configure your module.</span></span> <span data-ttu-id="a8671-107">具有舊版 Mergemod.dll 的使用者可以套用模組，但一律會取得預設設定。</span><span class="sxs-lookup"><span data-stu-id="a8671-107">Users who have earlier versions of Mergemod.dll can apply the module, but they always get the default settings.</span></span>
-   <span data-ttu-id="a8671-108">將 [ModuleConfiguration 資料表](moduleconfiguration-table.md) 加入至合併模組，以識別使用者可能設定的專案。</span><span class="sxs-lookup"><span data-stu-id="a8671-108">Add a [ModuleConfiguration Table](moduleconfiguration-table.md) to the merge module to identify the items that may be configured by an end-user.</span></span> <span data-ttu-id="a8671-109">為每個可設定的專案新增此資料表中的記錄。</span><span class="sxs-lookup"><span data-stu-id="a8671-109">Add a record in this table for each configurable item.</span></span> <span data-ttu-id="a8671-110">這些專案會取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)中所指定的範本。</span><span class="sxs-lookup"><span data-stu-id="a8671-110">These items are substituted into the templates that are specified in the [ModuleSubstitution Table](modulesubstitution-table.md).</span></span> <span data-ttu-id="a8671-111">在 [名稱] 欄位中輸入每個可設定專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8671-111">Enter a name for each configurable item into the Name field.</span></span> <span data-ttu-id="a8671-112">針對 [格式]、[類型] 和 [CoNtextData] 資料行中的每個專案，輸入格式、類型和語義內容。</span><span class="sxs-lookup"><span data-stu-id="a8671-112">Enter the format, type, and semantic context for each item in the Format, Type, and ContextData columns.</span></span> <span data-ttu-id="a8671-113">如需詳細資訊，請參閱 [語義類型](semantic-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a8671-113">For more information, see [Semantic Types](semantic-types.md).</span></span> <span data-ttu-id="a8671-114">使用 [CMSM 的特殊格式](cmsm-special-format.md)，在 [DefaultValue] 欄位中輸入專案的預設值。</span><span class="sxs-lookup"><span data-stu-id="a8671-114">Enter a default value for the item in the DefaultValue field using the [CMSM Special Format](cmsm-special-format.md).</span></span>
-   <span data-ttu-id="a8671-115">將 [ModuleSubstitution 資料表](modulesubstitution-table.md) 加入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="a8671-115">Add a [ModuleSubstitution Table](modulesubstitution-table.md) to the merge module.</span></span> <span data-ttu-id="a8671-116">這個資料表中的每一筆記錄都會對應到一個或多個可設定的專案，並放入 merge module 資料庫的一個欄位中。</span><span class="sxs-lookup"><span data-stu-id="a8671-116">Each record in this table corresponds to a substitution of one or more configurable items into one field of the merge module database.</span></span> <span data-ttu-id="a8671-117">輸入接收替代之欄位的資料表、資料列和資料行。</span><span class="sxs-lookup"><span data-stu-id="a8671-117">Enter the table, row, and column of the field that receives the substitution.</span></span> <span data-ttu-id="a8671-118">使用 [CMSM 的特殊格式](cmsm-special-format.md)，在 [值] 資料行中輸入替代的格式設定範本。</span><span class="sxs-lookup"><span data-stu-id="a8671-118">Enter a formatting template for the substitution into the Value column using the [CMSM Special Format](cmsm-special-format.md).</span></span>
-   <span data-ttu-id="a8671-119">將記錄加入至 ModuleSubstitution 和 ModuleConfiguration 資料表的 [驗證資料表](-validation-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="a8671-119">Add records to the [Validation Table](-validation-table.md) for the ModuleSubstitution and ModuleConfiguration tables.</span></span>
-   <span data-ttu-id="a8671-120">將記錄加入至[ModuleSubstitution 資料表](modulesubstitution-table.md)和[ModuleConfiguration 資料表](moduleconfiguration-table.md)的[ModuleIgnoreTable 資料表](moduleignoretable-table.md)。</span><span class="sxs-lookup"><span data-stu-id="a8671-120">Add records to the [ModuleIgnoreTable Table](moduleignoretable-table.md) for the [ModuleSubstitution Table](modulesubstitution-table.md) and the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="a8671-121">這可確保模組與版本為2.0 的 Mergemod.dll 版本的使用者相容。</span><span class="sxs-lookup"><span data-stu-id="a8671-121">This ensures that the module is compatible for users who have versions of Mergemod.dll that are earlier than version 2.0.</span></span>

 

 



