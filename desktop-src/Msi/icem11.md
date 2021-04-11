---
description: ICEM11 會確認可設定的合併模組會列出模組 ModuleIgnoreTable 資料表中的 ModuleConfiguration 資料表和 ModuleSubstitution 資料表。
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193684"
---
# <a name="icem11"></a><span data-ttu-id="d9deb-103">ICEM11</span><span class="sxs-lookup"><span data-stu-id="d9deb-103">ICEM11</span></span>

<span data-ttu-id="d9deb-104">ICEM11 會確認可設定的合併模組會列出模組[ModuleIgnoreTable 資料表](moduleignoretable-table.md)中的[ModuleConfiguration 資料表](moduleconfiguration-table.md)和[ModuleSubstitution 資料表](modulesubstitution-table.md)。</span><span class="sxs-lookup"><span data-stu-id="d9deb-104">ICEM11 verifies that a Configurable Merge Module lists the [ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md) in the [ModuleIgnoreTable table](moduleignoretable-table.md) of the module.</span></span> <span data-ttu-id="d9deb-105">這可確保無法辨識可設定合併模組 (小於2.0 版的合併工具，) 不會將這些資料表複製到目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="d9deb-105">This ensures that merge tools that do not recognize configurable merge modules(less than version 2.0) do not copy these tables into the target database.</span></span>

<span data-ttu-id="d9deb-106">此 ICEM 可在 Windows Installer 2.0 SDK 和更新版本提供的 Mergemod 檔中找到。</span><span class="sxs-lookup"><span data-stu-id="d9deb-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="d9deb-107">如需詳細資訊，請參閱 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="d9deb-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="d9deb-108">結果</span><span class="sxs-lookup"><span data-stu-id="d9deb-108">Result</span></span>

<span data-ttu-id="d9deb-109">如果模組包含未列于 ModuleIgnoreTable 資料表中的 ModuleConfiguration 或 ModuleSubstitution 資料表，ICEM11 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="d9deb-109">ICEM11 posts an error if the module contains a ModuleConfiguration or ModuleSubstitution table not listed in the ModuleIgnoreTable table.</span></span>

## <a name="example"></a><span data-ttu-id="d9deb-110">範例</span><span class="sxs-lookup"><span data-stu-id="d9deb-110">Example</span></span>

<span data-ttu-id="d9deb-111">ICEM11 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="d9deb-111">ICEM11 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

<span data-ttu-id="d9deb-112">[ModuleConfiguration](moduleconfiguration-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="d9deb-112">[ModuleConfiguration](moduleconfiguration-table.md) (partial)</span></span>



| <span data-ttu-id="d9deb-113">Name</span><span class="sxs-lookup"><span data-stu-id="d9deb-113">Name</span></span>     | <span data-ttu-id="d9deb-114">格式</span><span class="sxs-lookup"><span data-stu-id="d9deb-114">Format</span></span> | <span data-ttu-id="d9deb-115">類型</span><span class="sxs-lookup"><span data-stu-id="d9deb-115">Type</span></span>   | <span data-ttu-id="d9deb-116">CoNtextData</span><span class="sxs-lookup"><span data-stu-id="d9deb-116">ContextData</span></span> | <span data-ttu-id="d9deb-117">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d9deb-117">DefaultValue</span></span> |
|----------|--------|--------|-------------|--------------|
| <span data-ttu-id="d9deb-118">IconKey1</span><span class="sxs-lookup"><span data-stu-id="d9deb-118">IconKey1</span></span> | <span data-ttu-id="d9deb-119">1</span><span class="sxs-lookup"><span data-stu-id="d9deb-119">1</span></span>      | <span data-ttu-id="d9deb-120">Binary</span><span class="sxs-lookup"><span data-stu-id="d9deb-120">Binary</span></span> | <span data-ttu-id="d9deb-121">圖示</span><span class="sxs-lookup"><span data-stu-id="d9deb-121">Icon</span></span>        | <span data-ttu-id="d9deb-122">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="d9deb-122">DefaultIcon</span></span>  |



 

[<span data-ttu-id="d9deb-123">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="d9deb-123">ModuleSubstitution</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="d9deb-124">資料表</span><span class="sxs-lookup"><span data-stu-id="d9deb-124">Table</span></span>   | <span data-ttu-id="d9deb-125">資料列</span><span class="sxs-lookup"><span data-stu-id="d9deb-125">Row</span></span>              | <span data-ttu-id="d9deb-126">資料行</span><span class="sxs-lookup"><span data-stu-id="d9deb-126">Column</span></span> | <span data-ttu-id="d9deb-127">值</span><span class="sxs-lookup"><span data-stu-id="d9deb-127">Value</span></span>        |
|---------|------------------|--------|--------------|
| <span data-ttu-id="d9deb-128">控制</span><span class="sxs-lookup"><span data-stu-id="d9deb-128">Control</span></span> | <span data-ttu-id="d9deb-129">Dialog1;Control1</span><span class="sxs-lookup"><span data-stu-id="d9deb-129">Dialog1;Control1</span></span> | <span data-ttu-id="d9deb-130">Text</span><span class="sxs-lookup"><span data-stu-id="d9deb-130">Text</span></span>   | <span data-ttu-id="d9deb-131">\[IconKey1\]</span><span class="sxs-lookup"><span data-stu-id="d9deb-131">\[IconKey1\]</span></span> |



 

[<span data-ttu-id="d9deb-132">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="d9deb-132">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)



| <span data-ttu-id="d9deb-133">資料表</span><span class="sxs-lookup"><span data-stu-id="d9deb-133">Table</span></span>               |
|---------------------|
| <span data-ttu-id="d9deb-134">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9deb-134">ModuleConfiguration</span></span> |



 

<span data-ttu-id="d9deb-135">若要修正這個錯誤，請在 ModuleIgnoreTable 資料表中同時包含 ModuleSubstitution 和 ModuleConfiguration 資料表。</span><span class="sxs-lookup"><span data-stu-id="d9deb-135">To fix this error include both the ModuleSubstitution and ModuleConfiguration tables in the ModuleIgnoreTable table.</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="d9deb-136">執行期間所使用的資料表</span><span class="sxs-lookup"><span data-stu-id="d9deb-136">Table Used During Execution</span></span>

[<span data-ttu-id="d9deb-137">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="d9deb-137">ModuleSubstitution</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="d9deb-138">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9deb-138">ModuleConfiguration</span></span>](moduleconfiguration-table.md)

[<span data-ttu-id="d9deb-139">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="d9deb-139">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)

## <a name="related-topics"></a><span data-ttu-id="d9deb-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9deb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9deb-141">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="d9deb-141">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



