---
description: ICE50 會檢查是否已指定快速鍵圖示，以正確顯示並符合其目標檔案的副檔名。
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944844"
---
# <a name="ice50"></a><span data-ttu-id="2d171-103">ICE50</span><span class="sxs-lookup"><span data-stu-id="2d171-103">ICE50</span></span>

<span data-ttu-id="2d171-104">ICE50 會檢查是否已指定快速鍵圖示，以正確顯示並符合其目標檔案的副檔名。</span><span class="sxs-lookup"><span data-stu-id="2d171-104">ICE50 checks that shortcut icons are specified to display correctly and match their target file's extension.</span></span>

## <a name="result"></a><span data-ttu-id="2d171-105">結果</span><span class="sxs-lookup"><span data-stu-id="2d171-105">Result</span></span>

<span data-ttu-id="2d171-106">如果圖示和目標檔案的副檔名不相符，ICE50 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2d171-106">ICE50 posts an error message if the extension of the icon and target files do not match.</span></span> <span data-ttu-id="2d171-107">如果圖示儲存在沒有 .exe 或 .ico 副檔名的檔案中，ICE50 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="2d171-107">ICE50 posts a warning if icons are stored in files that do not have an .exe or .ico extension.</span></span>

## <a name="example"></a><span data-ttu-id="2d171-108">範例</span><span class="sxs-lookup"><span data-stu-id="2d171-108">Example</span></span>

<span data-ttu-id="2d171-109">ICE50 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d171-109">ICE50 reports the following error for the example shown.</span></span>



| <span data-ttu-id="2d171-110">ICE50 錯誤或警告</span><span class="sxs-lookup"><span data-stu-id="2d171-110">ICE50 error or warning</span></span>                                                                                                              | <span data-ttu-id="2d171-111">Description</span><span class="sxs-lookup"><span data-stu-id="2d171-111">Description</span></span>                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d171-112">快速鍵 ' Shortcut2 ' 的圖示 ' Icon2 ' 副檔名不符合元件 ' Component2 ' 的金鑰檔延伸。</span><span class="sxs-lookup"><span data-stu-id="2d171-112">The extension of Icon 'Icon2.dat' for Shortcut 'Shortcut2' does not match the extension of the Key File for component 'Component2'.</span></span> | <span data-ttu-id="2d171-113">如果圖示和目標檔案的副檔名不相符，則在公告元件時，快捷方式將不會有正確的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="2d171-113">If the extensions of the icon and the target file do not match, the shortcut will not have the correct context menu when the component is advertised.</span></span> <span data-ttu-id="2d171-114">若要修正這個錯誤，請將圖示重新命名以符合目標檔案的副檔名。</span><span class="sxs-lookup"><span data-stu-id="2d171-114">To fix this error, rename the icon to match the extension of the target file.</span></span><br/> |
| <span data-ttu-id="2d171-115">快速鍵 ' Shortcut1 ' 的圖示 ' Icon1.bat ' 副檔名不是 "exe" 或 ".ico"。</span><span class="sxs-lookup"><span data-stu-id="2d171-115">The extension of Icon 'Icon1.bat' for Shortcut 'Shortcut1' is not "exe" or "ico".</span></span> <span data-ttu-id="2d171-116">圖示將不會正確顯示。</span><span class="sxs-lookup"><span data-stu-id="2d171-116">The Icon will not be displayed correctly.</span></span>         | <span data-ttu-id="2d171-117">並非所有版本的 shell 都正確地顯示儲存在沒有 "exe" 或 ".ico" 副檔名之檔案中的圖示。</span><span class="sxs-lookup"><span data-stu-id="2d171-117">Not all versions of the shell correctly display icons stored in files that do not have extensions of "exe" or "ico".</span></span> <span data-ttu-id="2d171-118">若要修正此警告，請將圖示重新命名為 "exe" 或 ".ico" 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="2d171-118">To fix this warning, rename the icon have an extension of "exe" or "ico".</span></span><br/>                                      |



 

