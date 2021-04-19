---
description: 本主題說明如何建立一般的 MUI 應用程式。
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: 當地語系化資源和建立應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979025"
---
# <a name="localizing-resources-and-building-the-application"></a><span data-ttu-id="def28-103">當地語系化資源和建立應用程式</span><span class="sxs-lookup"><span data-stu-id="def28-103">Localizing Resources and Building the Application</span></span>

<span data-ttu-id="def28-104">本主題說明如何建立一般的 MUI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="def28-104">This topic describes how to build a typical MUI application.</span></span> <span data-ttu-id="def28-105">假設您使用 Microsoft Visual Studio 進行程式碼撰寫，並使用 Microsoft Visual Studio 或 Visual Studio 命令列進行建立。</span><span class="sxs-lookup"><span data-stu-id="def28-105">It is assumed that you are using Microsoft Visual Studio for coding and either Microsoft Visual Studio or the Visual Studio command line for building.</span></span> <span data-ttu-id="def28-106">假設您的應用程式使用 .sln 方案檔，並支援資源 .h 檔案來反映基礎語言資源檔。</span><span class="sxs-lookup"><span data-stu-id="def28-106">You are assumed to use an .sln solution file for your application and support a Resource.h file to reflect the base language resource file.</span></span>

> [!Note]  
> <span data-ttu-id="def28-107">如果使用組建的 Visual Studio 命令列，您將使用 **vcbuild** 命令來建立方案檔。</span><span class="sxs-lookup"><span data-stu-id="def28-107">If using the Visual Studio command line for the build, you will use the **vcbuild** command to build the solution file.</span></span>

 

<span data-ttu-id="def28-108">應用程式檔會針對每種語言分別建立。</span><span class="sxs-lookup"><span data-stu-id="def28-108">Application files are built separately for each language.</span></span> <span data-ttu-id="def28-109">每個組建都會建立與語言無關的相同 .exe 和特定語言的 .exe 檔案。</span><span class="sxs-lookup"><span data-stu-id="def28-109">Each build creates identical language-neutral .exe and language-specific .exe.mui files.</span></span> <span data-ttu-id="def28-110">此外，會將不同的其他檔案複製到適當的發行資料夾。</span><span class="sxs-lookup"><span data-stu-id="def28-110">In addition, various other files are copied to the appropriate release folders.</span></span>

<span data-ttu-id="def28-111">應用程式組建取決於您所使用的資源類型和當地語系化類型。</span><span class="sxs-lookup"><span data-stu-id="def28-111">The application build depends on the type of resources and the type of localization that you are using.</span></span> <span data-ttu-id="def28-112">針對預先組建當地語系化，您有一份針對每個支援語言當地語系化的基礎語言檔案。</span><span class="sxs-lookup"><span data-stu-id="def28-112">For pre-build localization, you have one copy of the base language file localized for each supported language.</span></span> <span data-ttu-id="def28-113">針對組建後當地語系化，您可以複製可執行檔和資源模組的組建所產生的 mui 檔案，並將這些複本提供給當地語系化人員。</span><span class="sxs-lookup"><span data-stu-id="def28-113">For post-build localization, you can copy the .mui file resulting from the build of the executable and resource module, and provide the copies to the localizers.</span></span>

> [!Note]  
> <span data-ttu-id="def28-114">下列程式假設 Win32 PE 資源具有一個針對每個語言建立的 Visual Studio 專案。</span><span class="sxs-lookup"><span data-stu-id="def28-114">The following procedure assumes Win32 PE resources with one Visual Studio project built for each language.</span></span> <span data-ttu-id="def28-115">在 .rc 檔中提供基礎語言資源，並使用 DLL 模組載入。</span><span class="sxs-lookup"><span data-stu-id="def28-115">The base language resources are provided in an .rc file and loaded using a DLL module.</span></span> <span data-ttu-id="def28-116">您可以視需要重複此程式，以建立支援的所有語言。</span><span class="sxs-lookup"><span data-stu-id="def28-116">You can repeat the procedure as needed to build for all languages supported.</span></span>

 

