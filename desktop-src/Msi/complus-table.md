---
description: Complus 資料表包含安裝 COM + 應用程式所需的資訊。
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Complus 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978386"
---
# <a name="complus-table"></a><span data-ttu-id="2562e-103">Complus 資料表</span><span class="sxs-lookup"><span data-stu-id="2562e-103">Complus Table</span></span>

<span data-ttu-id="2562e-104">Complus 資料表包含安裝 COM + 應用程式所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="2562e-104">The Complus table contains information needed to install COM+ applications.</span></span>

<span data-ttu-id="2562e-105">Complus 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="2562e-105">The Complus table has the following columns.</span></span>



| <span data-ttu-id="2562e-106">Column</span><span class="sxs-lookup"><span data-stu-id="2562e-106">Column</span></span>      | <span data-ttu-id="2562e-107">類型</span><span class="sxs-lookup"><span data-stu-id="2562e-107">Type</span></span>                         | <span data-ttu-id="2562e-108">答案</span><span class="sxs-lookup"><span data-stu-id="2562e-108">Key</span></span> | <span data-ttu-id="2562e-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2562e-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="2562e-110">元件\_</span><span class="sxs-lookup"><span data-stu-id="2562e-110">Component\_</span></span> | [<span data-ttu-id="2562e-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="2562e-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2562e-112">Y</span><span class="sxs-lookup"><span data-stu-id="2562e-112">Y</span></span>   | <span data-ttu-id="2562e-113">N</span><span class="sxs-lookup"><span data-stu-id="2562e-113">N</span></span>        |
| <span data-ttu-id="2562e-114">ExpType</span><span class="sxs-lookup"><span data-stu-id="2562e-114">ExpType</span></span>     | [<span data-ttu-id="2562e-115">整數</span><span class="sxs-lookup"><span data-stu-id="2562e-115">Integer</span></span>](integer.md)       | <span data-ttu-id="2562e-116">N</span><span class="sxs-lookup"><span data-stu-id="2562e-116">N</span></span>   | <span data-ttu-id="2562e-117">Y</span><span class="sxs-lookup"><span data-stu-id="2562e-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2562e-118">資料行</span><span class="sxs-lookup"><span data-stu-id="2562e-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2562e-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="2562e-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="2562e-120">[元件資料表](component-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2562e-120">An external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="2562e-121">這是包含 COM + 應用程式的元件。</span><span class="sxs-lookup"><span data-stu-id="2562e-121">This is the component that contains the COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="2562e-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span><span class="sxs-lookup"><span data-stu-id="2562e-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span></span>
</dt> <dd>

<span data-ttu-id="2562e-123">匯出在產生 .msi 檔案期間使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="2562e-123">Export flags used during the generation of the .msi file.</span></span> <span data-ttu-id="2562e-124">如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的 COM + 檔。</span><span class="sxs-lookup"><span data-stu-id="2562e-124">For more information see the COM+ documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2562e-125">備註</span><span class="sxs-lookup"><span data-stu-id="2562e-125">Remarks</span></span>

<span data-ttu-id="2562e-126">請參閱 [RegisterComPlus 動作](registercomplus-action.md) 和 [UnregisterComPlus 動作](unregistercomplus-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2562e-126">See the [RegisterComPlus action](registercomplus-action.md) and [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

<span data-ttu-id="2562e-127">請參閱 [安裝具有 Windows Installer 的 COM + 應用程式](installing-a-com--application-with-the-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="2562e-127">See [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span></span>

## <a name="validation"></a><span data-ttu-id="2562e-128">驗證</span><span class="sxs-lookup"><span data-stu-id="2562e-128">Validation</span></span>

<dl>

[<span data-ttu-id="2562e-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="2562e-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2562e-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="2562e-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2562e-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="2562e-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2562e-132">ICE66</span><span class="sxs-lookup"><span data-stu-id="2562e-132">ICE66</span></span>](ice66.md)  
</dl>

 

 



