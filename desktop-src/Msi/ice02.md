---
description: ICE02 會驗證元件、檔案和登錄資料表之間的特定參考是否互相交互。 這些參考必須是交互的，才能讓安裝程式正確地判斷元件的安裝狀態。
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689744"
---
# <a name="ice02"></a><span data-ttu-id="68285-104">ICE02</span><span class="sxs-lookup"><span data-stu-id="68285-104">ICE02</span></span>

<span data-ttu-id="68285-105">ICE02 會驗證[元件](component-table.md) [、檔案和登錄](file-table.md)[資料表之間](registry-table.md)的特定參考是否互相交互。</span><span class="sxs-lookup"><span data-stu-id="68285-105">ICE02 validates that certain references between the [Component](component-table.md), [File](file-table.md), and [Registry](registry-table.md) tables are reciprocal.</span></span> <span data-ttu-id="68285-106">這些參考必須是交互的，才能讓安裝程式正確地判斷元件的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="68285-106">These references must to be reciprocal for the installer to correctly determine the installation state of components.</span></span>

<span data-ttu-id="68285-107">安裝程式會使用元件資料表的 KeyPath 資料行，來偵測元件資料行中所列的元件是否存在。</span><span class="sxs-lookup"><span data-stu-id="68285-107">The installer uses the KeyPath column of the Component table to detect the presence of the component listed in the Component column.</span></span> <span data-ttu-id="68285-108">KeyPath 資料行包含登錄或檔案資料表中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="68285-108">The KeyPath column contains a key into the Registry or File tables.</span></span> <span data-ttu-id="68285-109">這兩個數據表都有一個元件資料 \_ 行，其中包含索引鍵的元件資料表，指向控制登錄專案或檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="68285-109">Both of these tables have a Component\_ column that contains a key back into the Component table pointing to the component that controls the registry entry or file.</span></span> <span data-ttu-id="68285-110">這些參考必須是相互參考。</span><span class="sxs-lookup"><span data-stu-id="68285-110">These references must be reciprocal.</span></span>

## <a name="result"></a><span data-ttu-id="68285-111">結果</span><span class="sxs-lookup"><span data-stu-id="68285-111">Result</span></span>

<span data-ttu-id="68285-112">如果 ICE02 發現的參考應該是交互且不是，則會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="68285-112">ICE02 posts an error message if it finds a reference that should be reciprocal and is not.</span></span>

## <a name="example"></a><span data-ttu-id="68285-113">範例</span><span class="sxs-lookup"><span data-stu-id="68285-113">Example</span></span>

<span data-ttu-id="68285-114">ICE02 會針對包含所顯示資料庫專案的 .msi 檔案張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="68285-114">ICE02 would post the following error message for a .msi file containing the database entries shown.</span></span>

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

<span data-ttu-id="68285-115">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="68285-115">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="68285-116">元件</span><span class="sxs-lookup"><span data-stu-id="68285-116">Component</span></span> | <span data-ttu-id="68285-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="68285-117">KeyPath</span></span>   |
|-----------|-----------|
| <span data-ttu-id="68285-118">紅色</span><span class="sxs-lookup"><span data-stu-id="68285-118">Red</span></span>       | <span data-ttu-id="68285-119">Red \_ File</span><span class="sxs-lookup"><span data-stu-id="68285-119">Red\_File</span></span> |
| <span data-ttu-id="68285-120">藍色</span><span class="sxs-lookup"><span data-stu-id="68285-120">Blue</span></span>      | <span data-ttu-id="68285-121">Red \_ File</span><span class="sxs-lookup"><span data-stu-id="68285-121">Red\_File</span></span> |



 

<span data-ttu-id="68285-122">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="68285-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="68285-123">File 資料行</span><span class="sxs-lookup"><span data-stu-id="68285-123">File Column</span></span> | <span data-ttu-id="68285-124">元件\_</span><span class="sxs-lookup"><span data-stu-id="68285-124">Component\_</span></span> |
|-------------|-------------|
| <span data-ttu-id="68285-125">Red \_ File</span><span class="sxs-lookup"><span data-stu-id="68285-125">Red\_File</span></span>   | <span data-ttu-id="68285-126">紅色</span><span class="sxs-lookup"><span data-stu-id="68285-126">Red</span></span>         |
| <span data-ttu-id="68285-127">Blue \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="68285-127">Blue\_File</span></span>  | <span data-ttu-id="68285-128">藍色</span><span class="sxs-lookup"><span data-stu-id="68285-128">Blue</span></span>        |



 

<span data-ttu-id="68285-129">元件 Blue 參考紅色檔案 \_ ，但紅色檔案 \_ 不是由元件藍色所控制，因此不能是 KeyPath 檔。</span><span class="sxs-lookup"><span data-stu-id="68285-129">Component Blue references Red\_File, but Red\_File is not controlled by Component Blue and therefore cannot be the KeyPath file.</span></span> <span data-ttu-id="68285-130">如果呼叫安裝程式以取得藍色的安裝狀態，則會不正確地檢查是否已 \_ 安裝 Red File。</span><span class="sxs-lookup"><span data-stu-id="68285-130">If the installer were called to get the installation state of Blue it would incorrectly check whether Red\_File was installed.</span></span> <span data-ttu-id="68285-131">將元件資料表中藍色的 KeyPath 欄位變更為 Blue \_ File 可修正錯誤。</span><span class="sxs-lookup"><span data-stu-id="68285-131">Changing the KeyPath field for Blue in the Component Table to Blue\_File fixes the error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68285-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="68285-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68285-133">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="68285-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



