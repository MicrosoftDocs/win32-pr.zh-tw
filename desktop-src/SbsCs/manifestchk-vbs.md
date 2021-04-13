---
description: VBScript 檔案 Manifestchk.vbs 是 Microsoft Windows 軟體開發套件 (SDK) 所提供的驗證工具，可驗證應用程式和組件資訊清單檔。
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386192"
---
# <a name="manifestchkvbs"></a><span data-ttu-id="4802c-103">Manifestchk.vbs</span><span class="sxs-lookup"><span data-stu-id="4802c-103">Manifestchk.vbs</span></span>

<span data-ttu-id="4802c-104">VBScript 檔案 Manifestchk.vbs 是 Microsoft Windows 軟體開發套件 (SDK) 所提供的驗證工具，可驗證應用程式和組件資訊清單檔。</span><span class="sxs-lookup"><span data-stu-id="4802c-104">The VBScript file Manifestchk.vbs is a validation tool provided in the Microsoft Windows Software Development Kit (SDK) that validates application and assembly manifest files.</span></span>

<span data-ttu-id="4802c-105">執行此範例需要 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="4802c-105">Running this sample requires Windows Script Host.</span></span> <span data-ttu-id="4802c-106">如需 Windows Script Host 的詳細資訊，請參閱 Windows SDK 的 Windows Script Host 一節。</span><span class="sxs-lookup"><span data-stu-id="4802c-106">For more information about Windows Script Host, see the Windows Script Host section of the Windows SDK.</span></span> <span data-ttu-id="4802c-107">Windows Script Host 其實是兩部主機。</span><span class="sxs-lookup"><span data-stu-id="4802c-107">Windows Script Host is actually two hosts.</span></span> <span data-ttu-id="4802c-108">CScript.exe 是可讓您從命令提示字元執行腳本的版本。</span><span class="sxs-lookup"><span data-stu-id="4802c-108">CScript.exe is the version that enables you to run scripts from the command prompt.</span></span> <span data-ttu-id="4802c-109">CScript.exe 提供命令列參數來設定腳本屬性。</span><span class="sxs-lookup"><span data-stu-id="4802c-109">CScript.exe provides command-line switches for setting script properties.</span></span>

<span data-ttu-id="4802c-110">命令列格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="4802c-110">The command-line format is the following:</span></span>

<span data-ttu-id="4802c-111">**Cscript//nologo manifestchk.vbs/s：** *\[ drive： \] \[ path \] schemafilename* **/m：** *\[ drive： \] \[ path \] manifestfilename* **\[ /q \] /t：** *選項*</span><span class="sxs-lookup"><span data-stu-id="4802c-111">**Cscript //nologo manifestchk.vbs /s:** *\[drive:\]\[path\]schemafilename* **/m:** *\[drive:\]\[path\]manifestfilename* **\[/q\] /t:** *option*</span></span>

<span data-ttu-id="4802c-112">下表說明為 Manifestchk.vbs 定義的旗標。</span><span class="sxs-lookup"><span data-stu-id="4802c-112">The flags defined for Manifestchk.vbs are described in the following table.</span></span>



