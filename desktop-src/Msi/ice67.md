---
description: ICE67 會檢查非公告快捷方式的目標是否屬於與快捷方式本身相同的元件，或目標群組件的屬性確定不會變更安裝位置。
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944980"
---
# <a name="ice67"></a><span data-ttu-id="01739-103">ICE67</span><span class="sxs-lookup"><span data-stu-id="01739-103">ICE67</span></span>

<span data-ttu-id="01739-104">ICE67 會檢查非公告快捷方式的目標是否屬於與快捷方式本身相同的元件，或目標群組件的屬性確定不會變更安裝位置。</span><span class="sxs-lookup"><span data-stu-id="01739-104">ICE67 checks that the target of a non-advertised shortcut belongs to the same component as the shortcut itself, or that the attributes of the target component ensure that it does not change installation locations.</span></span>

<span data-ttu-id="01739-105">如果目標群組件變更狀態且來源元件不正確，則無法修正 ICE67 回報的警告或錯誤，可能會導致快捷方式無效。</span><span class="sxs-lookup"><span data-stu-id="01739-105">Failure to fix a warning or error reported by ICE67 can cause the shortcut to be invalid if the target component changes state and the source component does not.</span></span> <span data-ttu-id="01739-106">例如，當目標檔案的元件設定為從來源執行時，將元件變更為本機的重新安裝會導致元件中包含未重新安裝快捷方式的元件。</span><span class="sxs-lookup"><span data-stu-id="01739-106">For example, when the target file's component is set to run from source, a reinstallation that changes the component to local results in the component containing the shortcut not being reinstalled.</span></span> <span data-ttu-id="01739-107">因此，快捷方式會指向不正確位置。</span><span class="sxs-lookup"><span data-stu-id="01739-107">Thus the shortcut points to an invalid location.</span></span>

<span data-ttu-id="01739-108">請注意，在某些情況下，使用不同的快捷方式元件是不可避免的。</span><span class="sxs-lookup"><span data-stu-id="01739-108">Note that in some cases, using a different component for the shortcut is unavoidable.</span></span> <span data-ttu-id="01739-109">例如，如果在使用者設定檔中建立快捷方式，並將該檔案安裝至非設定檔目錄，則您可能無法對這兩個數據使用相同的元件。</span><span class="sxs-lookup"><span data-stu-id="01739-109">For example, if the shortcut is created in the user profile and the file is installed to a non-profile directory, you may not be able to use the same component for both pieces of data.</span></span> <span data-ttu-id="01739-110"> (這會導致多使用者案例失敗，例如 [ICE57](ice57.md)) 中所述。</span><span class="sxs-lookup"><span data-stu-id="01739-110">(This results in failures in multi-user scenarios – such as those described in [ICE57](ice57.md)).</span></span> <span data-ttu-id="01739-111">在這種情況下，您可以使用已公告的快捷方式來達到您想要的行為，也可以直接確認目標群組件不能從來源執行變更為本機。</span><span class="sxs-lookup"><span data-stu-id="01739-111">In this case, you may be able to use advertised shortcuts to achieve the behavior you want, or you can simply ensure that the target component cannot change from run-from-source to local.</span></span>

## <a name="result"></a><span data-ttu-id="01739-112">結果</span><span class="sxs-lookup"><span data-stu-id="01739-112">Result</span></span>

<span data-ttu-id="01739-113">如果非公告快捷方式的目標不屬於與快捷方式本身相同的元件，或目標群組件的屬性不確定安裝位置不會變更，ICE67 會傳回錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="01739-113">ICE67 returns an error or a warning if the target of a non-advertised shortcut does not belong to the same component as the shortcut itself, or if the attributes of the target component do not ensure that the installation locations will not change.</span></span>

## <a name="example"></a><span data-ttu-id="01739-114">範例</span><span class="sxs-lookup"><span data-stu-id="01739-114">Example</span></span>

<span data-ttu-id="01739-115">ICE67 會報告下列範例所示的警告和錯誤。</span><span class="sxs-lookup"><span data-stu-id="01739-115">ICE67 reports the following warning and errors for the example shown.</span></span>

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

<span data-ttu-id="01739-116">Shortcut1 是由 Component2 所安裝，但其目標檔案 File1 是由 component1 所安裝。</span><span class="sxs-lookup"><span data-stu-id="01739-116">Shortcut1 is installed by Component2, but its target file, File1, is installed by component1.</span></span> <span data-ttu-id="01739-117">目標群組件標示為選擇性 (表示它可以是本機或從來源執行) 。</span><span class="sxs-lookup"><span data-stu-id="01739-117">The target component is marked optional (meaning that it can be local or run-from-source).</span></span> <span data-ttu-id="01739-118">可能會造成問題的其中一個可能的情況是 Component1 從來源執行變更為本機。</span><span class="sxs-lookup"><span data-stu-id="01739-118">One possible situation that would cause a problem is if Component1 changes from run-from-source to local.</span></span> <span data-ttu-id="01739-119">這會導致 Shortcut1 指向不正確位置。</span><span class="sxs-lookup"><span data-stu-id="01739-119">This would cause Shortcut1 to point to an invalid location.</span></span>

<span data-ttu-id="01739-120">若要修正此警告，請將快捷方式安裝為 Component1 的一部分，或將 Component1 標示為 LocalOnly 或 SourceOnly。</span><span class="sxs-lookup"><span data-stu-id="01739-120">To fix this warning, Install the shortcut as part of Component1, or mark Component1 as LocalOnly or SourceOnly.</span></span>

<span data-ttu-id="01739-121">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="01739-121">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="01739-122">檔案</span><span class="sxs-lookup"><span data-stu-id="01739-122">File</span></span>  | <span data-ttu-id="01739-123">元件\_</span><span class="sxs-lookup"><span data-stu-id="01739-123">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="01739-124">File1</span><span class="sxs-lookup"><span data-stu-id="01739-124">File1</span></span> | <span data-ttu-id="01739-125">Component1</span><span class="sxs-lookup"><span data-stu-id="01739-125">Component1</span></span>  |



 

<span data-ttu-id="01739-126"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="01739-126">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="01739-127">快速鍵</span><span class="sxs-lookup"><span data-stu-id="01739-127">Shortcut</span></span>  | <span data-ttu-id="01739-128">元件\_</span><span class="sxs-lookup"><span data-stu-id="01739-128">Component\_</span></span> | <span data-ttu-id="01739-129">目標</span><span class="sxs-lookup"><span data-stu-id="01739-129">Target</span></span>      |
|-----------|-------------|-------------|
| <span data-ttu-id="01739-130">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="01739-130">Shortcut1</span></span> | <span data-ttu-id="01739-131">Component2</span><span class="sxs-lookup"><span data-stu-id="01739-131">Component2</span></span>  | <span data-ttu-id="01739-132">\[\#1\]</span><span class="sxs-lookup"><span data-stu-id="01739-132">\[\#File1\]</span></span> |



 

<span data-ttu-id="01739-133">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="01739-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="01739-134">元件</span><span class="sxs-lookup"><span data-stu-id="01739-134">Component</span></span>  | <span data-ttu-id="01739-135">屬性</span><span class="sxs-lookup"><span data-stu-id="01739-135">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="01739-136">Component1</span><span class="sxs-lookup"><span data-stu-id="01739-136">Component1</span></span> | <span data-ttu-id="01739-137">2</span><span class="sxs-lookup"><span data-stu-id="01739-137">2</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="01739-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="01739-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01739-139">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="01739-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



