---
description: ICE36 會驗證圖示資料表中的每個圖示至少在 ARPPRODUCTICON 屬性或類別、ProgId 或快速鍵資料表中列出一次。
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027024"
---
# <a name="ice36"></a><span data-ttu-id="b0824-103">ICE36</span><span class="sxs-lookup"><span data-stu-id="b0824-103">ICE36</span></span>

<span data-ttu-id="b0824-104">ICE36 會驗證圖示資料表中的每個圖示至少在 [**ARPPRODUCTICON**](arpproducticon.md) 屬性或 [類別](class-table.md)、 [ProgId](progid-table.md)或 [快速鍵](shortcut-table.md) 資料表中列出一次。</span><span class="sxs-lookup"><span data-stu-id="b0824-104">ICE36 validates that every icon in the Icon table is listed at least once in the [**ARPPRODUCTICON**](arpproducticon.md) property or the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables.</span></span>

<span data-ttu-id="b0824-105">在公告期間，安裝程式會安裝使用者電腦上 [圖示表格](icon-table.md) 中所列的所有圖示。</span><span class="sxs-lookup"><span data-stu-id="b0824-105">During advertisement, the installer installs all the icons listed in the [Icon table](icon-table.md) on the user's computer.</span></span> <span data-ttu-id="b0824-106">在圖示表格中具有未使用的圖示，並不會阻止安裝執行，不過它會不必要地增加 .msi 檔案的大小，以及通告功能所需的時間和空間。</span><span class="sxs-lookup"><span data-stu-id="b0824-106">Having unused icons in the Icon table does not prevent the installation from running, however it does unnecessarily increase the size of the .msi file and the time and space required to advertise a feature.</span></span>

<span data-ttu-id="b0824-107">如果屬性或資料表中未參考圖示，而且沒有提供 UI 可在執行時間建立參考，您應該移除圖示以達到更佳的效能。</span><span class="sxs-lookup"><span data-stu-id="b0824-107">If an icon is not referenced in the property or table and there is no UI provided to create a reference at run time, you should remove the icon to achieve better performance.</span></span>

## <a name="result"></a><span data-ttu-id="b0824-108">結果</span><span class="sxs-lookup"><span data-stu-id="b0824-108">Result</span></span>

<span data-ttu-id="b0824-109">如果未在 [類別](class-table.md)、 [ProgId](progid-table.md)或 [快捷方式](shortcut-table.md) 表中參考的圖示表格中有圖示，且未提供可在執行時間建立這類參考的 UI，ICE36 會張貼訊息。</span><span class="sxs-lookup"><span data-stu-id="b0824-109">ICE36 posts a message if there is a icon in the Icon table that is not referenced in the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables and if there is no UI provided to create such a reference at run time.</span></span>

## <a name="example"></a><span data-ttu-id="b0824-110">範例</span><span class="sxs-lookup"><span data-stu-id="b0824-110">Example</span></span>

<span data-ttu-id="b0824-111">ICE36 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="b0824-111">ICE36 reports the following error for the example shown.</span></span>

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

<span data-ttu-id="b0824-112">[圖示表格](icon-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b0824-112">[Icon Table](icon-table.md) (partial)</span></span>



| <span data-ttu-id="b0824-113">Name</span><span class="sxs-lookup"><span data-stu-id="b0824-113">Name</span></span>  | <span data-ttu-id="b0824-114">資料</span><span class="sxs-lookup"><span data-stu-id="b0824-114">Data</span></span>     |
|-------|----------|
| <span data-ttu-id="b0824-115">Icon1</span><span class="sxs-lookup"><span data-stu-id="b0824-115">Icon1</span></span> | <span data-ttu-id="b0824-116">Control1</span><span class="sxs-lookup"><span data-stu-id="b0824-116">Control1</span></span> |
| <span data-ttu-id="b0824-117">Icon2</span><span class="sxs-lookup"><span data-stu-id="b0824-117">Icon2</span></span> | <span data-ttu-id="b0824-118">Control2</span><span class="sxs-lookup"><span data-stu-id="b0824-118">Control2</span></span> |
| <span data-ttu-id="b0824-119">Icon3</span><span class="sxs-lookup"><span data-stu-id="b0824-119">Icon3</span></span> | <span data-ttu-id="b0824-120">Control3</span><span class="sxs-lookup"><span data-stu-id="b0824-120">Control3</span></span> |
| <span data-ttu-id="b0824-121">Icon4</span><span class="sxs-lookup"><span data-stu-id="b0824-121">Icon4</span></span> | <span data-ttu-id="b0824-122">Control4</span><span class="sxs-lookup"><span data-stu-id="b0824-122">Control4</span></span> |



 

<span data-ttu-id="b0824-123">[ProgID 資料表](progid-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b0824-123">[ProgID Table](progid-table.md) (partial)</span></span>



| <span data-ttu-id="b0824-124">ProgID</span><span class="sxs-lookup"><span data-stu-id="b0824-124">ProgID</span></span>    |
|-----------|
| <span data-ttu-id="b0824-125">Property1</span><span class="sxs-lookup"><span data-stu-id="b0824-125">Property1</span></span> |



 

<span data-ttu-id="b0824-126">[類別表](class-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b0824-126">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="b0824-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="b0824-127">CLSID</span></span>                                  |
|----------------------------------------|
| <span data-ttu-id="b0824-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="b0824-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span></span> |



 

<span data-ttu-id="b0824-129"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="b0824-129">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="b0824-130">快速鍵</span><span class="sxs-lookup"><span data-stu-id="b0824-130">Shortcut</span></span>  | <span data-ttu-id="b0824-131">圖示\_</span><span class="sxs-lookup"><span data-stu-id="b0824-131">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="b0824-132">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="b0824-132">Shortcut1</span></span> | <span data-ttu-id="b0824-133">Icon2</span><span class="sxs-lookup"><span data-stu-id="b0824-133">Icon2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="b0824-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0824-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0824-135">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="b0824-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



