---
description: 您必須為動詞設定登錄值，以處理使用者可以從專案中選取單一專案、多個專案或選取專案的情況。 針對此動詞支援的三種情況，動詞都需要個別的登錄值。
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: 如何使用動詞選取模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973160"
---
# <a name="how-to-employ-the-verb-selection-model"></a><span data-ttu-id="522ea-104">如何使用動詞選取模型</span><span class="sxs-lookup"><span data-stu-id="522ea-104">How to Employ the Verb Selection Model</span></span>

<span data-ttu-id="522ea-105">您必須為動詞設定登錄值，以處理使用者可以從專案中選取單一專案、多個專案或選取專案的情況。</span><span class="sxs-lookup"><span data-stu-id="522ea-105">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="522ea-106">針對此動詞支援的三種情況，動詞都需要個別的登錄值。</span><span class="sxs-lookup"><span data-stu-id="522ea-106">A verb requires separate registry values for each of these three situations that the verb supports.</span></span>

## <a name="instructions"></a><span data-ttu-id="522ea-107">指示</span><span class="sxs-lookup"><span data-stu-id="522ea-107">Instructions</span></span>


<span data-ttu-id="522ea-108">指定所有動詞的 MultiSelectModel 值。</span><span class="sxs-lookup"><span data-stu-id="522ea-108">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="522ea-109">如果未指定 MultiSelectModel 值，則會從您選擇的動詞執行類型推斷。</span><span class="sxs-lookup"><span data-stu-id="522ea-109">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="522ea-110">針對以 COM 為基礎的方法 (例如 DropTarget 和 ExecuteCommand) **播放** 程式，並假設為其他方法 **檔** 。</span><span class="sxs-lookup"><span data-stu-id="522ea-110">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>

<span data-ttu-id="522ea-111">動詞選取模型的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="522ea-111">The possible values for the verb selection model are as follows:</span></span>

1.  <span data-ttu-id="522ea-112">針對僅支援單一選取專案的動詞指定 **single** 。</span><span class="sxs-lookup"><span data-stu-id="522ea-112">Specify **Single** for verbs that support only a single selection.</span></span>
2.  <span data-ttu-id="522ea-113">針對支援任意數量專案的動詞指定 **播放** 程式。</span><span class="sxs-lookup"><span data-stu-id="522ea-113">Specify **Player** for verbs that support any number of items.</span></span>
3.  <span data-ttu-id="522ea-114">針對每個專案建立最上層視窗的動詞命令指定 **檔** 。</span><span class="sxs-lookup"><span data-stu-id="522ea-114">Specify **Document** for verbs that create a top-level window for each item.</span></span> <span data-ttu-id="522ea-115">這麼做會限制啟用的專案數目，如果使用者開啟太多視窗，則有助於避免系統資源不足。</span><span class="sxs-lookup"><span data-stu-id="522ea-115">Doing so limits the number of items that are activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

## <a name="remarks"></a><span data-ttu-id="522ea-116">備註</span><span class="sxs-lookup"><span data-stu-id="522ea-116">Remarks</span></span>

<span data-ttu-id="522ea-117">當選取的專案數目不符合動詞選取模型，或大於下表所述的預設限制時，就無法顯示該動詞。</span><span class="sxs-lookup"><span data-stu-id="522ea-117">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="522ea-118">動詞執行的類型</span><span class="sxs-lookup"><span data-stu-id="522ea-118">Type of verb implementation</span></span> | <span data-ttu-id="522ea-119">文件</span><span class="sxs-lookup"><span data-stu-id="522ea-119">Document</span></span> | <span data-ttu-id="522ea-120">播放器</span><span class="sxs-lookup"><span data-stu-id="522ea-120">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="522ea-121">舊版</span><span class="sxs-lookup"><span data-stu-id="522ea-121">Legacy</span></span>                      | <span data-ttu-id="522ea-122">15個專案</span><span class="sxs-lookup"><span data-stu-id="522ea-122">15 items</span></span> | <span data-ttu-id="522ea-123">100專案</span><span class="sxs-lookup"><span data-stu-id="522ea-123">100 items</span></span> |
| <span data-ttu-id="522ea-124">COM</span><span class="sxs-lookup"><span data-stu-id="522ea-124">COM</span></span>                         | <span data-ttu-id="522ea-125">15個專案</span><span class="sxs-lookup"><span data-stu-id="522ea-125">15 items</span></span> | <span data-ttu-id="522ea-126">沒有限制</span><span class="sxs-lookup"><span data-stu-id="522ea-126">No limit</span></span>  |



 

<span data-ttu-id="522ea-127">以下是使用 MultiSelectModel 值的範例登錄專案。</span><span class="sxs-lookup"><span data-stu-id="522ea-127">The following are example registry entries that use the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



