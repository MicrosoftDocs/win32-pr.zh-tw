---
description: ICE62 會對 IsolatedComponent 資料表執行大量檢查，以取得可能會造成非預期行為的資料。
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987683"
---
# <a name="ice62"></a><span data-ttu-id="f8ad5-103">ICE62</span><span class="sxs-lookup"><span data-stu-id="f8ad5-103">ICE62</span></span>

<span data-ttu-id="f8ad5-104">ICE62 會對 [IsolatedComponent 資料表](isolatedcomponent-table.md) 執行大量檢查，以取得可能會造成非預期行為的資料。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-104">ICE62 performs extensive checks on the [IsolatedComponent table](isolatedcomponent-table.md) for data that may cause unexpected behavior.</span></span>

<span data-ttu-id="f8ad5-105">若無法修正 ICE62 回報的錯誤，可能會以各種不同的方式導致隔離元件系統失敗。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-105">Failure to fix an error reported by ICE62 can result in a failure of the isolated component system in a wide variety of ways.</span></span> <span data-ttu-id="f8ad5-106">例如，如果未設定共用元件的 SharedDllRefCount 位，當另一個應用程式使用該配置器且已卸載時，就可以移除元件的註冊。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-106">For example, if the SharedDllRefCount bit is not set for a shared component, the registration for the component could be removed when another application uses that ComponentId and is uninstalled.</span></span>

## <a name="result"></a><span data-ttu-id="f8ad5-107">結果</span><span class="sxs-lookup"><span data-stu-id="f8ad5-107">Result</span></span>

<span data-ttu-id="f8ad5-108">當 ICE62 在 IsolatedComponent 資料表中找到可能會產生非預期行為的資料時，會張貼警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-108">ICE62 posts a warning or error when it finds data in the IsolatedComponent table that may produce unexpected behavior.</span></span>

## <a name="example"></a><span data-ttu-id="f8ad5-109">範例</span><span class="sxs-lookup"><span data-stu-id="f8ad5-109">Example</span></span>

<span data-ttu-id="f8ad5-110">ICE62 會針對所顯示的範例報告下列錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-110">ICE62 reports the following errors and warning for the examples shown.</span></span>

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

<span data-ttu-id="f8ad5-111">Component2 會列為隔離 component1 的應用程式元件。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-111">Component2 is listed as the application component for the isolation of component1.</span></span> <span data-ttu-id="f8ad5-112">不過，Component2 有一個登錄機碼路徑，而且不提供可用於隔離元件的有效可執行檔路徑。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-112">However, Component2 has a registry key path, and does not provide a valid executable path to use to isolate the component.</span></span>

<span data-ttu-id="f8ad5-113">若要修正這個錯誤，請使用不同的元件作為隔離元件 Component1 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-113">To fix this error, use a different component as the application for the isolated component Component1.</span></span>

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

<span data-ttu-id="f8ad5-114">Component1 列為隔離的共用元件，但未設定 SharedDllRefCount 位。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-114">Component1 is listed as an isolated shared component, but does not have the SharedDllRefCount bit set.</span></span> <span data-ttu-id="f8ad5-115">這可能會導致元件的存留期不正確。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-115">This could result in the lifetime of the component being incorrect.</span></span> <span data-ttu-id="f8ad5-116">如果另一個應用程式使用此元件 (隔離或未) 並已卸載，則會移除該元件的註冊，但會保留此應用程式的獨立複本。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-116">If another application uses this component (isolated or not) and is uninstalled, the registration for the component is removed but this application's isolated copy remains.</span></span> <span data-ttu-id="f8ad5-117">這會導致修復和卸載問題。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-117">This causes repair and uninstall problems.</span></span>

<span data-ttu-id="f8ad5-118">若要修正這個錯誤，請設定元件的 SharedDllRefCount 位。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-118">To fix this error, set the SharedDllRefCount bit for the component.</span></span>

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

