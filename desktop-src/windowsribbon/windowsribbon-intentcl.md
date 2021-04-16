---
title: 編譯功能區標記
description: 若要讓 Windows 功能區架構使用功能區標記檔案，必須將標記檔案編譯成二進位格式的資源檔。
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows 功能區，編譯標記
- 功能區，編譯標記
- Windows 功能區，編譯器工作流程
- 功能區、編譯器工作流程
- 'Windows 功能區、UI 命令編譯器 (UICC.exe) '
- '功能區、UI 命令編譯器 (UICC.exe) '
- 'UI 命令編譯器 (UICC.exe) '
- 'UICC.exe (UI 命令編譯器) '
- 編譯 Windows 功能區標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507356"
---
# <a name="compiling-ribbon-markup"></a><span data-ttu-id="b28a6-112">編譯功能區標記</span><span class="sxs-lookup"><span data-stu-id="b28a6-112">Compiling Ribbon Markup</span></span>

<span data-ttu-id="b28a6-113">若要讓 Windows 功能區架構使用 [功能區標記](windowsribbon-schema.md) 檔案，必須將標記檔案編譯成二進位格式的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b28a6-113">For the Windows Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="b28a6-114">Windows 軟體開發套件 (SDK)  (7.0 （含）以後版本的 (UICC) 的專用標記編譯器會隨附于此用途。</span><span class="sxs-lookup"><span data-stu-id="b28a6-114">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="b28a6-115">除了編譯標記的二進位版本之外，UICC 會產生 ID 定義標頭 ( .h) 檔案，該檔案會將所有標記專案公開至功能區主應用程式，以及在組建階段用來將影像和字串資源連結至主應用程式的資源 ( .rc) 檔。</span><span class="sxs-lookup"><span data-stu-id="b28a6-115">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

