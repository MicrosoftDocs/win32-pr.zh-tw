---
description: ICE82 會驗證 RegisterProduct 動作、RegisterUser 動作、PublishProduct 動作和 PublishFeatures 動作都存在於 InstallExecuteSequence 資料表中。 如果所有動作都存在，則會驗證套件。
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694251"
---
# <a name="ice82"></a><span data-ttu-id="67822-104">ICE82</span><span class="sxs-lookup"><span data-stu-id="67822-104">ICE82</span></span>

<span data-ttu-id="67822-105">ICE82 會驗證 [RegisterProduct 動作](registerproduct-action.md)、 [RegisterUser 動作](registeruser-action.md)、 [PublishProduct 動作](publishproduct-action.md)和 [PublishFeatures 動作](publishfeatures-action.md) 都存在於 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="67822-105">ICE82 validates that the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) are all present in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="67822-106">如果所有動作都存在，則會驗證套件。</span><span class="sxs-lookup"><span data-stu-id="67822-106">The package is validated if all the actions are present.</span></span>

<span data-ttu-id="67822-107">ICE82 會在 InstallExecuteSequence、InstallUISequence、AdminExecuteSequence、AdminUISequence 或 AdvtExecuteSequence 資料表中列出兩個具有相同序號的動作時張貼警告。</span><span class="sxs-lookup"><span data-stu-id="67822-107">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables .</span></span>

## <a name="result"></a><span data-ttu-id="67822-108">結果</span><span class="sxs-lookup"><span data-stu-id="67822-108">Result</span></span>

<span data-ttu-id="67822-109">ICE82 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="67822-109">ICE82 posts the following warnings.</span></span>



| <span data-ttu-id="67822-110">ICE82 警告</span><span class="sxs-lookup"><span data-stu-id="67822-110">ICE82 warning</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="67822-111">Description</span><span class="sxs-lookup"><span data-stu-id="67822-111">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67822-112">InstallExecuteSequence 資料表未包含以下所述的動作集合：缺少的動作：</span><span class="sxs-lookup"><span data-stu-id="67822-112">The InstallExecuteSequence table does not contain the set of actions mentioned below: Actions Missing:</span></span><br/> <span data-ttu-id="67822-113">發佈功能</span><span class="sxs-lookup"><span data-stu-id="67822-113">Publish Features</span></span><br/> <span data-ttu-id="67822-114">發佈產品</span><span class="sxs-lookup"><span data-stu-id="67822-114">Publish Product</span></span><br/> <span data-ttu-id="67822-115">註冊產品</span><span class="sxs-lookup"><span data-stu-id="67822-115">Register Product</span></span><br/> <span data-ttu-id="67822-116">註冊使用者</span><span class="sxs-lookup"><span data-stu-id="67822-116">Register User</span></span><br/> | <span data-ttu-id="67822-117">如果所有四個動作都不存在，則 ICE82 自訂動作會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="67822-117">ICE82 custom action posts a warning if all four actions are absent.</span></span>                                                                                                                                         |
| <span data-ttu-id="67822-118">此動作 \[ 1 \] \[ \] 在資料表3中有重複的序號 \[ 2 \] 。</span><span class="sxs-lookup"><span data-stu-id="67822-118">This action \[1\] has duplicate sequence number \[2\] in the table \[3\].</span></span>                                                                                                                                                     | <span data-ttu-id="67822-119">ICE82 會在 InstallExecuteSequence、InstallUISequence、AdminExecuteSequence、AdminUISequence 或 AdvtExecuteSequence 資料表中列出兩個具有相同序號的動作時張貼警告。</span><span class="sxs-lookup"><span data-stu-id="67822-119">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables.</span></span> |



 

<span data-ttu-id="67822-120">ICE82 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="67822-120">ICE82 posts the following errors.</span></span>



| <span data-ttu-id="67822-121">ICE82 錯誤</span><span class="sxs-lookup"><span data-stu-id="67822-121">ICE82 error</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="67822-122">Description</span><span class="sxs-lookup"><span data-stu-id="67822-122">Description</span></span>                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="67822-123">InstallExecuteSequence 應包含以下所述的所有動作，或不存在任何動作</span><span class="sxs-lookup"><span data-stu-id="67822-123">The InstallExecuteSequence should either contain all of the actions mentioned below or none of them Actions Present</span></span><br/> <List of actions present> <br/> <span data-ttu-id="67822-124">遺漏的動作：</span><span class="sxs-lookup"><span data-stu-id="67822-124">Actions Missing:</span></span><br/> <List of actions missing> <br/> | <span data-ttu-id="67822-125">如果有四個動作中有部分存在，而其他動作都不存在，ICE82 就會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="67822-125">ICE82 posts an error if some of the four actions are present and others are absent.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="67822-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="67822-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67822-127">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="67822-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




