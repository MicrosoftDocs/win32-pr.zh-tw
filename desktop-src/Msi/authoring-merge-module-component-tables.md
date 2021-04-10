---
description: 每個合併模組都需要元件資料表。
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: 撰寫合併模組元件資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026643"
---
# <a name="authoring-merge-module-component-tables"></a><span data-ttu-id="888db-103">撰寫合併模組元件資料表</span><span class="sxs-lookup"><span data-stu-id="888db-103">Authoring Merge Module Component Tables</span></span>

<span data-ttu-id="888db-104">每個合併模組都需要 [元件資料表](component-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="888db-104">A [Component table](component-table.md) is required in every merge module.</span></span> <span data-ttu-id="888db-105">此資料表包含合併模組傳遞至目標 .msi 檔案的每個元件記錄。</span><span class="sxs-lookup"><span data-stu-id="888db-105">This table contains a record for each component delivered by the merge module to the target .msi file.</span></span> <span data-ttu-id="888db-106">請注意，這些元件中的每一個都必須在[撰寫 ModuleComponents 資料表](authoring-modulecomponents-tables.md)中所述的[ModuleComponents 資料表](modulecomponents-table.md)中指定。</span><span class="sxs-lookup"><span data-stu-id="888db-106">Note that each of these components must also be specified in the [ModuleComponents table](modulecomponents-table.md) described in [Authoring ModuleComponents Tables](authoring-modulecomponents-tables.md).</span></span>

<span data-ttu-id="888db-107">在元件資料行中輸入名稱時，請使用標準命名慣例，以確保每個元件的識別碼在所有合併模組和安裝資料庫中都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="888db-107">Use the standard naming convention when entering names into the Component column to ensure that the identifier for each component is unique for all merge modules and installation databases.</span></span> <span data-ttu-id="888db-108">如需詳細資訊，請參閱 [命名合併模組資料庫中的主鍵](naming-primary-keys-in-merge-module-databases.md)。</span><span class="sxs-lookup"><span data-stu-id="888db-108">For more information, see [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="888db-109">依 [元件表格](component-table.md)中的安裝資料庫所述，完成每筆記錄中剩餘的欄位。</span><span class="sxs-lookup"><span data-stu-id="888db-109">Complete the remaining fields in each record as described for an installation database in [Component table](component-table.md).</span></span> <span data-ttu-id="888db-110">合併模組新增至封裝的元件必須遵循下列各節中所述之有效 Windows Installer 元件的指導方針：</span><span class="sxs-lookup"><span data-stu-id="888db-110">The components added to a package by a merge module must adhere to the guidelines for valid Windows Installer Components described in the following sections:</span></span>

-   [<span data-ttu-id="888db-111">Windows Installer 元件</span><span class="sxs-lookup"><span data-stu-id="888db-111">Windows Installer Components</span></span>](windows-installer-components.md)
-   [<span data-ttu-id="888db-112">將應用程式組織成元件</span><span class="sxs-lookup"><span data-stu-id="888db-112">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)

 

 



