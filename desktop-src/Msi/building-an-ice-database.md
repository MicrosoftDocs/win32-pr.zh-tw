---
description: 選取適當的 [驗證] 以進行驗證之後，開發人員必須將自訂動作一起收集到 ICE 資料庫中。
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: 建立 ICE 資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848945"
---
# <a name="building-an-ice-database"></a><span data-ttu-id="c23d9-103">建立 ICE 資料庫</span><span class="sxs-lookup"><span data-stu-id="c23d9-103">Building an ICE Database</span></span>

<span data-ttu-id="c23d9-104">選取 [適當的](internal-consistency-evaluators-ices.md) [驗證] 以進行驗證之後，開發人員必須將自訂動作一起收集到 ICE 資料庫中。</span><span class="sxs-lookup"><span data-stu-id="c23d9-104">After selecting the appropriate [ICEs](internal-consistency-evaluators-ices.md) for validation, a developer must collect the custom actions together into an ICE database.</span></span> <span data-ttu-id="c23d9-105">.Cub 檔案是標準 .msi 資料庫，其中只包含 Ices-003 和其所需的資料表。</span><span class="sxs-lookup"><span data-stu-id="c23d9-105">A .cub file is a standard .msi database that contains only ICEs and their required tables.</span></span> <span data-ttu-id="c23d9-106">無法安裝 .cub 檔案，而且只能用來儲存和提供 ICE 自訂動作的存取權。</span><span class="sxs-lookup"><span data-stu-id="c23d9-106">A .cub file cannot be installed and is used only to store and provide access to ICE custom actions.</span></span>

<span data-ttu-id="c23d9-107">.Cub 檔案包含下列資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="c23d9-107">A .cub file contains the following database tables.</span></span>



| <span data-ttu-id="c23d9-108">資料表</span><span class="sxs-lookup"><span data-stu-id="c23d9-108">Table</span></span>                                  | <span data-ttu-id="c23d9-109">描述</span><span class="sxs-lookup"><span data-stu-id="c23d9-109">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c23d9-110">二進位</span><span class="sxs-lookup"><span data-stu-id="c23d9-110">Binary</span></span>](binary-table.md)             | <span data-ttu-id="c23d9-111">CustomAction 資料表中所參考之 ICE 海關動作的腳本檔案、Dll 和 Exe。</span><span class="sxs-lookup"><span data-stu-id="c23d9-111">The script files, DLLs, and EXEs of the ICE customs actions that are referenced in the CustomAction table.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="c23d9-112">CustomAction</span><span class="sxs-lookup"><span data-stu-id="c23d9-112">CustomAction</span></span>](customaction-table.md) | <span data-ttu-id="c23d9-113">這個資料表中的每一筆記錄都會對應到 .cub 檔中所包含的 ICE 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="c23d9-113">Each record in this table corresponds to an ICE custom action included in the .cub file.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="c23d9-114">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="c23d9-114">\_ICESequence</span></span>                          | <span data-ttu-id="c23d9-115">下表列出在其執行順序中，.cub 檔中所包含的 ICE 海關動作。</span><span class="sxs-lookup"><span data-stu-id="c23d9-115">This table lists the ICE customs actions included in the .cub file in their execution sequence.</span></span> <span data-ttu-id="c23d9-116">此表格中所列的 ICE 自訂動作會藉由呼叫 [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)來執行，或使用 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)個別執行。</span><span class="sxs-lookup"><span data-stu-id="c23d9-116">The ICE custom actions listed in this table are executed by calling [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), or individually executed using [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> |
| [<span data-ttu-id="c23d9-117">\_驗證</span><span class="sxs-lookup"><span data-stu-id="c23d9-117">\_Validation</span></span>](-validation-table.md)  | <span data-ttu-id="c23d9-118">此資料表包含要合併至驗證資料表的 .cub 檔專案。 \_</span><span class="sxs-lookup"><span data-stu-id="c23d9-118">This table contains the .cub file entries that are to be merged into the \_Validation table.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c23d9-119">\_特殊</span><span class="sxs-lookup"><span data-stu-id="c23d9-119">\_Special</span></span>                              | <span data-ttu-id="c23d9-120">特定 ICE 自訂動作所需的任何特殊處理資料表，都必須包含在 .cub 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c23d9-120">Any special processing tables required by particular ICE custom actions must be included in the .cub file.</span></span> <span data-ttu-id="c23d9-121">這些資料表的名稱必須有前置底線。</span><span class="sxs-lookup"><span data-stu-id="c23d9-121">The name of these tables must have a leading underscore.</span></span>                                                                                                        |



 

<span data-ttu-id="c23d9-122">請參閱 [範例 .cub](sample--cub-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="c23d9-122">See [Sample .cub File](sample--cub-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c23d9-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="c23d9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c23d9-124">打造冰</span><span class="sxs-lookup"><span data-stu-id="c23d9-124">Building An ICE</span></span>](building-an-ice.md)
</dt> </dl>

 

 



