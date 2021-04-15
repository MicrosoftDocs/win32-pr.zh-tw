---
title: MIDLRT.EXE 根據和 Windows 執行階段元件
description: 顯示如何建立中繼資料 ( winmd) 檔案，這些檔案代表自訂 Windows 執行階段元件的 API。
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL 編譯器 MIDL
- MIDL 編譯器 MIDL、MIDL 和 Windows 執行階段 winrt
- Windows 執行階段 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508200"
---
# <a name="midlrt-and-windows-runtime-components"></a><span data-ttu-id="80c33-106">MIDLRT.EXE 根據和 Windows 執行階段元件</span><span class="sxs-lookup"><span data-stu-id="80c33-106">MIDLRT and Windows Runtime components</span></span>

<span data-ttu-id="80c33-107">顯示如何建立中繼資料 ( winmd) 檔案，這些檔案代表自訂 Windows 執行階段元件的 API。</span><span class="sxs-lookup"><span data-stu-id="80c33-107">Shows how to create metadata (.winmd) files that represent the API for custom Windows Runtime components.</span></span>


<span data-ttu-id="80c33-108">使用 MIDLRT.EXE 根據編譯器，針對您的自訂 Windows 執行階段元件 ( winmd) 檔案建立中繼資料。</span><span class="sxs-lookup"><span data-stu-id="80c33-108">Use the MIDLRT compiler to build metadata (.winmd) files for your custom Windows Runtime components.</span></span>

<span data-ttu-id="80c33-109">產生中繼資料檔案時，您可以使用 MDMERGE 公用程式，將它們組成更有效率的封裝。</span><span class="sxs-lookup"><span data-stu-id="80c33-109">When your metadata files are generated, you can compose them into a more efficient package by using the MDMERGE utility.</span></span> <span data-ttu-id="80c33-110">如需詳細資訊，請參閱 [MDMERGE 和中繼資料](mdmerge-and-metadata-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="80c33-110">For more info, see [MDMERGE and metadata files](mdmerge-and-metadata-files.md).</span></span>


<span data-ttu-id="80c33-111">使用 MIDLRT.EXE 根據類似于使用 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="80c33-111">Using MIDLRT is similar to using the MIDL compiler.</span></span> <span data-ttu-id="80c33-112">使用下列命令，從命令列執行 MIDLRT.EXE 根據：</span><span class="sxs-lookup"><span data-stu-id="80c33-112">Run MIDLRT from the command line using the following command:</span></span>

<span data-ttu-id="80c33-113">**midlrt.exe 根據**  *<\*\*\*選項*\* _>_**檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="80c33-113">**midlrt** \*<\***options**_>_ **filename.idl**</span></span>

<span data-ttu-id="80c33-114">其中 \* < \***選項** _>_ 表示您想要使用的命令列選項，而 Filename 則是要編譯之 idl 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="80c33-114">where \*<\***options**_>_ represents the command-line options you want to use, and Filename.idl is the name of the IDL file to compile.</span></span>


<span data-ttu-id="80c33-115">下列清單顯示 MIDLRT.EXE 使用的命令列參數。</span><span class="sxs-lookup"><span data-stu-id="80c33-115">The following list shows the command-line switches that MIDLRT.EXE uses.</span></span>

<dl>

[<span data-ttu-id="80c33-116">**/enum \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="80c33-116">**/enum\_class**</span></span>](-enum-class.md)  
[<span data-ttu-id="80c33-117">**/metadata \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="80c33-117">**/metadata\_dir**</span></span>](-metadata-dir.md)  
[<span data-ttu-id="80c33-118">**/nomidl**</span><span class="sxs-lookup"><span data-stu-id="80c33-118">**/nomidl**</span></span>](-nomidl.md)  
[<span data-ttu-id="80c33-119">**/nomd**</span><span class="sxs-lookup"><span data-stu-id="80c33-119">**/nomd**</span></span>](-nomd.md)  
[<span data-ttu-id="80c33-120">**/ns \_ 前置詞**</span><span class="sxs-lookup"><span data-stu-id="80c33-120">**/ns\_prefix**</span></span>](-ns-prefix.md)  
[<span data-ttu-id="80c33-121">**/winmd**</span><span class="sxs-lookup"><span data-stu-id="80c33-121">**/winmd**</span></span>](-winmd.md)  
[<span data-ttu-id="80c33-122">**/winrt**</span><span class="sxs-lookup"><span data-stu-id="80c33-122">**/winrt**</span></span>](-winrt.md)  
</dl>

<span data-ttu-id="80c33-123">當您使用 MIDLRT.EXE 根據編譯器 [**/help**](-help-.md) 和/？時，可使用 midlrt.exe 根據編譯器參數和選項的完整清單。</span><span class="sxs-lookup"><span data-stu-id="80c33-123">A complete listing of MIDLRT compiler switches and options is available when you use the MIDLRT compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="80c33-124">開關。</span><span class="sxs-lookup"><span data-stu-id="80c33-124">switches.</span></span> <span data-ttu-id="80c33-125">這些參數是依類別目錄組織。</span><span class="sxs-lookup"><span data-stu-id="80c33-125">The switches are organized by categories.</span></span> <span data-ttu-id="80c33-126">如需詳細資訊，請參閱 [MIDL Command-Line 參考](midl-command-line-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="80c33-126">For more info, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80c33-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="80c33-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c33-128">MDMERGE 和中繼資料檔案</span><span class="sxs-lookup"><span data-stu-id="80c33-128">MDMERGE and metadata files</span></span>](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