<span data-ttu-id="2d171-119">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="2d171-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="2d171-120">檔案</span><span class="sxs-lookup"><span data-stu-id="2d171-120">File</span></span>  | <span data-ttu-id="2d171-121">FileName</span><span class="sxs-lookup"><span data-stu-id="2d171-121">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="2d171-122">File1</span><span class="sxs-lookup"><span data-stu-id="2d171-122">File1</span></span> | <span data-ttu-id="2d171-123">File1.bat</span><span class="sxs-lookup"><span data-stu-id="2d171-123">File1.bat</span></span> |
| <span data-ttu-id="2d171-124">File2</span><span class="sxs-lookup"><span data-stu-id="2d171-124">File2</span></span> | <span data-ttu-id="2d171-125">File2.pl</span><span class="sxs-lookup"><span data-stu-id="2d171-125">File2.pl</span></span>  |



 

<span data-ttu-id="2d171-126">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="2d171-126">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="2d171-127">功能</span><span class="sxs-lookup"><span data-stu-id="2d171-127">Feature</span></span>  |
|----------|
| <span data-ttu-id="2d171-128">Feature1</span><span class="sxs-lookup"><span data-stu-id="2d171-128">Feature1</span></span> |



 

<span data-ttu-id="2d171-129">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="2d171-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="2d171-130">元件</span><span class="sxs-lookup"><span data-stu-id="2d171-130">Component</span></span>  | <span data-ttu-id="2d171-131">KeyPath</span><span class="sxs-lookup"><span data-stu-id="2d171-131">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="2d171-132">Component1</span><span class="sxs-lookup"><span data-stu-id="2d171-132">Component1</span></span> | <span data-ttu-id="2d171-133">File1</span><span class="sxs-lookup"><span data-stu-id="2d171-133">File1</span></span>   |
| <span data-ttu-id="2d171-134">Component2</span><span class="sxs-lookup"><span data-stu-id="2d171-134">Component2</span></span> | <span data-ttu-id="2d171-135">File2</span><span class="sxs-lookup"><span data-stu-id="2d171-135">File2</span></span>   |



 

[<span data-ttu-id="2d171-136">圖示表</span><span class="sxs-lookup"><span data-stu-id="2d171-136">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="2d171-137">Name</span><span class="sxs-lookup"><span data-stu-id="2d171-137">Name</span></span>      | <span data-ttu-id="2d171-138">資料</span><span class="sxs-lookup"><span data-stu-id="2d171-138">Data</span></span>            |
|-----------|-----------------|
| <span data-ttu-id="2d171-139">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="2d171-139">Icon1.bat</span></span> | <span data-ttu-id="2d171-140">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="2d171-140">\[Binary Data\]</span></span> |
| <span data-ttu-id="2d171-141">Icon2 .dat</span><span class="sxs-lookup"><span data-stu-id="2d171-141">Icon2.dat</span></span> | <span data-ttu-id="2d171-142">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="2d171-142">\[Binary Data\]</span></span> |



 

<span data-ttu-id="2d171-143"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="2d171-143">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="2d171-144">快速鍵</span><span class="sxs-lookup"><span data-stu-id="2d171-144">Shortcut</span></span>  | <span data-ttu-id="2d171-145">元件</span><span class="sxs-lookup"><span data-stu-id="2d171-145">Component</span></span>  | <span data-ttu-id="2d171-146">目標</span><span class="sxs-lookup"><span data-stu-id="2d171-146">Target</span></span>   | <span data-ttu-id="2d171-147">圖示\_</span><span class="sxs-lookup"><span data-stu-id="2d171-147">Icon\_</span></span>    |
|-----------|------------|----------|-----------|
| <span data-ttu-id="2d171-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="2d171-148">Shortcut1</span></span> | <span data-ttu-id="2d171-149">Component1</span><span class="sxs-lookup"><span data-stu-id="2d171-149">Component1</span></span> | <span data-ttu-id="2d171-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="2d171-150">Feature1</span></span> | <span data-ttu-id="2d171-151">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="2d171-151">Icon1.bat</span></span> |
| <span data-ttu-id="2d171-152">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="2d171-152">Shortcut2</span></span> | <span data-ttu-id="2d171-153">Component2</span><span class="sxs-lookup"><span data-stu-id="2d171-153">Component2</span></span> | <span data-ttu-id="2d171-154">Feature1</span><span class="sxs-lookup"><span data-stu-id="2d171-154">Feature1</span></span> | <span data-ttu-id="2d171-155">Icon2 .dat</span><span class="sxs-lookup"><span data-stu-id="2d171-155">Icon2.dat</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2d171-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d171-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d171-157">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="2d171-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




