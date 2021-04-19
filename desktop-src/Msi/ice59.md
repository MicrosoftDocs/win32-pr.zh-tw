---
description: ICE59 檢查公告的快捷方式屬於快捷方式的目標功能所安裝的元件。
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975048"
---
# <a name="ice59"></a><span data-ttu-id="8857b-103">ICE59</span><span class="sxs-lookup"><span data-stu-id="8857b-103">ICE59</span></span>

<span data-ttu-id="8857b-104">ICE59 檢查公告的快捷方式屬於快捷方式的目標功能所安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="8857b-104">ICE59 checks that advertised shortcuts belong to components that are installed by the target feature of the shortcut.</span></span>

<span data-ttu-id="8857b-105">ICE59 回報的錯誤通常會導致下列行為：</span><span class="sxs-lookup"><span data-stu-id="8857b-105">Errors reported by ICE59 generally lead to the following behavior:</span></span>

1.  <span data-ttu-id="8857b-106">通告的快捷方式會啟動 Windows Installer，以安裝 [目標] 資料行中所列的功能。</span><span class="sxs-lookup"><span data-stu-id="8857b-106">The advertised shortcut will launch the Windows Installer to install the feature listed in the Target column.</span></span>
2.  <span data-ttu-id="8857b-107">但是，由於 [FeatureComponents 資料表](featurecomponents-table.md) 不會將目標功能對應到包含快捷方式的元件，因此不會安裝快捷方式) 所啟用之元件 (的 keyfile。</span><span class="sxs-lookup"><span data-stu-id="8857b-107">But because the [FeatureComponents table](featurecomponents-table.md) does not map the target feature to the component containing the shortcut, the keyfile of the component (which is activated by the shortcut) is not installed.</span></span>
3.  <span data-ttu-id="8857b-108">因此，快捷方式會中斷，且不會進行任何動作。</span><span class="sxs-lookup"><span data-stu-id="8857b-108">Therefore the shortcut is broken and will not do anything.</span></span>

## <a name="result"></a><span data-ttu-id="8857b-109">結果</span><span class="sxs-lookup"><span data-stu-id="8857b-109">Result</span></span>

<span data-ttu-id="8857b-110">如果公告的快捷方式不屬於快捷方式的目標功能所安裝的元件，ICE59 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="8857b-110">ICE59 posts an error if an advertised shortcut does not belong to the components that are installed by the target feature of the shortcut.</span></span>

## <a name="example"></a><span data-ttu-id="8857b-111">範例</span><span class="sxs-lookup"><span data-stu-id="8857b-111">Example</span></span>

<span data-ttu-id="8857b-112">ICE59 會針對所顯示的範例報告下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="8857b-112">ICE59 reports the following error for the example shown:</span></span>

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

<span data-ttu-id="8857b-113">在此情況下，ShortcutB 會通告 FeatureA，啟動時，會啟動 ComponentB 的金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="8857b-113">In this case, ShortcutB advertises FeatureA, and when activated, starts the key file of ComponentB.</span></span> <span data-ttu-id="8857b-114">但 FeatureA 永遠不會安裝 ComponentB，因此即使在隨選安裝階段完成後，快速鍵的目標也不存在。</span><span class="sxs-lookup"><span data-stu-id="8857b-114">Yet ComponentB is never installed by FeatureA, so even after the installation-on-demand phase completes, the target of the shortcut does not exist.</span></span>

<span data-ttu-id="8857b-115">若要修正這個錯誤，請將資料列加入至關聯 FeatureA 和 ComponentB 的 [FeatureComponents 資料表](featurecomponents-table.md) 中。</span><span class="sxs-lookup"><span data-stu-id="8857b-115">To fix this error, add a row to the [FeatureComponents table](featurecomponents-table.md) that associates FeatureA and ComponentB.</span></span>

<span data-ttu-id="8857b-116"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="8857b-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="8857b-117">快速鍵</span><span class="sxs-lookup"><span data-stu-id="8857b-117">Shortcut</span></span>  | <span data-ttu-id="8857b-118">目標</span><span class="sxs-lookup"><span data-stu-id="8857b-118">Target</span></span>   | <span data-ttu-id="8857b-119">元件\_</span><span class="sxs-lookup"><span data-stu-id="8857b-119">Component\_</span></span> |
|-----------|----------|-------------|
| <span data-ttu-id="8857b-120">ShortcutB</span><span class="sxs-lookup"><span data-stu-id="8857b-120">ShortcutB</span></span> | <span data-ttu-id="8857b-121">FeatureA</span><span class="sxs-lookup"><span data-stu-id="8857b-121">FeatureA</span></span> | <span data-ttu-id="8857b-122">ComponentB</span><span class="sxs-lookup"><span data-stu-id="8857b-122">ComponentB</span></span>  |



 

[<span data-ttu-id="8857b-123">FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="8857b-123">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="8857b-124">功能\_</span><span class="sxs-lookup"><span data-stu-id="8857b-124">Feature\_</span></span> | <span data-ttu-id="8857b-125">元件\_</span><span class="sxs-lookup"><span data-stu-id="8857b-125">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="8857b-126">FeatureA</span><span class="sxs-lookup"><span data-stu-id="8857b-126">FeatureA</span></span>  | <span data-ttu-id="8857b-127">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8857b-127">ComponentA</span></span>  |



 

<span data-ttu-id="8857b-128">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="8857b-128">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="8857b-129">功能</span><span class="sxs-lookup"><span data-stu-id="8857b-129">Feature</span></span>  | <span data-ttu-id="8857b-130">層級</span><span class="sxs-lookup"><span data-stu-id="8857b-130">Level</span></span> |
|----------|-------|
| <span data-ttu-id="8857b-131">FeatureA</span><span class="sxs-lookup"><span data-stu-id="8857b-131">FeatureA</span></span> | <span data-ttu-id="8857b-132">10</span><span class="sxs-lookup"><span data-stu-id="8857b-132">10</span></span>    |



 

<span data-ttu-id="8857b-133">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="8857b-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="8857b-134">元件</span><span class="sxs-lookup"><span data-stu-id="8857b-134">Component</span></span>  | <span data-ttu-id="8857b-135">KeyPath</span><span class="sxs-lookup"><span data-stu-id="8857b-135">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="8857b-136">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8857b-136">ComponentA</span></span> | <span data-ttu-id="8857b-137">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="8857b-137">FileA</span></span>   |
| <span data-ttu-id="8857b-138">ComponentB</span><span class="sxs-lookup"><span data-stu-id="8857b-138">ComponentB</span></span> | <span data-ttu-id="8857b-139">>fileb.docx</span><span class="sxs-lookup"><span data-stu-id="8857b-139">FileB</span></span>   |



 

<span data-ttu-id="8857b-140">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="8857b-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="8857b-141">檔案</span><span class="sxs-lookup"><span data-stu-id="8857b-141">File</span></span>  | <span data-ttu-id="8857b-142">元件\_</span><span class="sxs-lookup"><span data-stu-id="8857b-142">Component\_</span></span> | <span data-ttu-id="8857b-143">順序</span><span class="sxs-lookup"><span data-stu-id="8857b-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="8857b-144">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="8857b-144">FileA</span></span> | <span data-ttu-id="8857b-145">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8857b-145">ComponentA</span></span>  | <span data-ttu-id="8857b-146">1</span><span class="sxs-lookup"><span data-stu-id="8857b-146">1</span></span>        |
| <span data-ttu-id="8857b-147">>fileb.docx</span><span class="sxs-lookup"><span data-stu-id="8857b-147">FileB</span></span> | <span data-ttu-id="8857b-148">ComponentB</span><span class="sxs-lookup"><span data-stu-id="8857b-148">ComponentB</span></span>  | <span data-ttu-id="8857b-149">2</span><span class="sxs-lookup"><span data-stu-id="8857b-149">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8857b-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="8857b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8857b-151">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="8857b-151">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