| <span data-ttu-id="4802c-113">旗標</span><span class="sxs-lookup"><span data-stu-id="4802c-113">Flag</span></span> | <span data-ttu-id="4802c-114">描述</span><span class="sxs-lookup"><span data-stu-id="4802c-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4802c-115">/s</span><span class="sxs-lookup"><span data-stu-id="4802c-115">/s</span></span>   | <span data-ttu-id="4802c-116">指定要對其驗證資訊清單的資訊清單架構檔案名。</span><span class="sxs-lookup"><span data-stu-id="4802c-116">Specifies the manifest schema file name to validate manifests against.</span></span> <span data-ttu-id="4802c-117">請參閱 [資訊清單檔案架構](manifest-file-schema.md)中的架構。</span><span class="sxs-lookup"><span data-stu-id="4802c-117">See the schema at [Manifest File Schema](manifest-file-schema.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4802c-118">/m</span><span class="sxs-lookup"><span data-stu-id="4802c-118">/m</span></span>   | <span data-ttu-id="4802c-119">指定要驗證的資訊清單檔案名。</span><span class="sxs-lookup"><span data-stu-id="4802c-119">Specifies the manifest file name to validate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4802c-120">/q</span><span class="sxs-lookup"><span data-stu-id="4802c-120">/q</span></span>   | <span data-ttu-id="4802c-121">抑制主控台的所有輸出。</span><span class="sxs-lookup"><span data-stu-id="4802c-121">Suppresses all output to the console.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4802c-122">/t</span><span class="sxs-lookup"><span data-stu-id="4802c-122">/t</span></span>   | <span data-ttu-id="4802c-123">指定資訊清單檔的類型。</span><span class="sxs-lookup"><span data-stu-id="4802c-123">Specifies the type of manifest file.</span></span> <span data-ttu-id="4802c-124">有效值為： AM 驗證[組件資訊清單](assembly-manifests.md)或[應用程式指令](application-manifests.md)清單的[資訊清單檔架構](manifest-file-schema.md)</span><span class="sxs-lookup"><span data-stu-id="4802c-124">The valid values are: AM   Validate the [manifest file schema](manifest-file-schema.md) of an [assembly manifest](assembly-manifests.md) or [application manifest](application-manifests.md)</span></span><br/> <span data-ttu-id="4802c-125">電腦驗證[發行者設定檔](publisher-configuration-files.md)的[發行者設定檔架構](publisher-configuration-file-schema.md)</span><span class="sxs-lookup"><span data-stu-id="4802c-125">PC   Validate the [publisher configuration file schema](publisher-configuration-file-schema.md) of a [publisher configuration file](publisher-configuration-files.md)</span></span><br/> <span data-ttu-id="4802c-126">AC 驗證 [應用程式佈建檔](application-configuration-files.md)的應用程式佈建檔架構。</span><span class="sxs-lookup"><span data-stu-id="4802c-126">AC   Validate the application configuration file schema of an [application configuration file](application-configuration-files.md).</span></span><br/> |



 

<span data-ttu-id="4802c-127">如果未指定/q 旗標，Manifestchk.vbs 會顯示檔案中第一個錯誤的詳細資訊，並顯示一則訊息，指出驗證程式是否成功。</span><span class="sxs-lookup"><span data-stu-id="4802c-127">If the /q flag is not specified, Manifestchk.vbs displays detailed information about the first error encountered in the file, and displays a message stating whether the validation process was successful or not.</span></span>

<span data-ttu-id="4802c-128">此公用程式會檢查下列各項：</span><span class="sxs-lookup"><span data-stu-id="4802c-128">This utility checks for the following:</span></span>

-   <span data-ttu-id="4802c-129">有效的命令列。</span><span class="sxs-lookup"><span data-stu-id="4802c-129">A valid command line.</span></span>
-   <span data-ttu-id="4802c-130">已安裝 MSXML 第3版。</span><span class="sxs-lookup"><span data-stu-id="4802c-130">That MSXML version 3 is installed.</span></span>
-   <span data-ttu-id="4802c-131">資訊清單會使用格式正確的 XML。</span><span class="sxs-lookup"><span data-stu-id="4802c-131">That the manifest uses well-formed XML.</span></span>
-   <span data-ttu-id="4802c-132">資訊清單同意提供的架構。</span><span class="sxs-lookup"><span data-stu-id="4802c-132">That the manifest agrees with the provided schema.</span></span> <span data-ttu-id="4802c-133">請注意，Manifestchk.vbs 只會根據提供的架構中指定的內容來驗證資訊清單檔。</span><span class="sxs-lookup"><span data-stu-id="4802c-133">Note that Manifestchk.vbs verifies the manifest file based only on what is specified in the provided schema.</span></span> <span data-ttu-id="4802c-134">如需資訊清單架構的範例，請參閱 [資訊清單檔案架構](manifest-file-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="4802c-134">For an example of a manifest schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="4802c-135">如果驗證程式成功，Cscript.exe 會傳回值0，如果失敗，則傳回1。</span><span class="sxs-lookup"><span data-stu-id="4802c-135">Cscript.exe returns a value of 0 if the validation process was successful and 1 if it was not successful.</span></span> <span data-ttu-id="4802c-136">如果命令列引數中有錯誤，則會傳回2。</span><span class="sxs-lookup"><span data-stu-id="4802c-136">It returns 2 if there is an error in a command line argument.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4802c-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="4802c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4802c-138">並存元件開發工具</span><span class="sxs-lookup"><span data-stu-id="4802c-138">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




