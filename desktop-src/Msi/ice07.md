---
description: ICE07 會驗證安裝套件是否指定將字型安裝至 FontsFolder。 如果字型安裝在 FontsFolder 以外的資料夾中，安裝程式會建立快捷方式，而不是實際安裝字型。
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996816"
---
# <a name="ice07"></a><span data-ttu-id="212f5-104">ICE07</span><span class="sxs-lookup"><span data-stu-id="212f5-104">ICE07</span></span>

<span data-ttu-id="212f5-105">ICE07 會驗證安裝套件是否指定將字型安裝至 FontsFolder。</span><span class="sxs-lookup"><span data-stu-id="212f5-105">ICE07 validates that installation package specifies that fonts be installed into the FontsFolder.</span></span> <span data-ttu-id="212f5-106">如果字型安裝在 FontsFolder 以外的資料夾中，安裝程式會建立快捷方式，而不是實際安裝字型。</span><span class="sxs-lookup"><span data-stu-id="212f5-106">If a font is installed to a folder other than the FontsFolder the installer creates a shortcut rather than actually installing the font.</span></span>

<span data-ttu-id="212f5-107">ICE07 自訂動作會針對 [字型資料表](font-table.md)中的每個字型執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="212f5-107">The ICE07 custom action does the following for each font in the [Font table](font-table.md).</span></span>

1.  <span data-ttu-id="212f5-108">使用 [字型表格](font-table.md)尋找每個字型標題所屬的字型檔案。</span><span class="sxs-lookup"><span data-stu-id="212f5-108">Finds the font file to which each font title belongs using the [Font table](font-table.md).</span></span>
2.  <span data-ttu-id="212f5-109">查詢檔案資料表的元件資料 \_ 行，以控制每個檔案的元件。 [](file-table.md)</span><span class="sxs-lookup"><span data-stu-id="212f5-109">Queries the Component\_ column of the [File table](file-table.md) for the component that controls each file.</span></span>
3.  <span data-ttu-id="212f5-110">查詢 \_ [元件資料表](component-table.md) 的目錄資料行，以取得目錄資料表中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="212f5-110">Queries the Directory\_ column of the [Component table](component-table.md) to obtain a key into the Directory table.</span></span>
4.  <span data-ttu-id="212f5-111">解析 [目錄表](directory-table.md) ，以判斷安裝程式用來安裝字型檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="212f5-111">Resolves the [Directory table](directory-table.md) to determine the name of the folder into which the installer is to install the font file</span></span>
5.  <span data-ttu-id="212f5-112">如果字型檔案安裝在 FontsFolder 以外的資料夾中，則會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="212f5-112">Posts an error if the font file is being installed into a folder other than the FontsFolder.</span></span>

## <a name="result"></a><span data-ttu-id="212f5-113">結果</span><span class="sxs-lookup"><span data-stu-id="212f5-113">Result</span></span>

<span data-ttu-id="212f5-114">如果 ICE07 發現資料庫指定將字型檔案安裝到 FontsFolder 以外的資料夾中，則會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="212f5-114">ICE07 posts an error if it finds that the database specifies that a font file be installed into a folder other than the FontsFolder.</span></span>

## <a name="example"></a><span data-ttu-id="212f5-115">範例</span><span class="sxs-lookup"><span data-stu-id="212f5-115">Example</span></span>

<span data-ttu-id="212f5-116">IC07 會針對所顯示的範例張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="212f5-116">IC07 would post the following error message for the example shown.</span></span>

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[<span data-ttu-id="212f5-117">字型資料表</span><span class="sxs-lookup"><span data-stu-id="212f5-117">Font Table</span></span>](font-table.md)



| <span data-ttu-id="212f5-118">檔案\_</span><span class="sxs-lookup"><span data-stu-id="212f5-118">File\_</span></span> | <span data-ttu-id="212f5-119">FontTitle</span><span class="sxs-lookup"><span data-stu-id="212f5-119">FontTitle</span></span> |
|--------|-----------|
| <span data-ttu-id="212f5-120">默特爾</span><span class="sxs-lookup"><span data-stu-id="212f5-120">Myrtle</span></span> | <span data-ttu-id="212f5-121">Tahoma</span><span class="sxs-lookup"><span data-stu-id="212f5-121">Tahoma</span></span>    |



 

<span data-ttu-id="212f5-122">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="212f5-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="212f5-123">檔案</span><span class="sxs-lookup"><span data-stu-id="212f5-123">File</span></span>   | <span data-ttu-id="212f5-124">元件\_</span><span class="sxs-lookup"><span data-stu-id="212f5-124">Component\_</span></span>   |
|--------|---------------|
| <span data-ttu-id="212f5-125">默特爾</span><span class="sxs-lookup"><span data-stu-id="212f5-125">Myrtle</span></span> | <span data-ttu-id="212f5-126">Myrtle \_ 海灘</span><span class="sxs-lookup"><span data-stu-id="212f5-126">Myrtle\_Beach</span></span> |



 

<span data-ttu-id="212f5-127">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="212f5-127">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="212f5-128">元件</span><span class="sxs-lookup"><span data-stu-id="212f5-128">Component</span></span>     | <span data-ttu-id="212f5-129">目錄\_</span><span class="sxs-lookup"><span data-stu-id="212f5-129">Directory\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="212f5-130">Myrtle \_ 海灘</span><span class="sxs-lookup"><span data-stu-id="212f5-130">Myrtle\_Beach</span></span> | <span data-ttu-id="212f5-131">沙洲</span><span class="sxs-lookup"><span data-stu-id="212f5-131">SandBar</span></span>     |



 

<span data-ttu-id="212f5-132">在此範例中，會將 Tahoma 的字型對應到字型檔案 Myrtle。</span><span class="sxs-lookup"><span data-stu-id="212f5-132">In this example, the font Tahoma maps to the font file Myrtle.</span></span> <span data-ttu-id="212f5-133">Myrtle 檔案屬於 Myrtle 海灘的元件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="212f5-133">The file Myrtle belongs to the component Myrtle\_Beach.</span></span> <span data-ttu-id="212f5-134">目錄資料表的解析會顯示屬於 Myrtle 海灘的所有檔案 \_ 都會安裝在 Sandbar 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="212f5-134">Resolution of the Directory table shows that all the files belonging to Myrtle\_Beach are to be installed in the Sandbar folder.</span></span> <span data-ttu-id="212f5-135">因為這不是 FontsFolder，所以 ICE07 會張貼一則錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="212f5-135">Because this is not the FontsFolder, ICE07 posts an error message.</span></span>

<span data-ttu-id="212f5-136">請注意，如果 Myrtle 海灘的元件 \_ 確實屬於 Sandbar 資料夾，而不是 FontsFolder，則 Tahoma 的字型可能不屬於 Myrtle \_ 海灘。</span><span class="sxs-lookup"><span data-stu-id="212f5-136">Note that if the component Myrtle\_Beach really belongs in the Sandbar folder, and not the FontsFolder, then the font Tahoma may not belong in Myrtle\_Beach.</span></span> <span data-ttu-id="212f5-137">可能的錯誤修正方式是在另一個元件中包含 Tahoma，而該元件會安裝在 FontsFolder 目錄中。</span><span class="sxs-lookup"><span data-stu-id="212f5-137">A possible fix for the error would be to include Tahoma in another component that does get installed in the FontsFolder directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="212f5-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="212f5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="212f5-139">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="212f5-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