<span data-ttu-id="f8ad5-119">Component1 和 Component2 是由不同的功能所安裝。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-119">Component1 and Component2 are installed by different features.</span></span> <span data-ttu-id="f8ad5-120">Component1 是由 Feature1 所安裝，而 Component2 則是由 Feature2 安裝。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-120">Component1 is installed by Feature1, and Component2 is installed by Feature2.</span></span> <span data-ttu-id="f8ad5-121">Feature1 不是 Feature2 的父系，因此可能會安裝應用程式，而不是隔離的元件，進而中斷隔離。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-121">Feature1 is not a parent of Feature2, hence it is possible for the application to be installed but not the isolated component, breaking the isolation.</span></span>

<span data-ttu-id="f8ad5-122">若要修正這個錯誤，請將專案加入至 FeatureComponents 資料表，以將 Component1 連結至 (的相同功能，或) 安裝 Component2 之功能的父功能。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-122">To fix this error, add an entry to the FeatureComponents table linking Component1 to the same feature as (or a parent feature of) the feature that installs Component2.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

<span data-ttu-id="f8ad5-123">Component1 在元件資料表中有條件。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-123">Component1 has a condition in the Component table.</span></span> <span data-ttu-id="f8ad5-124">如果在電腦上安裝的存留期內，此情況的變更為 FALSE，則隔離的元件可能會在沒有註冊資訊的情況下孤立。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-124">If this condition ever changes from TRUE to FALSE during the lifetime of an installation on a computer, the isolated component could be orphaned without registration information.</span></span>

<span data-ttu-id="f8ad5-125">若要修正這個警告，請移除條件，或撰寫條件，讓它永遠不會從 TRUE 變更為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-125">To fix this warning, remove the condition, or author the condition so that it can never change from TRUE to FALSE.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

<span data-ttu-id="f8ad5-126">Component1 會針對 Component2 和 Component3 隔離，而這兩個元件也會安裝在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-126">Component1 is isolated for both Component2 and Component3, and the two components are also installed to the same directory.</span></span> <span data-ttu-id="f8ad5-127">應用程式會共用隔離的元件，但如果移除一個應用程式，則會移除共用的元件，也會導致其他應用程式遺失隔離的元件。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-127">The applications share an isolated component, but if one application is removed the shared component is removed as well causing the other applications to lose the isolated component.</span></span>

<span data-ttu-id="f8ad5-128">若要修正此警告，請將應用程式安裝到不同的目錄，或檢查是否有一些應用程式確實需要隔離的元件。</span><span class="sxs-lookup"><span data-stu-id="f8ad5-128">To fix this warning, install the applications to different directories or check whether some of the applications truly require an isolated component.</span></span>

