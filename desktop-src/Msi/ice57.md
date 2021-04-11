---
description: ICE57 會驗證個別的元件不會混用每部電腦和每個使用者的資料。 這個 ICE 自訂動作會檢查登錄專案、檔案、目錄金鑰路徑，以及非公告的快捷方式。
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194095"
---
# <a name="ice57"></a><span data-ttu-id="3bd85-104">ICE57</span><span class="sxs-lookup"><span data-stu-id="3bd85-104">ICE57</span></span>

<span data-ttu-id="3bd85-105">ICE57 會驗證個別的元件不會混用每部電腦和每個使用者的資料。</span><span class="sxs-lookup"><span data-stu-id="3bd85-105">ICE57 validates that individual components do not mix per-machine and per-user data.</span></span> <span data-ttu-id="3bd85-106">這個 ICE 自訂動作會檢查登錄專案、檔案、目錄金鑰路徑，以及非公告的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="3bd85-106">This ICE custom action checks registry entries, files, directory key paths, and non-advertised shortcuts.</span></span>

<span data-ttu-id="3bd85-107">混用相同元件中的每位使用者和每部電腦資料，可能會導致多使用者環境中的部分使用者只部分安裝元件。</span><span class="sxs-lookup"><span data-stu-id="3bd85-107">Mixing per-user and per-machine data in the same component could result in only partial installation of the component for some users in a multi-user environment.</span></span>

