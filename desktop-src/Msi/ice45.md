---
description: ICE45 會驗證資料庫中的位欄位資料行是否未將任何保留的位設定為1。
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192447"
---
# <a name="ice45"></a><span data-ttu-id="e58d2-103">ICE45</span><span class="sxs-lookup"><span data-stu-id="e58d2-103">ICE45</span></span>

<span data-ttu-id="e58d2-104">ICE45 會驗證資料庫中的位欄位資料行是否未將任何保留的位設定為1。</span><span class="sxs-lookup"><span data-stu-id="e58d2-104">ICE45 validates that bit field columns in the database do not set any reserved bits to 1.</span></span>

<span data-ttu-id="e58d2-105">保留的位在目前的安裝程式版本中不提供任何功能，但在未來的版本中可能會提供。</span><span class="sxs-lookup"><span data-stu-id="e58d2-105">Reserved bits provide no functionality in current versions of the installer, but might in future versions.</span></span> <span data-ttu-id="e58d2-106">它們應該設定為0，以與 Windows Installer 的未來版本相容。</span><span class="sxs-lookup"><span data-stu-id="e58d2-106">They should be set to 0 to be compatible with future versions of Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="e58d2-107">結果</span><span class="sxs-lookup"><span data-stu-id="e58d2-107">Result</span></span>

<span data-ttu-id="e58d2-108">如果下列任何一份資料表包含位欄位，並將保留的位設定為1，ICE45 就會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e58d2-108">ICE45 posts an error message if any of the following tables contains a bit field with a reserved bit set to a value of 1.</span></span>

-   [<span data-ttu-id="e58d2-109">BBControl 資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-109">BBControl table</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="e58d2-110">對話方塊資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-110">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="e58d2-111">功能資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-111">Feature table</span></span>](feature-table.md)
-   [<span data-ttu-id="e58d2-112">檔資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-112">File table</span></span>](file-table.md)
-   [<span data-ttu-id="e58d2-113">MoveFile 資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-113">MoveFile table</span></span>](movefile-table.md)
-   [<span data-ttu-id="e58d2-114">ModuleConfiguration 資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-114">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)
-   [<span data-ttu-id="e58d2-115">ODBCDataSource 資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-115">ODBCDataSource table</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="e58d2-116">修補資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-116">Patch table</span></span>](patch-table.md)
-   [<span data-ttu-id="e58d2-117">RemoveFile 資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-117">RemoveFile table</span></span>](removefile-table.md)
-   [<span data-ttu-id="e58d2-118">ServiceControl 資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-118">ServiceControl table</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="e58d2-119">ServiceInstall 資料表</span><span class="sxs-lookup"><span data-stu-id="e58d2-119">ServiceInstall table</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="e58d2-120">樣式表單</span><span class="sxs-lookup"><span data-stu-id="e58d2-120">TextStyle table</span></span>](textstyle-table.md)

<span data-ttu-id="e58d2-121">如果 [控制資料表](control-table.md) 包含位欄位，並將保留的位設定為1，則 ICE45 會張貼兩個警告訊息的其中一個。</span><span class="sxs-lookup"><span data-stu-id="e58d2-121">ICE45 posts one of two warning messages if the [Control Table](control-table.md) contains a bit field with a reserved bit set to a value of 1.</span></span>

## <a name="example"></a><span data-ttu-id="e58d2-122">範例</span><span class="sxs-lookup"><span data-stu-id="e58d2-122">Example</span></span>

<span data-ttu-id="e58d2-123">ICE45 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="e58d2-123">ICE45 reports the following error for the example shown.</span></span>

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

<span data-ttu-id="e58d2-124">ICE45 會針對所顯示的範例報告下列警告。</span><span class="sxs-lookup"><span data-stu-id="e58d2-124">ICE45 reports the following warning for the example shown.</span></span>

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

<span data-ttu-id="e58d2-125">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="e58d2-125">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="e58d2-126">檔案</span><span class="sxs-lookup"><span data-stu-id="e58d2-126">File</span></span>  | <span data-ttu-id="e58d2-127">屬性</span><span class="sxs-lookup"><span data-stu-id="e58d2-127">Attributes</span></span> |
|-------|------------|
| <span data-ttu-id="e58d2-128">File1</span><span class="sxs-lookup"><span data-stu-id="e58d2-128">File1</span></span> | <span data-ttu-id="e58d2-129">128</span><span class="sxs-lookup"><span data-stu-id="e58d2-129">128</span></span>        |



 

<span data-ttu-id="e58d2-130">[控制資料表](control-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="e58d2-130">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="e58d2-131">對話</span><span class="sxs-lookup"><span data-stu-id="e58d2-131">Dialog</span></span>  | <span data-ttu-id="e58d2-132">控制</span><span class="sxs-lookup"><span data-stu-id="e58d2-132">Control</span></span> | <span data-ttu-id="e58d2-133">屬性</span><span class="sxs-lookup"><span data-stu-id="e58d2-133">Attributes</span></span> |
|---------|---------|------------|
| <span data-ttu-id="e58d2-134">Dialog1</span><span class="sxs-lookup"><span data-stu-id="e58d2-134">Dialog1</span></span> | <span data-ttu-id="e58d2-135">Edit1</span><span class="sxs-lookup"><span data-stu-id="e58d2-135">Edit1</span></span>   | <span data-ttu-id="e58d2-136">2097152</span><span class="sxs-lookup"><span data-stu-id="e58d2-136">2097152</span></span>    |
| <span data-ttu-id="e58d2-137">Dialog1</span><span class="sxs-lookup"><span data-stu-id="e58d2-137">Dialog1</span></span> | <span data-ttu-id="e58d2-138">Edit2</span><span class="sxs-lookup"><span data-stu-id="e58d2-138">Edit2</span></span>   | <span data-ttu-id="e58d2-139">1048576</span><span class="sxs-lookup"><span data-stu-id="e58d2-139">1048576</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="e58d2-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="e58d2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e58d2-141">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="e58d2-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



