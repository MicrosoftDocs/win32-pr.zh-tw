---
description: 此表格包含圖示檔。 資料表中的每個圖示都會複製到檔案做為產品公告的一部分，以用於公告的快捷方式和 OLE 伺服器。 請參閱 OLE 對資料流程的限制。
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: 圖示表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192445"
---
# <a name="icon-table"></a><span data-ttu-id="30240-105">圖示表</span><span class="sxs-lookup"><span data-stu-id="30240-105">Icon Table</span></span>

<span data-ttu-id="30240-106">此表格包含圖示檔。</span><span class="sxs-lookup"><span data-stu-id="30240-106">This table contains the icon files.</span></span> <span data-ttu-id="30240-107">資料表中的每個圖示都會複製到檔案做為產品公告的一部分，以用於公告的快捷方式和 OLE 伺服器。</span><span class="sxs-lookup"><span data-stu-id="30240-107">Each icon from the table is copied to a file as a part of product advertisement to be used for advertised shortcuts and OLE servers.</span></span> <span data-ttu-id="30240-108">請參閱 [OLE 對資料流程的限制](ole-limitations-on-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="30240-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="30240-109">圖示表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="30240-109">The Icon table has the following columns.</span></span>



| <span data-ttu-id="30240-110">Column</span><span class="sxs-lookup"><span data-stu-id="30240-110">Column</span></span> | <span data-ttu-id="30240-111">類型</span><span class="sxs-lookup"><span data-stu-id="30240-111">Type</span></span>                         | <span data-ttu-id="30240-112">答案</span><span class="sxs-lookup"><span data-stu-id="30240-112">Key</span></span> | <span data-ttu-id="30240-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="30240-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="30240-114">Name</span><span class="sxs-lookup"><span data-stu-id="30240-114">Name</span></span>   | [<span data-ttu-id="30240-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="30240-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="30240-116">Y</span><span class="sxs-lookup"><span data-stu-id="30240-116">Y</span></span>   | <span data-ttu-id="30240-117">N</span><span class="sxs-lookup"><span data-stu-id="30240-117">N</span></span>        |
| <span data-ttu-id="30240-118">資料</span><span class="sxs-lookup"><span data-stu-id="30240-118">Data</span></span>   | [<span data-ttu-id="30240-119">二進位</span><span class="sxs-lookup"><span data-stu-id="30240-119">Binary</span></span>](binary.md)         | <span data-ttu-id="30240-120">N</span><span class="sxs-lookup"><span data-stu-id="30240-120">N</span></span>   | <span data-ttu-id="30240-121">N</span><span class="sxs-lookup"><span data-stu-id="30240-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="30240-122">資料行</span><span class="sxs-lookup"><span data-stu-id="30240-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="30240-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="30240-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="30240-124">圖示檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="30240-124">Name of the icon file.</span></span>

</dd> <dt>

<span data-ttu-id="30240-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>資料</span><span class="sxs-lookup"><span data-stu-id="30240-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="30240-126">PE 中的二進位圖示資料 ( .dll 或 .exe) 或圖示 ( .ico) 格式。</span><span class="sxs-lookup"><span data-stu-id="30240-126">The binary icon data in PE (.dll or .exe) or icon (.ico) format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30240-127">備註</span><span class="sxs-lookup"><span data-stu-id="30240-127">Remarks</span></span>

<span data-ttu-id="30240-128">當 [PublishProduct 動作](publishproduct-action.md) 執行時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="30240-128">This table is referred to when the [PublishProduct action](publishproduct-action.md) is executed.</span></span>

<span data-ttu-id="30240-129">快速鍵、副檔名和 Clsid 的圖示必須儲存在與目標檔案本身不同的檔案中。</span><span class="sxs-lookup"><span data-stu-id="30240-129">The icons for shortcuts, file name extensions, and CLSIDs must be stored in files that are separate from the target file itself.</span></span> <span data-ttu-id="30240-130">這是必要的，因為安裝程式應該只在廣告資源時將小型圖示檔複製到使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="30240-130">This is required because the installer should copy only the small icon files to the user's machine when advertising the resource.</span></span> <span data-ttu-id="30240-131">因此，安裝套件的開發人員必須撰寫只包含圖示的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="30240-131">A developer of an installation package therefore needs to author separate files containing only the icons.</span></span> <span data-ttu-id="30240-132">這些圖示檔接著會以二進位資料的形式儲存在圖示資料表中。</span><span class="sxs-lookup"><span data-stu-id="30240-132">These icon files are then stored as binary data in the Icon table.</span></span>

<span data-ttu-id="30240-133">嚴格與副檔名或 Clsid 相關聯的圖示檔可以有任何副檔名，例如 .ico。</span><span class="sxs-lookup"><span data-stu-id="30240-133">Icon files that are associated strictly with file name extensions or CLSIDs can have any extension, such as .ico.</span></span> <span data-ttu-id="30240-134">不過，與快捷方式相關聯的圖示檔必須是 EXE 二進位格式，而且必須命名，使其擴充功能符合目標的副檔名。</span><span class="sxs-lookup"><span data-stu-id="30240-134">However, Icon files that are associated with shortcuts must be in the EXE binary format and must be named such that their extension matches the extension of the target.</span></span> <span data-ttu-id="30240-135">如果未遵循此規則，快捷方式將無法運作。</span><span class="sxs-lookup"><span data-stu-id="30240-135">The shortcut will not work if this rule is not followed.</span></span> <span data-ttu-id="30240-136">例如，如果快捷方式是指向具有金鑰檔 Red.bar 的資源，則圖示檔也必須有副檔名 bar。</span><span class="sxs-lookup"><span data-stu-id="30240-136">For example, if a shortcut is to point to a resource having the key file Red.bar, then the icon file must also have the extension .bar.</span></span> <span data-ttu-id="30240-137">只要所有目標檔案都具有相同的副檔名，就可以將多個圖示芝到相同的圖示檔。</span><span class="sxs-lookup"><span data-stu-id="30240-137">Multiple icons can be stuffed into the same icon file as long as all of the target files have the same extension.</span></span>

## <a name="validation"></a><span data-ttu-id="30240-138">驗證</span><span class="sxs-lookup"><span data-stu-id="30240-138">Validation</span></span>

<dl>

[<span data-ttu-id="30240-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="30240-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="30240-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="30240-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="30240-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="30240-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="30240-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="30240-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="30240-143">ICE36</span><span class="sxs-lookup"><span data-stu-id="30240-143">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="30240-144">ICE50</span><span class="sxs-lookup"><span data-stu-id="30240-144">ICE50</span></span>](ice50.md)  
</dl>

 

 