<span data-ttu-id="3bd85-108">請參閱 [**ALLUSERS**](allusers.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="3bd85-108">See the [**ALLUSERS**](allusers.md) property.</span></span>

## <a name="result"></a><span data-ttu-id="3bd85-109">結果</span><span class="sxs-lookup"><span data-stu-id="3bd85-109">Result</span></span>

<span data-ttu-id="3bd85-110">如果 ICE57 找到任何包含每一電腦和每個使用者登錄專案、檔案、目錄金鑰路徑或非公告快速鍵的元件，則會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bd85-110">ICE57 posts an error if it finds any component that contains both a per-machine and per-user registry entries, files, directory key paths, or non-advertised shortcuts.</span></span>

## <a name="example"></a><span data-ttu-id="3bd85-111">範例</span><span class="sxs-lookup"><span data-stu-id="3bd85-111">Example</span></span>

<span data-ttu-id="3bd85-112">針對顯示的範例 ICE57reports 下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bd85-112">ICE57reports the following errors for the example shown.</span></span>

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

<span data-ttu-id="3bd85-113">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="3bd85-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="3bd85-114">元件</span><span class="sxs-lookup"><span data-stu-id="3bd85-114">Component</span></span>  | <span data-ttu-id="3bd85-115">目錄</span><span class="sxs-lookup"><span data-stu-id="3bd85-115">Directory</span></span>  | <span data-ttu-id="3bd85-116">屬性</span><span class="sxs-lookup"><span data-stu-id="3bd85-116">Attributes</span></span> | <span data-ttu-id="3bd85-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="3bd85-117">KeyPath</span></span> |
|------------|------------|------------|---------|
| <span data-ttu-id="3bd85-118">Component1</span><span class="sxs-lookup"><span data-stu-id="3bd85-118">Component1</span></span> | <span data-ttu-id="3bd85-119">DirectoryA</span><span class="sxs-lookup"><span data-stu-id="3bd85-119">DirectoryA</span></span> | <span data-ttu-id="3bd85-120">0</span><span class="sxs-lookup"><span data-stu-id="3bd85-120">0</span></span>          | <span data-ttu-id="3bd85-121">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="3bd85-121">FileA</span></span>   |
| <span data-ttu-id="3bd85-122">Component2</span><span class="sxs-lookup"><span data-stu-id="3bd85-122">Component2</span></span> | <span data-ttu-id="3bd85-123">DirectoryA</span><span class="sxs-lookup"><span data-stu-id="3bd85-123">DirectoryA</span></span> | <span data-ttu-id="3bd85-124">4</span><span class="sxs-lookup"><span data-stu-id="3bd85-124">4</span></span>          | <span data-ttu-id="3bd85-125">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="3bd85-125">RegKeyB</span></span> |
| <span data-ttu-id="3bd85-126">Component3</span><span class="sxs-lookup"><span data-stu-id="3bd85-126">Component3</span></span> | <span data-ttu-id="3bd85-127">DirectoryA</span><span class="sxs-lookup"><span data-stu-id="3bd85-127">DirectoryA</span></span> | <span data-ttu-id="3bd85-128">0</span><span class="sxs-lookup"><span data-stu-id="3bd85-128">0</span></span>          | <span data-ttu-id="3bd85-129">FileC</span><span class="sxs-lookup"><span data-stu-id="3bd85-129">FileC</span></span>   |
| <span data-ttu-id="3bd85-130">Component4</span><span class="sxs-lookup"><span data-stu-id="3bd85-130">Component4</span></span> | <span data-ttu-id="3bd85-131">DirectoryA</span><span class="sxs-lookup"><span data-stu-id="3bd85-131">DirectoryA</span></span> | <span data-ttu-id="3bd85-132">4</span><span class="sxs-lookup"><span data-stu-id="3bd85-132">4</span></span>          | <span data-ttu-id="3bd85-133">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="3bd85-133">RegKeyD</span></span> |



 

<span data-ttu-id="3bd85-134">登錄[表](registry-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="3bd85-134">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="3bd85-135">登錄</span><span class="sxs-lookup"><span data-stu-id="3bd85-135">Registry</span></span> | <span data-ttu-id="3bd85-136">Root</span><span class="sxs-lookup"><span data-stu-id="3bd85-136">Root</span></span> | <span data-ttu-id="3bd85-137">元件\_</span><span class="sxs-lookup"><span data-stu-id="3bd85-137">Component\_</span></span> |
|----------|------|-------------|
| <span data-ttu-id="3bd85-138">RegKeyA</span><span class="sxs-lookup"><span data-stu-id="3bd85-138">RegKeyA</span></span>  | <span data-ttu-id="3bd85-139">1</span><span class="sxs-lookup"><span data-stu-id="3bd85-139">1</span></span>    | <span data-ttu-id="3bd85-140">Component1</span><span class="sxs-lookup"><span data-stu-id="3bd85-140">Component1</span></span>  |
| <span data-ttu-id="3bd85-141">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="3bd85-141">RegKeyB</span></span>  | <span data-ttu-id="3bd85-142">1</span><span class="sxs-lookup"><span data-stu-id="3bd85-142">1</span></span>    | <span data-ttu-id="3bd85-143">Component2</span><span class="sxs-lookup"><span data-stu-id="3bd85-143">Component2</span></span>  |
| <span data-ttu-id="3bd85-144">RegKeyC</span><span class="sxs-lookup"><span data-stu-id="3bd85-144">RegKeyC</span></span>  | <span data-ttu-id="3bd85-145">-1</span><span class="sxs-lookup"><span data-stu-id="3bd85-145">-1</span></span>   | <span data-ttu-id="3bd85-146">Component3</span><span class="sxs-lookup"><span data-stu-id="3bd85-146">Component3</span></span>  |
| <span data-ttu-id="3bd85-147">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="3bd85-147">RegKeyD</span></span>  | <span data-ttu-id="3bd85-148">-1</span><span class="sxs-lookup"><span data-stu-id="3bd85-148">-1</span></span>   | <span data-ttu-id="3bd85-149">Component4</span><span class="sxs-lookup"><span data-stu-id="3bd85-149">Component4</span></span>  |



 

<span data-ttu-id="3bd85-150">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="3bd85-150">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="3bd85-151">檔案</span><span class="sxs-lookup"><span data-stu-id="3bd85-151">File</span></span>  | <span data-ttu-id="3bd85-152">元件\_</span><span class="sxs-lookup"><span data-stu-id="3bd85-152">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="3bd85-153">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="3bd85-153">FileA</span></span> | <span data-ttu-id="3bd85-154">Component1</span><span class="sxs-lookup"><span data-stu-id="3bd85-154">Component1</span></span>  |
| <span data-ttu-id="3bd85-155">>fileb.docx</span><span class="sxs-lookup"><span data-stu-id="3bd85-155">FileB</span></span> | <span data-ttu-id="3bd85-156">Component2</span><span class="sxs-lookup"><span data-stu-id="3bd85-156">Component2</span></span>  |
| <span data-ttu-id="3bd85-157">FileC</span><span class="sxs-lookup"><span data-stu-id="3bd85-157">FileC</span></span> | <span data-ttu-id="3bd85-158">Component3</span><span class="sxs-lookup"><span data-stu-id="3bd85-158">Component3</span></span>  |
| <span data-ttu-id="3bd85-159">提交</span><span class="sxs-lookup"><span data-stu-id="3bd85-159">FileD</span></span> | <span data-ttu-id="3bd85-160">Component4</span><span class="sxs-lookup"><span data-stu-id="3bd85-160">Component4</span></span>  |



 

[<span data-ttu-id="3bd85-161">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="3bd85-161">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="3bd85-162">目錄</span><span class="sxs-lookup"><span data-stu-id="3bd85-162">Directory</span></span>  | <span data-ttu-id="3bd85-163">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="3bd85-163">Directory\_Parent</span></span> | <span data-ttu-id="3bd85-164">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="3bd85-164">DefaultDir</span></span> |
|------------|-------------------|------------|
| <span data-ttu-id="3bd85-165">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="3bd85-165">TARGETDIR</span></span>  |                   | <span data-ttu-id="3bd85-166">SourceDir</span><span class="sxs-lookup"><span data-stu-id="3bd85-166">SourceDir</span></span>  |
| <span data-ttu-id="3bd85-167">DirectoryA</span><span class="sxs-lookup"><span data-stu-id="3bd85-167">DirectoryA</span></span> | <span data-ttu-id="3bd85-168">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="3bd85-168">TARGETDIR</span></span>         | <span data-ttu-id="3bd85-169">DirectoryA</span><span class="sxs-lookup"><span data-stu-id="3bd85-169">DirectoryA</span></span> |



 

<span data-ttu-id="3bd85-170">若要修正錯誤，請重新組織應用程式，讓每個元件只包含每個使用者或每一電腦的資源，而不是兩者都包含。</span><span class="sxs-lookup"><span data-stu-id="3bd85-170">To fix the errors, reorganize the application such that each component contains only per-user or per-machine resources, and not both.</span></span>

<span data-ttu-id="3bd85-171">第一個錯誤訊息是張貼的，因為 Component1 包含每一電腦的 >filea.docx () ，而 HKCU 登錄機碼 RegKeyA (每個使用者) 。</span><span class="sxs-lookup"><span data-stu-id="3bd85-171">The first error message is posted because Component1 contains FileA (per-machine) and the HKCU registry key RegKeyA (per user).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bd85-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="3bd85-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bd85-173">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="3bd85-173">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



