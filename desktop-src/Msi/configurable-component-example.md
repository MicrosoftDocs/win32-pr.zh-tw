---
description: 此範例可讓模組取用者個別設定編輯控制項、總和檢查碼屬性，以及壓縮屬性。
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: 可設定的元件範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983333"
---
# <a name="configurable-component-example"></a><span data-ttu-id="513b3-103">可設定的元件範例</span><span class="sxs-lookup"><span data-stu-id="513b3-103">Configurable Component Example</span></span>

<span data-ttu-id="513b3-104">在此範例中，下列 ModuleConfiguration 和 ModuleSubstitution 資料表可讓模組取用者個別設定編輯控制項的 Password 屬性、檔案的總和檢查碼屬性，以及相同檔案的壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="513b3-104">In this example, the following ModuleConfiguration and ModuleSubstitution tables allows the module consumer to independently configure the Password attribute for an edit control, the checksum attribute for a file, and the compressed attribute for the same file.</span></span>

[<span data-ttu-id="513b3-105">ModuleSubstitution 資料表</span><span class="sxs-lookup"><span data-stu-id="513b3-105">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="513b3-106">資料表</span><span class="sxs-lookup"><span data-stu-id="513b3-106">Table</span></span>   | <span data-ttu-id="513b3-107">資料列</span><span class="sxs-lookup"><span data-stu-id="513b3-107">Row</span></span>           | <span data-ttu-id="513b3-108">資料行</span><span class="sxs-lookup"><span data-stu-id="513b3-108">Column</span></span>     | <span data-ttu-id="513b3-109">值</span><span class="sxs-lookup"><span data-stu-id="513b3-109">Value</span></span>                        |
|---------|---------------|------------|------------------------------|
| <span data-ttu-id="513b3-110">控制</span><span class="sxs-lookup"><span data-stu-id="513b3-110">Control</span></span> | <span data-ttu-id="513b3-111">Dialog1;Edit1</span><span class="sxs-lookup"><span data-stu-id="513b3-111">Dialog1;Edit1</span></span> | <span data-ttu-id="513b3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="513b3-112">Attributes</span></span> | <span data-ttu-id="513b3-113">\[= 密碼\]</span><span class="sxs-lookup"><span data-stu-id="513b3-113">\[=Password\]</span></span>                |
| <span data-ttu-id="513b3-114">檔案</span><span class="sxs-lookup"><span data-stu-id="513b3-114">File</span></span>    | <span data-ttu-id="513b3-115">File1</span><span class="sxs-lookup"><span data-stu-id="513b3-115">File1</span></span>         | <span data-ttu-id="513b3-116">屬性</span><span class="sxs-lookup"><span data-stu-id="513b3-116">Attributes</span></span> | <span data-ttu-id="513b3-117">\[= Checksum \] \[ = 已壓縮\]</span><span class="sxs-lookup"><span data-stu-id="513b3-117">\[=Checksum\]\[=Compressed\]</span></span> |



 

[<span data-ttu-id="513b3-118">ModuleConfiguration 資料表</span><span class="sxs-lookup"><span data-stu-id="513b3-118">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md)



| <span data-ttu-id="513b3-119">Name</span><span class="sxs-lookup"><span data-stu-id="513b3-119">Name</span></span>       | <span data-ttu-id="513b3-120">格式</span><span class="sxs-lookup"><span data-stu-id="513b3-120">Format</span></span>   | <span data-ttu-id="513b3-121">類型</span><span class="sxs-lookup"><span data-stu-id="513b3-121">Type</span></span> | <span data-ttu-id="513b3-122">CoNtextData</span><span class="sxs-lookup"><span data-stu-id="513b3-122">ContextData</span></span>                              | <span data-ttu-id="513b3-123">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="513b3-123">DefaultValue</span></span> | <span data-ttu-id="513b3-124">屬性</span><span class="sxs-lookup"><span data-stu-id="513b3-124">Attributes</span></span> | <span data-ttu-id="513b3-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="513b3-125">DisplayName</span></span> | <span data-ttu-id="513b3-126">Description</span><span class="sxs-lookup"><span data-stu-id="513b3-126">Description</span></span> |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| <span data-ttu-id="513b3-127">密碼</span><span class="sxs-lookup"><span data-stu-id="513b3-127">Password</span></span>   | <span data-ttu-id="513b3-128">字元</span><span class="sxs-lookup"><span data-stu-id="513b3-128">Bitfield</span></span> |      | <span data-ttu-id="513b3-129">2097152;True = 2097152;False = 0</span><span class="sxs-lookup"><span data-stu-id="513b3-129">2097152;True=2097152;False=0</span></span>             | <span data-ttu-id="513b3-130">0</span><span class="sxs-lookup"><span data-stu-id="513b3-130">0</span></span>            | <span data-ttu-id="513b3-131">0</span><span class="sxs-lookup"><span data-stu-id="513b3-131">0</span></span>          |             |             |
| <span data-ttu-id="513b3-132">總和檢查碼</span><span class="sxs-lookup"><span data-stu-id="513b3-132">Checksum</span></span>   | <span data-ttu-id="513b3-133">字元</span><span class="sxs-lookup"><span data-stu-id="513b3-133">Bitfield</span></span> |      | <span data-ttu-id="513b3-134">1024;Checksum = 1024;無總和檢查碼 = 0</span><span class="sxs-lookup"><span data-stu-id="513b3-134">1024;Checksum=1024;No Checksum=0</span></span>         | <span data-ttu-id="513b3-135">0</span><span class="sxs-lookup"><span data-stu-id="513b3-135">0</span></span>            | <span data-ttu-id="513b3-136">0</span><span class="sxs-lookup"><span data-stu-id="513b3-136">0</span></span>          |             |             |
| <span data-ttu-id="513b3-137">Compressed</span><span class="sxs-lookup"><span data-stu-id="513b3-137">Compressed</span></span> | <span data-ttu-id="513b3-138">字元</span><span class="sxs-lookup"><span data-stu-id="513b3-138">Bitfield</span></span> |      | <span data-ttu-id="513b3-139">24576;壓縮 = 16384;未壓縮 = 8192</span><span class="sxs-lookup"><span data-stu-id="513b3-139">24576;Compressed=16384;Uncompressed=8192</span></span> | <span data-ttu-id="513b3-140">8192</span><span class="sxs-lookup"><span data-stu-id="513b3-140">8192</span></span>         | <span data-ttu-id="513b3-141">0</span><span class="sxs-lookup"><span data-stu-id="513b3-141">0</span></span>          |             |             |



 

 

 



