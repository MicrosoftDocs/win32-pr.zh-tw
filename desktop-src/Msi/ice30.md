---
description: ICE30 會驗證封裝含相同檔案的元件安裝，絕對不會在相同的目錄中多次安裝檔案。
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983714"
---
# <a name="ice30"></a><span data-ttu-id="37e39-103">ICE30</span><span class="sxs-lookup"><span data-stu-id="37e39-103">ICE30</span></span>

<span data-ttu-id="37e39-104">ICE30 會驗證封裝含相同檔案的元件安裝，絕對不會在相同的目錄中多次安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="37e39-104">ICE30 validates that the installation of components containing the same file never installs the file more than once in the same directory.</span></span>

<span data-ttu-id="37e39-105">ICE30 會移至 [元件資料表](component-table.md) 中的每個元件，然後從 [目錄資料表](directory-table.md)判斷元件的目標目錄。</span><span class="sxs-lookup"><span data-stu-id="37e39-105">ICE30 goes to every component in the [Component table](component-table.md) and then determines the component's target directory from the [Directory table](directory-table.md).</span></span> <span data-ttu-id="37e39-106">然後，它會檢查哪些元件會安裝至相同的目標目錄。</span><span class="sxs-lookup"><span data-stu-id="37e39-106">It then checks to see which of these components install to the same target directory.</span></span> <span data-ttu-id="37e39-107">最後，它會使用 [File 資料表](file-table.md) 來確認這些元件中的檔案都沒有相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="37e39-107">Finally, it uses the [File table](file-table.md) to verify that none of the files in these components have the same name.</span></span>

<span data-ttu-id="37e39-108">ICE30 會檢查長檔名 (LFN) 和簡短檔案名 (SFN) 。</span><span class="sxs-lookup"><span data-stu-id="37e39-108">ICE30 checks both long file names (LFN) and short file names (SFN).</span></span>

<span data-ttu-id="37e39-109">ICE30 不會評估目錄解析中的屬性，因為這些屬性會在執行時間變更並改變目錄解析配置。</span><span class="sxs-lookup"><span data-stu-id="37e39-109">ICE30 does not evaluate properties in the resolution of directories because these properties can change at runtime and alter the directory resolution scheme.</span></span> <span data-ttu-id="37e39-110">這表示 ICE30 可以偵測檔案衝突，因為它們的路徑中具有相同屬性的目錄，但未偵測到兩個具有相同值的屬性所產生的衝突。</span><span class="sxs-lookup"><span data-stu-id="37e39-110">This means ICE30 can detect file collisions due to directories with the same property in their paths, but does not detect collisions resulting from two properties having the same value.</span></span>

## <a name="result"></a><span data-ttu-id="37e39-111">結果</span><span class="sxs-lookup"><span data-stu-id="37e39-111">Result</span></span>

<span data-ttu-id="37e39-112">ICE30 會針對每一對安裝相同檔案的元件，將錯誤訊息張貼至相同的目錄。</span><span class="sxs-lookup"><span data-stu-id="37e39-112">ICE30 posts an error message for each pair of components that installs the same file to the same directory.</span></span>

## <a name="example"></a><span data-ttu-id="37e39-113">範例</span><span class="sxs-lookup"><span data-stu-id="37e39-113">Example</span></span>

<span data-ttu-id="37e39-114">顯示的範例會傳回下列每個錯誤兩次。</span><span class="sxs-lookup"><span data-stu-id="37e39-114">The example shown returns each of the following errors twice.</span></span>



