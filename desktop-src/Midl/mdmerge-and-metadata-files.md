---
title: MDMERGE 和中繼資料檔案
description: 根據命名空間，將多個中繼資料 ( winmd) 檔案組成多個輸出中繼資料檔案。
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- 中繼資料
- winmd 檔案
- Windows 中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931947"
---
# <a name="mdmerge-and-metadata-files"></a><span data-ttu-id="e7bc7-106">MDMERGE 和中繼資料檔案</span><span class="sxs-lookup"><span data-stu-id="e7bc7-106">MDMERGE and metadata files</span></span>

<span data-ttu-id="e7bc7-107">根據命名空間，將多個中繼資料 ( winmd) 檔案組成多個輸出中繼資料檔案。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-107">Composes multiple metadata (.winmd) files into a number of output metadata files, based on namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="e7bc7-108">使用方式</span><span class="sxs-lookup"><span data-stu-id="e7bc7-108">Usage</span></span>

<span data-ttu-id="e7bc7-109">使用下列命令，從命令列執行 MDMERGE：</span><span class="sxs-lookup"><span data-stu-id="e7bc7-109">Run MDMERGE from the command line using the following command:</span></span>

<span data-ttu-id="e7bc7-110">**mdmerge** *< ***選項***>*</span><span class="sxs-lookup"><span data-stu-id="e7bc7-110">**mdmerge** *<***options***>*</span></span>

<span data-ttu-id="e7bc7-111">其中的 *< ***選項*** >* 代表您要使用的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-111">where *<***options***>* represents the command-line options you want to use.</span></span>

<span data-ttu-id="e7bc7-112">使用 MIDLRT.EXE 根據編譯器產生自訂 Windows 執行階段元件的中繼資料檔案。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-112">Generate metadata files for your custom Windows Runtime components by using the MIDLRT compiler.</span></span> <span data-ttu-id="e7bc7-113">如需詳細資訊，請參閱 [midlrt.exe 根據和 Windows 執行階段元件](midlrt-and-windows-runtime-components.md)。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-113">For more info, see [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).</span></span>

## <a name="command-line-switches"></a><span data-ttu-id="e7bc7-114">命令列參數</span><span class="sxs-lookup"><span data-stu-id="e7bc7-114">Command-line switches</span></span>

<span data-ttu-id="e7bc7-115">下列清單顯示 MDMERGE 使用的命令列參數。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-115">The following list shows the command-line switches that MDMERGE uses.</span></span>

<dl>

[<span data-ttu-id="e7bc7-116">**/i**</span><span class="sxs-lookup"><span data-stu-id="e7bc7-116">**/i**</span></span>](-mdmerge-i.md)  
[<span data-ttu-id="e7bc7-117">**/metadata \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="e7bc7-117">**/metadata\_dir**</span></span>](-mdmerge-metadata-dir.md)  
[<span data-ttu-id="e7bc7-118">**n**</span><span class="sxs-lookup"><span data-stu-id="e7bc7-118">**/n**</span></span>](-mdmerge-n.md)  
[<span data-ttu-id="e7bc7-119">**/o**</span><span class="sxs-lookup"><span data-stu-id="e7bc7-119">**/o**</span></span>](-mdmerge-o.md)  
[<span data-ttu-id="e7bc7-120">**/partial**</span><span class="sxs-lookup"><span data-stu-id="e7bc7-120">**/partial**</span></span>](-mdmerge-partial.md)  
[<span data-ttu-id="e7bc7-121">**/v**</span><span class="sxs-lookup"><span data-stu-id="e7bc7-121">**/v**</span></span>](-mdmerge-v.md)  
</dl>

<span data-ttu-id="e7bc7-122">當您使用 **-h** 和 **/？** 時，可使用 MDMERGE 編譯器參數和選項的完整清單。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-122">A complete listing of MDMERGE compiler switches and options is available when you use the **-h** and **/?**</span></span> <span data-ttu-id="e7bc7-123">開關。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-123">switches.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7bc7-124">備註</span><span class="sxs-lookup"><span data-stu-id="e7bc7-124">Remarks</span></span>

<span data-ttu-id="e7bc7-125">中繼資料組合可讓多個 IDL 檔案包含相同命名空間中 Windows 執行階段元件的定義。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-125">Metadata composition enables multiple IDL files to contain definitions for Windows Runtime components in the same namespace.</span></span> <span data-ttu-id="e7bc7-126">這可讓您無法在單一 IDL 檔案內的命名空間中定義所有類型。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-126">This frees you from defining all of the types in a namespace within a single IDL file.</span></span>

<span data-ttu-id="e7bc7-127">您的應用程式所使用的 Windows 執行階段元件可能很多。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-127">You're likely to have numerous Windows Runtime components that your apps use.</span></span> <span data-ttu-id="e7bc7-128">當您執行最後一個步驟來產生可部署的 Windows 執行階段中繼資料元件時，您可以將 MDMERGE 設定為合併多個中繼資料目錄中的元件，例如與系統一起安裝的元件 (% WINDOWS% \\ system32 \\ WinMetadata) 、您的基礎類型，以及目前專案的組建目錄。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-128">When you perform the final step to produce deployable Windows Runtime metadata assemblies, you can configure MDMERGE to merge components from multiple metadata directories, like those that are installed with the system (%WINDOWS%\\system32\\WinMetadata), your foundation types, and your current project’s build directory.</span></span> <span data-ttu-id="e7bc7-129">所有必要的型別都會合並到可供您針對 Windows Store 封裝的正確、可部署的中繼資料元件。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-129">All necessary types are merged into the correct, deployable, metadata assemblies that you can package for the Windows Store.</span></span>

<span data-ttu-id="e7bc7-130">您可以使用 [**/n**](-mdmerge-n.md) 選項來指定所支援的命名空間深度，以撰寫中繼資料元件。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-130">You can use the [**/n**](-mdmerge-n.md) option to specify the supported namespace depth for composing metadata assemblies.</span></span> <span data-ttu-id="e7bc7-131">這可讓您設定 Windows 執行階段元件的熱分割，因此只會封裝單一的 winmd 檔案，而不是多個檔案。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-131">This enables configuring a hot split for your Windows Runtime components, so that only a single .winmd file is packaged instead of many.</span></span> <span data-ttu-id="e7bc7-132">這可減少 Windows Store 應用程式所需的載入時間和檔案 i/o。</span><span class="sxs-lookup"><span data-stu-id="e7bc7-132">This reduces the load times and file I/O required by your Windows Store apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7bc7-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7bc7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7bc7-134">MIDLRT.EXE 根據和 Windows 執行階段元件</span><span class="sxs-lookup"><span data-stu-id="e7bc7-134">MIDLRT and Windows Runtime components</span></span>](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