[<span data-ttu-id="f8ad5-129">IsolatedComponent 資料表</span><span class="sxs-lookup"><span data-stu-id="f8ad5-129">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="f8ad5-130">元件 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="f8ad5-130">Component\_Shared</span></span> | <span data-ttu-id="f8ad5-131">元件 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="f8ad5-131">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="f8ad5-132">Component1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-132">Component1</span></span>        | <span data-ttu-id="f8ad5-133">Component2</span><span class="sxs-lookup"><span data-stu-id="f8ad5-133">Component2</span></span>             |
| <span data-ttu-id="f8ad5-134">Component1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-134">Component1</span></span>        | <span data-ttu-id="f8ad5-135">Component3</span><span class="sxs-lookup"><span data-stu-id="f8ad5-135">Component3</span></span>             |



 

[<span data-ttu-id="f8ad5-136">元件資料表</span><span class="sxs-lookup"><span data-stu-id="f8ad5-136">Component Table</span></span>](component-table.md)



| <span data-ttu-id="f8ad5-137">元件</span><span class="sxs-lookup"><span data-stu-id="f8ad5-137">Component</span></span>  | <span data-ttu-id="f8ad5-138">ComponentId</span><span class="sxs-lookup"><span data-stu-id="f8ad5-138">ComponentId</span></span> | <span data-ttu-id="f8ad5-139">目錄\_</span><span class="sxs-lookup"><span data-stu-id="f8ad5-139">Directory\_</span></span> | <span data-ttu-id="f8ad5-140">屬性</span><span class="sxs-lookup"><span data-stu-id="f8ad5-140">Attributes</span></span> | <span data-ttu-id="f8ad5-141">條件</span><span class="sxs-lookup"><span data-stu-id="f8ad5-141">Condition</span></span>   | <span data-ttu-id="f8ad5-142">KeyPath</span><span class="sxs-lookup"><span data-stu-id="f8ad5-142">KeyPath</span></span>   |
|------------|-------------|-------------|------------|-------------|-----------|
| <span data-ttu-id="f8ad5-143">Component1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-143">Component1</span></span> |             | <span data-ttu-id="f8ad5-144">Dir1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-144">Dir1</span></span>        | <span data-ttu-id="f8ad5-145">0</span><span class="sxs-lookup"><span data-stu-id="f8ad5-145">0</span></span>          | <span data-ttu-id="f8ad5-146">MYCONDITION</span><span class="sxs-lookup"><span data-stu-id="f8ad5-146">MYCONDITION</span></span> | <span data-ttu-id="f8ad5-147">File1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-147">File1</span></span>     |
| <span data-ttu-id="f8ad5-148">Component2</span><span class="sxs-lookup"><span data-stu-id="f8ad5-148">Component2</span></span> |             | <span data-ttu-id="f8ad5-149">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="f8ad5-149">TARGETDIR</span></span>   | <span data-ttu-id="f8ad5-150">4</span><span class="sxs-lookup"><span data-stu-id="f8ad5-150">4</span></span>          |             | <span data-ttu-id="f8ad5-151">Registry2</span><span class="sxs-lookup"><span data-stu-id="f8ad5-151">Registry2</span></span> |
| <span data-ttu-id="f8ad5-152">Component3</span><span class="sxs-lookup"><span data-stu-id="f8ad5-152">Component3</span></span> |             | <span data-ttu-id="f8ad5-153">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="f8ad5-153">TARGETDIR</span></span>   | <span data-ttu-id="f8ad5-154">0</span><span class="sxs-lookup"><span data-stu-id="f8ad5-154">0</span></span>          |             | <span data-ttu-id="f8ad5-155">File3</span><span class="sxs-lookup"><span data-stu-id="f8ad5-155">File3</span></span>     |



 

[<span data-ttu-id="f8ad5-156">FeatureComponentsTable</span><span class="sxs-lookup"><span data-stu-id="f8ad5-156">FeatureComponentsTable</span></span>](featurecomponents-table.md)



| <span data-ttu-id="f8ad5-157">功能\_</span><span class="sxs-lookup"><span data-stu-id="f8ad5-157">Feature\_</span></span> | <span data-ttu-id="f8ad5-158">元件\_</span><span class="sxs-lookup"><span data-stu-id="f8ad5-158">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="f8ad5-159">Feature1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-159">Feature1</span></span>  | <span data-ttu-id="f8ad5-160">Component1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-160">Component1</span></span>  |
| <span data-ttu-id="f8ad5-161">Feature2</span><span class="sxs-lookup"><span data-stu-id="f8ad5-161">Feature2</span></span>  | <span data-ttu-id="f8ad5-162">Component2</span><span class="sxs-lookup"><span data-stu-id="f8ad5-162">Component2</span></span>  |
| <span data-ttu-id="f8ad5-163">Feature1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-163">Feature1</span></span>  | <span data-ttu-id="f8ad5-164">Component3</span><span class="sxs-lookup"><span data-stu-id="f8ad5-164">Component3</span></span>  |



 

<span data-ttu-id="f8ad5-165">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f8ad5-165">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="f8ad5-166">功能</span><span class="sxs-lookup"><span data-stu-id="f8ad5-166">Feature</span></span>  | <span data-ttu-id="f8ad5-167">功能 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="f8ad5-167">Feature\_Parent</span></span> |
|----------|-----------------|
| <span data-ttu-id="f8ad5-168">Feature1</span><span class="sxs-lookup"><span data-stu-id="f8ad5-168">Feature1</span></span> |                 |
| <span data-ttu-id="f8ad5-169">Feature2</span><span class="sxs-lookup"><span data-stu-id="f8ad5-169">Feature2</span></span> |                 |



 

## <a name="related-topics"></a><span data-ttu-id="f8ad5-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8ad5-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8ad5-171">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="f8ad5-171">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