| <span data-ttu-id="37e39-115">ICE30 錯誤或警告</span><span class="sxs-lookup"><span data-stu-id="37e39-115">ICE30 error or warning</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="37e39-116">Description</span><span class="sxs-lookup"><span data-stu-id="37e39-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e39-117">錯誤：在 SFN 系統上，有兩個不同的元件在 ' TARGETDIR PRODUCT ' 中安裝了目標檔案 ' README.TXT. 1 ' \\ ： ' Component1 ' 和 ' Component2 '。</span><span class="sxs-lookup"><span data-stu-id="37e39-117">ERROR: The target file 'README.1st' is installed in 'TARGETDIR\\PRODUCT' by two different components on an SFN system: 'Component1' and 'Component2'.</span></span> <span data-ttu-id="37e39-118">這會中斷元件參考計數。</span><span class="sxs-lookup"><span data-stu-id="37e39-118">This breaks component reference counting.</span></span>                                                                                           | <span data-ttu-id="37e39-119">Component1 和 Component2 都有一個名為 ' READEME. 1 ' 的檔案。</span><span class="sxs-lookup"><span data-stu-id="37e39-119">Component1 and Component2 both have a file named 'READEME.1st'.</span></span> <span data-ttu-id="37e39-120">使用簡短的檔案名時，安裝程式會將 Dir1 和 Dir2 安裝至相同的目錄 TARGETDIR \\ 產品。</span><span class="sxs-lookup"><span data-stu-id="37e39-120">When using short file names, the installer installs both Dir1 and Dir2 to the same directory, TARGETDIR\\PRODUCT.</span></span><br/> <span data-ttu-id="37e39-121">ICE30 會產生兩個錯誤，每個檔案各一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="37e39-121">ICE30 generate two errors, one for each file.</span></span> <span data-ttu-id="37e39-122">在顯示錯誤位置的撰寫環境中，第一個錯誤是在檔案 [資料表](file-table.md)中的一個檔案專案，第二個是在另一個檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="37e39-122">In an authoring environment that displays error locations, the first error is at one file's entry in the [File Table](file-table.md), and the second at the location of the other file.</span></span><br/> |
| <span data-ttu-id="37e39-123">錯誤：安裝 conditionalized 元件會導致在 LFN 系統上有兩個不同元件的「TARGETDIR 通用工具」中，安裝目標檔案「讀我檔案」 \\ ： ' Component3 ' 和 ' Component4 '。</span><span class="sxs-lookup"><span data-stu-id="37e39-123">ERROR: Installation of a conditionalized component would cause the target file 'README.1st' to be installed in 'TARGETDIR\\COMMON TOOLS' by two different components on an LFN system: 'Component3' and 'Component4'.</span></span> <span data-ttu-id="37e39-124">這會中斷元件參考計數。</span><span class="sxs-lookup"><span data-stu-id="37e39-124">This would break component reference counting.</span></span>                      | <span data-ttu-id="37e39-125">Component4 在 [元件資料表](component-table.md) 的 [條件] 資料行中有一個專案，而 Component3 則否。</span><span class="sxs-lookup"><span data-stu-id="37e39-125">Component4 has an entry in the Condition column of the [Component table](component-table.md) and Component3 does not.</span></span> <span data-ttu-id="37e39-126">如果 [**VersionNT**](versionnt.md) 為 True，則會安裝 Component4，而且會發生與讀我檔案的衝突。第一次是由 Component3 安裝。</span><span class="sxs-lookup"><span data-stu-id="37e39-126">If [**VersionNT**](versionnt.md) is True, Component4 is installed, and there a collision with the Readme.1st always installed by Component3.</span></span><br/> <span data-ttu-id="37e39-127">ICE30 會產生4個錯誤，一對 SFN，一個用於 LFN。</span><span class="sxs-lookup"><span data-stu-id="37e39-127">ICE30 generates 4 errors, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |
| <span data-ttu-id="37e39-128">警告：目標檔案 ' README.TXT. 1 ' 可能在 \\ SFN 系統上由兩個不同的 conditionalized 元件安裝在「TARGETDIR 通用工具」中： ' Component4 ' 和 ' Component5 '。</span><span class="sxs-lookup"><span data-stu-id="37e39-128">WARNING: The target file 'README.1st' might be installed in 'TARGETDIR\\COMMON TOOLS' by two different conditionalized components on an SFN system: 'Component4' and 'Component5'.</span></span> <span data-ttu-id="37e39-129">如果條件不是互斥的，這會中斷元件參考計數系統。</span><span class="sxs-lookup"><span data-stu-id="37e39-129">If the conditions are not mutually exclusive, this will break the component reference counting system.</span></span> | <span data-ttu-id="37e39-130">因為 Component4 和 Component5 在 [元件資料表](component-table.md) 的條件資料行中都有專案，所以可能不會發生此檔案衝突。</span><span class="sxs-lookup"><span data-stu-id="37e39-130">Because Component4 and Component5 both have entries in the Condition column of the [Component table](component-table.md) this file collision may not occur.</span></span> <span data-ttu-id="37e39-131">ICE30 只會張貼警告，因為條件必須在安裝時決定。</span><span class="sxs-lookup"><span data-stu-id="37e39-131">ICE30 only posts a warning because the conditions must be determined at the time of the installation.</span></span><br/> <span data-ttu-id="37e39-132">ICE30 會產生4個警告，一對 SFN，一個用於 LFN。</span><span class="sxs-lookup"><span data-stu-id="37e39-132">ICE30 generates 4 warnings, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |



 