<span data-ttu-id="def28-117">**若要建立應用程式**</span><span class="sxs-lookup"><span data-stu-id="def28-117">**To build the application**</span></span>

1.  <span data-ttu-id="def28-118">設定基礎語言的 Visual Studio 專案。</span><span class="sxs-lookup"><span data-stu-id="def28-118">Set up a Visual Studio project for the base language.</span></span>
2.  <span data-ttu-id="def28-119">如果有興趣使用資源設定檔與資源工具，請依照 [準備資源設定檔](preparing-a-resource-configuration-file.md)中所述的方式設定一個。</span><span class="sxs-lookup"><span data-stu-id="def28-119">If interested in using a resource configuration file with the resource tools, set one up as described in [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>
3.  <span data-ttu-id="def28-120">在專案的屬性頁中，設定 RC 編譯器公用程式所需的參數，[設定屬性] → [資源] → [ **命令列] → [其他選項**]。</span><span class="sxs-lookup"><span data-stu-id="def28-120">Set parameters required by the RC Compiler utility in the property pages for the project under **Configuration Properties → Resources → Command Line → Additional options**.</span></span>
4.  <span data-ttu-id="def28-121">執行 RC 編譯器。</span><span class="sxs-lookup"><span data-stu-id="def28-121">Run RC Compiler.</span></span> <span data-ttu-id="def28-122">此公用程式會使用資源設定資料，將不可當地語系化和可當地語系化的資源編譯並分割成兩個不同的物件檔案。</span><span class="sxs-lookup"><span data-stu-id="def28-122">The utility compiles and splits the non-localizable and localizable resources into two different object files, using resource configuration data.</span></span> <span data-ttu-id="def28-123">在這個步驟中，語言中立的資源會連結到 LN 檔。</span><span class="sxs-lookup"><span data-stu-id="def28-123">In this step the language-neutral resources are linked into an LN file.</span></span> <span data-ttu-id="def28-124">如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md)中的公用程式描述。</span><span class="sxs-lookup"><span data-stu-id="def28-124">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
5.  <span data-ttu-id="def28-125">若要將特定語言的資源連結到特定語言的 mui 檔，請在 [設定屬性] → [組建事件] → [ **建立後事件] →命令列** 底下的屬性頁中，為專案設定建立後事件。</span><span class="sxs-lookup"><span data-stu-id="def28-125">To link the language-specific resources into a language-specific .mui file, set a post-build event for the project in the property pages under **Configuration Properties → Build Events → Post-Build Event → Command Line**.</span></span>
6.  <span data-ttu-id="def28-126">設定建立後事件，以將 LN 檔中的總和檢查碼值套用至語言的 mui 檔。</span><span class="sxs-lookup"><span data-stu-id="def28-126">Set a post-build event to apply the checksum value from the LN file to the .mui file for the language.</span></span> <span data-ttu-id="def28-127">您可以使用 MUIRCT 公用程式進行此步驟。</span><span class="sxs-lookup"><span data-stu-id="def28-127">You can use the MUIRCT utility for this step.</span></span> <span data-ttu-id="def28-128">如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md)中的公用程式描述。</span><span class="sxs-lookup"><span data-stu-id="def28-128">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
7.  <span data-ttu-id="def28-129">使用後置事件命令列新增命令，以將檔案複製到適當的發行資料夾結構。</span><span class="sxs-lookup"><span data-stu-id="def28-129">Use the post-build event command line to add commands to copy the files into the appropriate release folder structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="def28-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="def28-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="def28-131">使用多語系消費者介面</span><span class="sxs-lookup"><span data-stu-id="def28-131">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="def28-132">準備資源設定檔</span><span class="sxs-lookup"><span data-stu-id="def28-132">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="def28-133">資源公用程式</span><span class="sxs-lookup"><span data-stu-id="def28-133">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



