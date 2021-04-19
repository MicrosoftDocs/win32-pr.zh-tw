---
description: ICE42 會驗證 InProc 伺服器是否未連結至類別表中的 EXE 檔案。 它也會驗證只有 LocalServer 和 LocalServer32 類別具有引數和 DefInProc 值。
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983713"
---
# <a name="ice42"></a><span data-ttu-id="0c8ba-104">ICE42</span><span class="sxs-lookup"><span data-stu-id="0c8ba-104">ICE42</span></span>

<span data-ttu-id="0c8ba-105">ICE42 會驗證 InProc 伺服器是否未連結至 [類別表](class-table.md)中的 EXE 檔案。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-105">ICE42 validates that InProc servers are not linked to EXE files in the [Class table](class-table.md).</span></span> <span data-ttu-id="0c8ba-106">它也會驗證只有 LocalServer 和 LocalServer32 類別具有引數和 DefInProc 值。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-106">It also validates that only LocalServer and LocalServer32 classes have arguments and DefInProc values.</span></span>

## <a name="result"></a><span data-ttu-id="0c8ba-107">結果</span><span class="sxs-lookup"><span data-stu-id="0c8ba-107">Result</span></span>

<span data-ttu-id="0c8ba-108">如果有 InProc 伺服器連結至類別資料表中的 EXE 檔案，ICE42 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-108">ICE42 posts an error if there are InProc servers linked to EXE files in the Class table.</span></span>

## <a name="example"></a><span data-ttu-id="0c8ba-109">範例</span><span class="sxs-lookup"><span data-stu-id="0c8ba-109">Example</span></span>

<span data-ttu-id="0c8ba-110">ICE42 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-110">ICE42 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="0c8ba-111">ICE42 錯誤</span><span class="sxs-lookup"><span data-stu-id="0c8ba-111">ICE42 error</span></span>                                                                                                                             | <span data-ttu-id="0c8ba-112">Description</span><span class="sxs-lookup"><span data-stu-id="0c8ba-112">Description</span></span>                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8ba-113">CLSID ' {GUID1} ' 是 InProc 伺服器，但正在執行的元件 ' Component1 ' 有 EXE ( ' test.exe ' ) 作為 KeyFile。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-113">CLSID '{GUID1}' is an InProc server, but the implementing component 'Component1' has an EXE ('test.exe') as its KeyFile.</span></span>                | <span data-ttu-id="0c8ba-114">有一個可執行檔指定為 InProc 伺服器。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-114">There is an executable file specified as an InProc server.</span></span> <span data-ttu-id="0c8ba-115">EXE 檔案不能是 InProc 伺服器。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-115">EXE files cannot be InProc servers.</span></span>                                                                                                                            |
| <span data-ttu-id="0c8ba-116">內容 ' InProcServer32 ' 中的 CLSID ' {GUID1} ' 有引數。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-116">CLSID '{GUID1}' in context 'InProcServer32' has an argument.</span></span> <span data-ttu-id="0c8ba-117">只有 LocalServer 內容可以有引數。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-117">Only LocalServer contexts can have arguments.</span></span>                              | <span data-ttu-id="0c8ba-118">若要修正這個錯誤，請移除引數。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-118">To fix this error, remove the argument.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="0c8ba-119">內容 ' InProcServer32 ' 中的 CLSID ' {GUID1} ' 指定了預設 InProc 值。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-119">CLSID '{GUID1}' in context 'InProcServer32' specifies a default InProc value.</span></span> <span data-ttu-id="0c8ba-120">只有 LocalServer 內容可以有預設 InProc 值。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-120">Only LocalServer contexts can have default InProc values.</span></span> | <span data-ttu-id="0c8ba-121">具有預設 InProc 值的物件不是在 LocalServer 或 LocalServer32 內容中運作的物件。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-121">There is an object with a default InProc value that is not an object operating in the LocalServer or LocalServer32 contexts.</span></span> <span data-ttu-id="0c8ba-122">若要修正這個錯誤，請移除 DeflnProc 值或變更類別的內容。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-122">To fix this error, remove the DeflnProc value or change the context of the class.</span></span><br/> |



 

<span data-ttu-id="0c8ba-123">[類別表](class-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="0c8ba-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="0c8ba-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="0c8ba-124">CLSID</span></span>   | <span data-ttu-id="0c8ba-125">Context</span><span class="sxs-lookup"><span data-stu-id="0c8ba-125">Context</span></span>        | <span data-ttu-id="0c8ba-126">元件\_</span><span class="sxs-lookup"><span data-stu-id="0c8ba-126">Component\_</span></span> | <span data-ttu-id="0c8ba-127">DefInProcHandler</span><span class="sxs-lookup"><span data-stu-id="0c8ba-127">DefInProcHandler</span></span> | <span data-ttu-id="0c8ba-128">引數</span><span class="sxs-lookup"><span data-stu-id="0c8ba-128">Argument</span></span> |
|---------|----------------|-------------|------------------|----------|
| <span data-ttu-id="0c8ba-129">GUID1</span><span class="sxs-lookup"><span data-stu-id="0c8ba-129">{GUID1}</span></span> | <span data-ttu-id="0c8ba-130">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="0c8ba-130">InProcServer32</span></span> | <span data-ttu-id="0c8ba-131">Component1</span><span class="sxs-lookup"><span data-stu-id="0c8ba-131">Component1</span></span>  | <span data-ttu-id="0c8ba-132">InProcServer</span><span class="sxs-lookup"><span data-stu-id="0c8ba-132">InProcServer</span></span>     | <span data-ttu-id="0c8ba-133">精 氨 酸</span><span class="sxs-lookup"><span data-stu-id="0c8ba-133">Arg</span></span>      |



 

<span data-ttu-id="0c8ba-134">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="0c8ba-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="0c8ba-135">元件</span><span class="sxs-lookup"><span data-stu-id="0c8ba-135">Component</span></span>  | <span data-ttu-id="0c8ba-136">KeyPath</span><span class="sxs-lookup"><span data-stu-id="0c8ba-136">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="0c8ba-137">Component1</span><span class="sxs-lookup"><span data-stu-id="0c8ba-137">Component1</span></span> | <span data-ttu-id="0c8ba-138">File1</span><span class="sxs-lookup"><span data-stu-id="0c8ba-138">File1</span></span>   |



 

<span data-ttu-id="0c8ba-139">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="0c8ba-139">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="0c8ba-140">檔案</span><span class="sxs-lookup"><span data-stu-id="0c8ba-140">File</span></span>  | <span data-ttu-id="0c8ba-141">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="0c8ba-141">Filename</span></span> |
|-------|----------|
| <span data-ttu-id="0c8ba-142">File1</span><span class="sxs-lookup"><span data-stu-id="0c8ba-142">File1</span></span> | <span data-ttu-id="0c8ba-143">test.exe</span><span class="sxs-lookup"><span data-stu-id="0c8ba-143">test.exe</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0c8ba-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c8ba-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c8ba-145">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="0c8ba-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