<span data-ttu-id="37e39-133">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="37e39-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="37e39-134">元件</span><span class="sxs-lookup"><span data-stu-id="37e39-134">Component</span></span>  | <span data-ttu-id="37e39-135">目錄</span><span class="sxs-lookup"><span data-stu-id="37e39-135">Directory</span></span> | <span data-ttu-id="37e39-136">條件</span><span class="sxs-lookup"><span data-stu-id="37e39-136">Condition</span></span> |
|------------|-----------|-----------|
| <span data-ttu-id="37e39-137">Component1</span><span class="sxs-lookup"><span data-stu-id="37e39-137">Component1</span></span> | <span data-ttu-id="37e39-138">Dir1</span><span class="sxs-lookup"><span data-stu-id="37e39-138">Dir1</span></span>      |           |
| <span data-ttu-id="37e39-139">Component2</span><span class="sxs-lookup"><span data-stu-id="37e39-139">Component2</span></span> | <span data-ttu-id="37e39-140">Dir2</span><span class="sxs-lookup"><span data-stu-id="37e39-140">Dir2</span></span>      |           |
| <span data-ttu-id="37e39-141">Component3</span><span class="sxs-lookup"><span data-stu-id="37e39-141">Component3</span></span> | <span data-ttu-id="37e39-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="37e39-142">Dir3</span></span>      |           |
| <span data-ttu-id="37e39-143">Component4</span><span class="sxs-lookup"><span data-stu-id="37e39-143">Component4</span></span> | <span data-ttu-id="37e39-144">Dir3</span><span class="sxs-lookup"><span data-stu-id="37e39-144">Dir3</span></span>      | <span data-ttu-id="37e39-145">VersionNT</span><span class="sxs-lookup"><span data-stu-id="37e39-145">VersionNT</span></span> |
| <span data-ttu-id="37e39-146">Component5</span><span class="sxs-lookup"><span data-stu-id="37e39-146">Component5</span></span> | <span data-ttu-id="37e39-147">Dir3</span><span class="sxs-lookup"><span data-stu-id="37e39-147">Dir3</span></span>      | <span data-ttu-id="37e39-148">Version9X</span><span class="sxs-lookup"><span data-stu-id="37e39-148">Version9X</span></span> |



 

