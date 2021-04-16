---
description: 合併模組資料庫的主鍵名稱必須遵守標準命名慣例。
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: 命名合併模組資料庫中的主鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512780"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a><span data-ttu-id="d9406-103">命名合併模組資料庫中的主鍵</span><span class="sxs-lookup"><span data-stu-id="d9406-103">Naming Primary Keys in Merge Module Databases</span></span>

<span data-ttu-id="d9406-104">合併模組資料庫的主鍵名稱必須遵守標準命名慣例。</span><span class="sxs-lookup"><span data-stu-id="d9406-104">The names of primary keys a merge module database must adhere to a standard naming convention.</span></span> <span data-ttu-id="d9406-105">此命名慣例的目的是要降低在合併模組和目標安裝封裝的資料表資料行之間建立名稱衝突的可能性。</span><span class="sxs-lookup"><span data-stu-id="d9406-105">The purpose of this naming convention is to reduce the possibility of creating a name conflict between the table columns in the merge module and the target installation package.</span></span> <span data-ttu-id="d9406-106">命名慣例無法套用至主要索引鍵是可安裝資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="d9406-106">The naming convention cannot be applied to tables in which the primary key is installable data.</span></span> <span data-ttu-id="d9406-107">請勿將命名慣例套用至下列資料表：</span><span class="sxs-lookup"><span data-stu-id="d9406-107">Do not apply the naming convention to the following tables:</span></span>

-   [<span data-ttu-id="d9406-108">MIME 資料表</span><span class="sxs-lookup"><span data-stu-id="d9406-108">MIME Table</span></span>](mime-table.md)
-   [<span data-ttu-id="d9406-109">延伸模組資料表</span><span class="sxs-lookup"><span data-stu-id="d9406-109">Extension Table</span></span>](extension-table.md)
-   [<span data-ttu-id="d9406-110">圖示表</span><span class="sxs-lookup"><span data-stu-id="d9406-110">Icon Table</span></span>](icon-table.md)
-   [<span data-ttu-id="d9406-111">動詞資料表</span><span class="sxs-lookup"><span data-stu-id="d9406-111">Verb Table</span></span>](verb-table.md)
-   [<span data-ttu-id="d9406-112">ProgId 資料表</span><span class="sxs-lookup"><span data-stu-id="d9406-112">ProgId Table</span></span>](progid-table.md)

<span data-ttu-id="d9406-113">例如，請勿將用於 MIME 資料表的主鍵，因為這是 MIME 類型，而套用命名程式會變更其意義。</span><span class="sxs-lookup"><span data-stu-id="d9406-113">For example, do not use for the primary key of the MIME table because this is the MIME type and applying the naming procedure would change its meaning.</span></span> <span data-ttu-id="d9406-114">在這些情況下，名稱衝突取決於各模組之間唯一的資料意義。</span><span class="sxs-lookup"><span data-stu-id="d9406-114">In these cases, name conflicts depend on the meaning of the data being unique across modules.</span></span>

<span data-ttu-id="d9406-115">合併模組中的主鍵名稱必須由可讀取的名稱所組成，並附加自合併模組之 GUID 所建立的字串。</span><span class="sxs-lookup"><span data-stu-id="d9406-115">The name of a primary key in a merge module must consist of a readable name appended with a string made from the merge module's GUID.</span></span> <span data-ttu-id="d9406-116">每個合併模組都必須有自己的 [*GUID*](g-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="d9406-116">Every merge module must have its own [*GUID*](g-gly.md).</span></span> <span data-ttu-id="d9406-117">合併模組的 GUID 也應該撰寫到合併模組的 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="d9406-117">The merge module's GUID should also be authored into the [**Revision Number Summary**](revision-number-summary.md) property of the merge module.</span></span> <span data-ttu-id="d9406-118">開發人員可以使用 GUIDGEN 之類的公用程式來建立 Guid。</span><span class="sxs-lookup"><span data-stu-id="d9406-118">Developers can create GUIDs using a utility such as GUIDGEN.</span></span>

<span data-ttu-id="d9406-119">下列程式描述如何產生遵守標準命名慣例的主資料庫索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d9406-119">The following procedure describes how to generate a primary database key that adheres to the standard naming convention.</span></span> <span data-ttu-id="d9406-120">僅將下列程式套用至主要索引鍵不是安裝資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="d9406-120">Apply the following procedure only to tables where the primary key is not data being installed.</span></span>

<span data-ttu-id="d9406-121">**在合併模組中命名資料表記錄的主鍵**</span><span class="sxs-lookup"><span data-stu-id="d9406-121">**To name a primary key of a table record in a merge module**</span></span>

1.  <span data-ttu-id="d9406-122">撰寫主要金鑰名稱的可讀取部分。</span><span class="sxs-lookup"><span data-stu-id="d9406-122">Author the readable part of the name for the primary key.</span></span> <span data-ttu-id="d9406-123">挑選可識別此記錄的可讀取名稱，例如，MyRowEntry。</span><span class="sxs-lookup"><span data-stu-id="d9406-123">Pick a readable name that identifies this record, for example, MyRowEntry.</span></span>
2.  <span data-ttu-id="d9406-124">產生或取得合併模組的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d9406-124">Generate or obtain the GUID of the merge module.</span></span> <span data-ttu-id="d9406-125">請注意，所有 Guid 都必須以大寫撰寫。</span><span class="sxs-lookup"><span data-stu-id="d9406-125">Note that all GUIDs must be authored in uppercase.</span></span> <span data-ttu-id="d9406-126">如需有關 Guid 的詳細資訊，請參閱 [guid](guid.md)。</span><span class="sxs-lookup"><span data-stu-id="d9406-126">For more information about GUIDs, see [GUID](guid.md).</span></span> <span data-ttu-id="d9406-127">以下是 GUID： {880DE2F0-CDD8-11D1-A849-006097ABDE17} 的範例。</span><span class="sxs-lookup"><span data-stu-id="d9406-127">The following is an example of a GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}.</span></span> <span data-ttu-id="d9406-128">在下列步驟中，您會將此修改為必須附加至合併模組中每個主鍵名稱的字元字串。</span><span class="sxs-lookup"><span data-stu-id="d9406-128">In the following steps you modify this into a character string that must be appended to every primary key name in the merge module.</span></span>
3.  <span data-ttu-id="d9406-129">從 GUID 的開頭和結尾移除大括弧。</span><span class="sxs-lookup"><span data-stu-id="d9406-129">Remove the curly braces from the beginning and end of the GUID.</span></span>
4.  <span data-ttu-id="d9406-130">將所有的連字號變更為底線。</span><span class="sxs-lookup"><span data-stu-id="d9406-130">Change all the dashes to underscores.</span></span>
5.  <span data-ttu-id="d9406-131">將結果附加至主要金鑰名稱可讀取部分的結尾。</span><span class="sxs-lookup"><span data-stu-id="d9406-131">Append the result to the end of the readable part of the primary key name.</span></span> <span data-ttu-id="d9406-132">以句點分隔已修改 GUID 的可讀取名稱。</span><span class="sxs-lookup"><span data-stu-id="d9406-132">Separate the readable name from the modified GUID by a period.</span></span> <span data-ttu-id="d9406-133">上述範例 GUID 的主要金鑰名稱會變成 MyRowEntry. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17。</span><span class="sxs-lookup"><span data-stu-id="d9406-133">The primary key name for the example GUID given above becomes MyRowEntry.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>
6.  <span data-ttu-id="d9406-134">重複以命名合併模組中所有資料表的所有主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d9406-134">Repeat to name all the primary keys of all tables in the merge module.</span></span>

 

 



