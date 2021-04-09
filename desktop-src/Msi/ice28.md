---
description: ICE28 通常用來驗證 ForceReboot 動作是放在動作順序資料表中的特定動作群組之前或之後，而不在其中。 請參閱 ForceReboot 動作主題，以判斷組成此群組的動作。
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689743"
---
# <a name="ice28"></a><span data-ttu-id="b533e-104">ICE28</span><span class="sxs-lookup"><span data-stu-id="b533e-104">ICE28</span></span>

<span data-ttu-id="b533e-105">ICE28 通常用來驗證 ForceReboot 動作是放在動作順序資料表中的特定動作群組之前或之後，而不在其中。</span><span class="sxs-lookup"><span data-stu-id="b533e-105">ICE28 is commonly used to validate that the ForceReboot action is placed before or after, and never within, a specific group of actions in the action sequence tables.</span></span> <span data-ttu-id="b533e-106">請參閱 [ForceReboot 動作](forcereboot-action.md) 主題，以判斷組成此群組的動作。</span><span class="sxs-lookup"><span data-stu-id="b533e-106">See the [ForceReboot action](forcereboot-action.md) topic to determine the actions that comprise this group.</span></span>

<span data-ttu-id="b533e-107">ICE28 會驗證下列順序資料表中的動作：</span><span class="sxs-lookup"><span data-stu-id="b533e-107">ICE28 validates actions in the following sequence tables:</span></span>

[<span data-ttu-id="b533e-108">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="b533e-108">AdminUISequence table</span></span>](adminuisequence-table.md)

[<span data-ttu-id="b533e-109">AdminExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="b533e-109">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)

[<span data-ttu-id="b533e-110">InstallUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="b533e-110">InstallUISequence table</span></span>](installuisequence-table.md)

[<span data-ttu-id="b533e-111">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="b533e-111">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="b533e-112">結果</span><span class="sxs-lookup"><span data-stu-id="b533e-112">Result</span></span>

<span data-ttu-id="b533e-113">如果在指定的動作群組內排序 ForceReboot，ICE28 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b533e-113">ICE28 posts an error message if ForceReboot is sequenced within the specified action group.</span></span>

## <a name="example"></a><span data-ttu-id="b533e-114">範例</span><span class="sxs-lookup"><span data-stu-id="b533e-114">Example</span></span>

<span data-ttu-id="b533e-115">如範例所示，ICE28 會張貼下列錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="b533e-115">For the example shown, ICE28 posts the following error message:</span></span>

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[<span data-ttu-id="b533e-116">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="b533e-116">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="b533e-117">動作</span><span class="sxs-lookup"><span data-stu-id="b533e-117">Action</span></span>             | <span data-ttu-id="b533e-118">順序</span><span class="sxs-lookup"><span data-stu-id="b533e-118">Sequence</span></span> |
|--------------------|----------|
| <span data-ttu-id="b533e-119">ForceReboot</span><span class="sxs-lookup"><span data-stu-id="b533e-119">ForceReboot</span></span>        | <span data-ttu-id="b533e-120">10</span><span class="sxs-lookup"><span data-stu-id="b533e-120">10</span></span>       |
| <span data-ttu-id="b533e-121">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b533e-121">RegisterMIMEInfo</span></span>   |   <span data-ttu-id="b533e-122">5</span><span class="sxs-lookup"><span data-stu-id="b533e-122">5</span></span>      |
| <span data-ttu-id="b533e-123">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b533e-123">RegisterProgIdInfo</span></span> | <span data-ttu-id="b533e-124">15</span><span class="sxs-lookup"><span data-stu-id="b533e-124">15</span></span>       |



 

<span data-ttu-id="b533e-125">指定給 ForceReboot 中斷的序號會產生錯誤，因為它位於 RegisterMIMEInfo 和 RegisterProgIdInfo 的序號之間。</span><span class="sxs-lookup"><span data-stu-id="b533e-125">The sequence number of 10 given to ForceReboot breaks generates the error, because it comes between the sequence numbers of RegisterMIMEInfo and RegisterProgIdInfo.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b533e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="b533e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b533e-127">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="b533e-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



