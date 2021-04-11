---
description: ICE26 會驗證 Windows Installer 資料庫中的順序資料表。
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850176"
---
# <a name="ice26"></a><span data-ttu-id="070df-103">ICE26</span><span class="sxs-lookup"><span data-stu-id="070df-103">ICE26</span></span>

<span data-ttu-id="070df-104">ICE26 會驗證下列每一個 [*順序資料表*](s-gly.md) 都包含資料表所需的動作，而且不包含資料表中不允許的任何動作：</span><span class="sxs-lookup"><span data-stu-id="070df-104">ICE26 validates that each of the following [*sequence tables*](s-gly.md) contain the actions that are required by the table and does not contain any actions disallowed in the table:</span></span>

-   [<span data-ttu-id="070df-105">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="070df-105">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="070df-106">AdminExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="070df-106">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="070df-107">InstallUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="070df-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="070df-108">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="070df-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="070df-109">結果</span><span class="sxs-lookup"><span data-stu-id="070df-109">Result</span></span>

<span data-ttu-id="070df-110">如果安裝封裝的順序資料表缺少必要的動作，或包含不允許的動作，ICE26 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="070df-110">ICE26 posts an error message if the installation package has a sequence table that lacks a required action or that contains an action that is disallowed for the table.</span></span>

## <a name="example"></a><span data-ttu-id="070df-111">範例</span><span class="sxs-lookup"><span data-stu-id="070df-111">Example</span></span>



| <span data-ttu-id="070df-112">ICE26 錯誤</span><span class="sxs-lookup"><span data-stu-id="070df-112">ICE26 error</span></span>                                                                   | <span data-ttu-id="070df-113">Description</span><span class="sxs-lookup"><span data-stu-id="070df-113">Description</span></span>                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070df-114">動作： InstallExecuteSequence 順序資料表中必須有 ' Action1 '。</span><span class="sxs-lookup"><span data-stu-id="070df-114">Action: 'Action1' is required in the InstallExecuteSequence Sequence table.</span></span>   | <span data-ttu-id="070df-115">指定的順序資料表中遺漏必要的動作。</span><span class="sxs-lookup"><span data-stu-id="070df-115">A required action is missing from the indicated sequence table.</span></span> <span data-ttu-id="070df-116">請參閱 [使用順序資料表](using-a-sequence-table.md)中的 template.msi 或建議的順序資料表。</span><span class="sxs-lookup"><span data-stu-id="070df-116">See the template.msi or the suggested sequence tables in [Using a Sequence Table](using-a-sequence-table.md).</span></span> |
| <span data-ttu-id="070df-117">動作： InstallExecuteSequence 順序資料表中禁止 ' Action2 '。</span><span class="sxs-lookup"><span data-stu-id="070df-117">Action: 'Action2' is prohibited in the InstallExecuteSequence Sequence table.</span></span> | <span data-ttu-id="070df-118">這個動作不能在指定的順序資料表中。</span><span class="sxs-lookup"><span data-stu-id="070df-118">This action cannot be in the indicated sequence table.</span></span> <span data-ttu-id="070df-119">從順序資料表中移除此動作。</span><span class="sxs-lookup"><span data-stu-id="070df-119">Remove this action from the sequence table.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="070df-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="070df-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="070df-121">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="070df-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