-   [<span data-ttu-id="b28a6-116">編譯器工作流程</span><span class="sxs-lookup"><span data-stu-id="b28a6-116">Compiler Workflow</span></span>](#compiler-workflow)
-   [<span data-ttu-id="b28a6-117">命令列語法</span><span class="sxs-lookup"><span data-stu-id="b28a6-117">Command-Line Syntax</span></span>](#command-line-syntax)
    -   [<span data-ttu-id="b28a6-118">引數和選項</span><span class="sxs-lookup"><span data-stu-id="b28a6-118">Arguments and Options</span></span>](#arguments-and-options)
    -   [<span data-ttu-id="b28a6-119">範例</span><span class="sxs-lookup"><span data-stu-id="b28a6-119">Example</span></span>](#example)
-   [<span data-ttu-id="b28a6-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b28a6-120">Related topics</span></span>](#related-topics)

## <a name="compiler-workflow"></a><span data-ttu-id="b28a6-121">編譯器工作流程</span><span class="sxs-lookup"><span data-stu-id="b28a6-121">Compiler Workflow</span></span>

<span data-ttu-id="b28a6-122">下圖說明功能區標記編譯器的工作流程。</span><span class="sxs-lookup"><span data-stu-id="b28a6-122">The workflow of the Ribbon markup compiler is illustrated in the following diagram.</span></span>

![顯示功能區標記編譯器工作流程的圖表。](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a><span data-ttu-id="b28a6-124">命令列語法</span><span class="sxs-lookup"><span data-stu-id="b28a6-124">Command-Line Syntax</span></span>

<span data-ttu-id="b28a6-125">下列範例顯示功能區標記編譯器的命令列語法。</span><span class="sxs-lookup"><span data-stu-id="b28a6-125">The command-line syntax for the Ribbon markup compiler is shown in the following example.</span></span>


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a><span data-ttu-id="b28a6-126">引數和選項</span><span class="sxs-lookup"><span data-stu-id="b28a6-126">Arguments and Options</span></span>

<span data-ttu-id="b28a6-127">下表說明此工具的引數和選項。</span><span class="sxs-lookup"><span data-stu-id="b28a6-127">The arguments and options for this tool are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="b28a6-128">所列的命令列選項必須依照指定的順序來指定。</span><span class="sxs-lookup"><span data-stu-id="b28a6-128">The command-line options listed must be specified in the order given.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b28a6-129">選項</span><span class="sxs-lookup"><span data-stu-id="b28a6-129">Option</span></span></th>
<th><span data-ttu-id="b28a6-130">Description</span><span class="sxs-lookup"><span data-stu-id="b28a6-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b28a6-131">/header<headerFile></span><span class="sxs-lookup"><span data-stu-id="b28a6-131">/header:<headerFile></span></span></td>
<td><span data-ttu-id="b28a6-132">產生名為的標頭檔 <headerFile> ，其中包含標記命令識別碼資源符號。</span><span class="sxs-lookup"><span data-stu-id="b28a6-132">Generate a header file called <headerFile> that contains the markup Command ID resource symbols.</span></span> <span data-ttu-id="b28a6-133">如果省略，則不會產生標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b28a6-133">If omitted, a header file is not generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b28a6-134">/res<resourceFile></span><span class="sxs-lookup"><span data-stu-id="b28a6-134">/res:<resourceFile></span></span></td>
<td><span data-ttu-id="b28a6-135">產生稱為的資源檔， <resourceFile> 此檔案會在組建階段將所有影像和字串資源、二進位標記檔和標頭檔連結至主應用程式。</span><span class="sxs-lookup"><span data-stu-id="b28a6-135">Generate a resource file called <resourceFile> that links all image and string resources, the binary markup file, and the header file to the host application at build time.</span></span> <span data-ttu-id="b28a6-136">如果省略，則不會產生資源檔。</span><span class="sxs-lookup"><span data-stu-id="b28a6-136">If omitted, a resource file is not generated.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b28a6-137">/name<ribbonName></span><span class="sxs-lookup"><span data-stu-id="b28a6-137">/name:<ribbonName></span></span></td>
<td><span data-ttu-id="b28a6-138">登入之二進位標記檔案的資源名稱 <resourceFile> 。</span><span class="sxs-lookup"><span data-stu-id="b28a6-138">The resource name for the binary markup file that is logged in the <resourceFile>.</span></span> <span data-ttu-id="b28a6-139">預設值為 APPLICATION_RIBBON。</span><span class="sxs-lookup"><span data-stu-id="b28a6-139">The default is APPLICATION_RIBBON.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b28a6-140">/W{0\1\2}</span><span class="sxs-lookup"><span data-stu-id="b28a6-140">/W{0\1\2}</span></span></td>
<td><span data-ttu-id="b28a6-141">根據嚴重性來篩選事件訊息。</span><span class="sxs-lookup"><span data-stu-id="b28a6-141">Filter the event messages based on severity.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b28a6-142">0</span><span class="sxs-lookup"><span data-stu-id="b28a6-142">0</span></span><br/></td>
<td><span data-ttu-id="b28a6-143">僅限錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b28a6-143">Error messages only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b28a6-144">1</span><span class="sxs-lookup"><span data-stu-id="b28a6-144">1</span></span><br/></td>
<td><span data-ttu-id="b28a6-145">僅限錯誤和警告訊息。</span><span class="sxs-lookup"><span data-stu-id="b28a6-145">Error and Warning messages only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b28a6-146"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="b28a6-146"><strong>2</strong></span></span><br/></td>
<td><span data-ttu-id="b28a6-147">預設值。</span><span class="sxs-lookup"><span data-stu-id="b28a6-147">Default.</span></span> <br/> <span data-ttu-id="b28a6-148">錯誤、警告和參考訊息。</span><span class="sxs-lookup"><span data-stu-id="b28a6-148">Error, Warning, and Informational messages.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a><span data-ttu-id="b28a6-149">範例</span><span class="sxs-lookup"><span data-stu-id="b28a6-149">Example</span></span>

<span data-ttu-id="b28a6-150">下列範例示範如何使用功能區標記編譯器，為功能區應用程式產生一組一般的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b28a6-150">The following example demonstrates how to use the Ribbon markup compiler to generate a typical set of resource files for a Ribbon application.</span></span>

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a><span data-ttu-id="b28a6-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="b28a6-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b28a6-152">使用功能區標記宣告命令和控制項</span><span class="sxs-lookup"><span data-stu-id="b28a6-152">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="b28a6-153">建立功能區應用程式</span><span class="sxs-lookup"><span data-stu-id="b28a6-153">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





