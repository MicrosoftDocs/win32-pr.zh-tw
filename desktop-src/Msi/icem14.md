---
description: ICEM14 會驗證 ModuleSubstitution 資料表的 Value 資料行。
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114332"
---
# <a name="icem14"></a><span data-ttu-id="2d151-103">ICEM14</span><span class="sxs-lookup"><span data-stu-id="2d151-103">ICEM14</span></span>

<span data-ttu-id="2d151-104">ICEM14 會驗證 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 Value 資料行。</span><span class="sxs-lookup"><span data-stu-id="2d151-104">ICEM14 validates the Value Column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="2d151-105">結果</span><span class="sxs-lookup"><span data-stu-id="2d151-105">Result</span></span>

<span data-ttu-id="2d151-106">ICEM14 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d151-106">ICEM14 posts the following errors.</span></span>



| <span data-ttu-id="2d151-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="2d151-107">Error</span></span>                                                                                                                                                         | <span data-ttu-id="2d151-108">意義</span><span class="sxs-lookup"><span data-stu-id="2d151-108">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d151-109">資料列 \[ 1 \] \[ 中 ModuleSubstitution 資料行的取代字串。2 \] . \[\]在 ModuleConfiguration 資料表中找不到3。</span><span class="sxs-lookup"><span data-stu-id="2d151-109">The replacement string in ModuleSubstitution.Value column in row \[1\].\[2\].\[3\] is not found in ModuleConfiguration table.</span></span>                                 | <span data-ttu-id="2d151-110">\[1 \] . \[2 \] . \[3 \] 指的是 ModuleSubstitution 資料表中資料 *列的資料表.* 資料行主鍵。</span><span class="sxs-lookup"><span data-stu-id="2d151-110">\[1\].\[2\].\[3\] refers to a *table.row.column* primary key for a row in the ModuleSubstitution table.</span></span> <span data-ttu-id="2d151-111">此資料列的 [值] 欄位中的格式化範本未對應至 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中可設定屬性的資料列。</span><span class="sxs-lookup"><span data-stu-id="2d151-111">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                            |
| <span data-ttu-id="2d151-112">在第1列的 ModuleSubstitution 資料表中 \[ \] 。 \[2 \] . \[3 \] ，資料表 '% s ' 中指出可設定的專案。</span><span class="sxs-lookup"><span data-stu-id="2d151-112">In ModuleSubstitution table in row \[1\].\[2\].\[3\], a configurable item is indicated in the table '%s'.</span></span> <span data-ttu-id="2d151-113">資料表 '% s ' 不能包含可設定的專案。</span><span class="sxs-lookup"><span data-stu-id="2d151-113">The table '%s' must not contain configurable items.</span></span> | <span data-ttu-id="2d151-114">下列其中一個資料表列在 ModuleSubstitution 資料表的資料表資料行中： [ModuleSubstitution](modulesubstitution-table.md)、 [ModuleConfiguration](moduleconfiguration-table.md)、 [ModuleExclusion](moduleexclusion-table.md)或 [ModuleSignature](modulesignature-table.md)。</span><span class="sxs-lookup"><span data-stu-id="2d151-114">One of the following tables is listed in the Table column of the ModuleSubstitution table: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md), or [ModuleSignature](modulesignature-table.md).</span></span> <span data-ttu-id="2d151-115">這些資料表不能包含可設定的欄位。</span><span class="sxs-lookup"><span data-stu-id="2d151-115">These tables cannot contain configurable fields.</span></span> |
| <span data-ttu-id="2d151-116">在第1列的 ModuleSubstitution 資料表中 \[ \] 。 \[2 \] . \[3 \] ，指定空的取代字串。</span><span class="sxs-lookup"><span data-stu-id="2d151-116">In ModuleSubstitution table in row \[1\].\[2\].\[3\], an empty replacement string is specified.</span></span>                                                               | <span data-ttu-id="2d151-117">此資料列的 [值] 欄位中的格式化範本未對應至 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中可設定屬性的資料列。</span><span class="sxs-lookup"><span data-stu-id="2d151-117">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="2d151-118">ICEM14 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="2d151-118">ICEM14 posts the following warning.</span></span>



| <span data-ttu-id="2d151-119">警告</span><span class="sxs-lookup"><span data-stu-id="2d151-119">Warning</span></span>                                                                  | <span data-ttu-id="2d151-120">意義</span><span class="sxs-lookup"><span data-stu-id="2d151-120">Meaning</span></span>                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="2d151-121">存在 ModuleSubstitution 資料表，但遺漏 ModuleConfiguration 資料表</span><span class="sxs-lookup"><span data-stu-id="2d151-121">ModuleSubstitution table exists but ModuleConfiguration table is missing</span></span> | <span data-ttu-id="2d151-122">ModuleConfiguration 資料表不存在。</span><span class="sxs-lookup"><span data-stu-id="2d151-122">The ModuleConfiguration table is absent.</span></span> |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="2d151-123">執行期間所使用的資料表</span><span class="sxs-lookup"><span data-stu-id="2d151-123">Table Used During Execution</span></span>

[<span data-ttu-id="2d151-124">ModuleSubstitution 資料表</span><span class="sxs-lookup"><span data-stu-id="2d151-124">ModuleSubstitution table</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="2d151-125">ModuleConfiguration 資料表</span><span class="sxs-lookup"><span data-stu-id="2d151-125">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)

## <a name="related-topics"></a><span data-ttu-id="2d151-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d151-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d151-127">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="2d151-127">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