[<span data-ttu-id="37e39-149">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="37e39-149">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="37e39-150">目錄</span><span class="sxs-lookup"><span data-stu-id="37e39-150">Directory</span></span> | <span data-ttu-id="37e39-151">上層 \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="37e39-151">Parent\_Directory</span></span> | <span data-ttu-id="37e39-152">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="37e39-152">DefaultDir</span></span>                    |
|-----------|-------------------|-------------------------------|
| <span data-ttu-id="37e39-153">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="37e39-153">SOURCEDIR</span></span> |                   | <span data-ttu-id="37e39-154">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="37e39-154">TARGETDIR</span></span>                     |
| <span data-ttu-id="37e39-155">Dir1</span><span class="sxs-lookup"><span data-stu-id="37e39-155">Dir1</span></span>      | <span data-ttu-id="37e39-156">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="37e39-156">SOURCEDIR</span></span>         | <span data-ttu-id="37e39-157">產品 \| Component1 產品：。</span><span class="sxs-lookup"><span data-stu-id="37e39-157">Product\|Component1 Product:.</span></span> |
| <span data-ttu-id="37e39-158">Dir2</span><span class="sxs-lookup"><span data-stu-id="37e39-158">Dir2</span></span>      | <span data-ttu-id="37e39-159">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="37e39-159">SOURCEDIR</span></span>         | <span data-ttu-id="37e39-160">產品：。</span><span class="sxs-lookup"><span data-stu-id="37e39-160">Product:.</span></span>                     |
| <span data-ttu-id="37e39-161">Dir3</span><span class="sxs-lookup"><span data-stu-id="37e39-161">Dir3</span></span>      | <span data-ttu-id="37e39-162">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="37e39-162">SOURCEDIR</span></span>         | <span data-ttu-id="37e39-163">常用 \| 工具：</span><span class="sxs-lookup"><span data-stu-id="37e39-163">Common\|Common Tools:</span></span>         |



 

<span data-ttu-id="37e39-164">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="37e39-164">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="37e39-165">檔案</span><span class="sxs-lookup"><span data-stu-id="37e39-165">File</span></span>  | <span data-ttu-id="37e39-166">元件\_</span><span class="sxs-lookup"><span data-stu-id="37e39-166">Component\_</span></span> | <span data-ttu-id="37e39-167">FileName</span><span class="sxs-lookup"><span data-stu-id="37e39-167">FileName</span></span>   |
|-------|-------------|------------|
| <span data-ttu-id="37e39-168">File1</span><span class="sxs-lookup"><span data-stu-id="37e39-168">File1</span></span> | <span data-ttu-id="37e39-169">Component1</span><span class="sxs-lookup"><span data-stu-id="37e39-169">Component1</span></span>  | <span data-ttu-id="37e39-170">README.TXT</span><span class="sxs-lookup"><span data-stu-id="37e39-170">README.1st</span></span> |
| <span data-ttu-id="37e39-171">File2</span><span class="sxs-lookup"><span data-stu-id="37e39-171">File2</span></span> | <span data-ttu-id="37e39-172">Component2</span><span class="sxs-lookup"><span data-stu-id="37e39-172">Component2</span></span>  | <span data-ttu-id="37e39-173">README.TXT</span><span class="sxs-lookup"><span data-stu-id="37e39-173">README.1st</span></span> |
| <span data-ttu-id="37e39-174">File3</span><span class="sxs-lookup"><span data-stu-id="37e39-174">File3</span></span> | <span data-ttu-id="37e39-175">Component3</span><span class="sxs-lookup"><span data-stu-id="37e39-175">Component3</span></span>  | <span data-ttu-id="37e39-176">README.TXT</span><span class="sxs-lookup"><span data-stu-id="37e39-176">README.1st</span></span> |
| <span data-ttu-id="37e39-177">File4</span><span class="sxs-lookup"><span data-stu-id="37e39-177">File4</span></span> | <span data-ttu-id="37e39-178">Component4</span><span class="sxs-lookup"><span data-stu-id="37e39-178">Component4</span></span>  | <span data-ttu-id="37e39-179">README.TXT</span><span class="sxs-lookup"><span data-stu-id="37e39-179">README.1st</span></span> |
| <span data-ttu-id="37e39-180">File5</span><span class="sxs-lookup"><span data-stu-id="37e39-180">File5</span></span> | <span data-ttu-id="37e39-181">Component5</span><span class="sxs-lookup"><span data-stu-id="37e39-181">Component5</span></span>  | <span data-ttu-id="37e39-182">README.TXT</span><span class="sxs-lookup"><span data-stu-id="37e39-182">README.1st</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="37e39-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="37e39-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37e39-184">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="37e39-184">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




