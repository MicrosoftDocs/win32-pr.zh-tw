---
description: 本節說明如何將資源字串加入 Windows Installer 的快捷方式資料表中，以供 (MUI) 的多語系使用者介面使用。
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: MUI 快捷方式範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0392713c1eaedabaa989baecd79478a9b329e955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988761"
---
# <a name="a-mui-shortcut-example"></a><span data-ttu-id="b08ae-103">MUI 快捷方式範例</span><span class="sxs-lookup"><span data-stu-id="b08ae-103">A MUI Shortcut Example</span></span>

<span data-ttu-id="b08ae-104">本節說明如何將資源字串加入 Windows Installer 的 [快捷方式](shortcut-table.md) 資料表中，以供 (MUI) 的多語系使用者介面使用。</span><span class="sxs-lookup"><span data-stu-id="b08ae-104">This section describes how to add resource strings to the Windows Installer [Shortcut](shortcut-table.md) table for use with Multilingual User Interfaces (MUI).</span></span>

<span data-ttu-id="b08ae-105">**Windows Installer 2.0 和 Windows Installer 3.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="b08ae-105">**Windows Installer 2.0 and Windows Installer 3.0:** Not supported.</span></span> <span data-ttu-id="b08ae-106">此範例需要 Windows Installer 4.0。</span><span class="sxs-lookup"><span data-stu-id="b08ae-106">This example requires Windows Installer 4.0.</span></span>

<span data-ttu-id="b08ae-107">如需如何開發具備 MUI 功能的應用程式的相關資訊，請參閱 [多語系消費者介面 (MUI) ](/windows/desktop/Intl/multilingual-user-interface) 檔。</span><span class="sxs-lookup"><span data-stu-id="b08ae-107">Refer to the [Multilingual User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) documentation for information on how to develop MUI-enabled applications .</span></span>

<span data-ttu-id="b08ae-108">若要將 Windows Vista 多語系使用者介面所使用的資源字串新增至 Windows Installer 套件：</span><span class="sxs-lookup"><span data-stu-id="b08ae-108">To add the resource strings used by Windows Vista Multilingual User Interfaces to a Windows Installer package:</span></span>

1.  <span data-ttu-id="b08ae-109">將所有語言中性和語言檔案的資訊新增至檔案 [資料表](file-table.md)。</span><span class="sxs-lookup"><span data-stu-id="b08ae-109">Add the information for all the language-neutral and language files to the [File Table](file-table.md).</span></span> <span data-ttu-id="b08ae-110">例如，檔案可能包含語言中性檔案 (msimsg.dll) 和英文的語言檔案（英文） (msimsgen.dll mui) 、日文 (msimsgja.dll mui) 和中文 (msimsgcs.dll mui) 。</span><span class="sxs-lookup"><span data-stu-id="b08ae-110">For example, the files might consist of a language-neutral file (msimsg.dll) and language files for English (msimsgen.dll.mui), Japanese (msimsgja.dll.mui), and Chinese (msimsgcs.dll.mui).</span></span> <span data-ttu-id="b08ae-111">每個檔案都可以屬於不同的元件。</span><span class="sxs-lookup"><span data-stu-id="b08ae-111">Each file can belong to a different component.</span></span> <span data-ttu-id="b08ae-112">每個檔案都可以同時具有完整和簡短的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b08ae-112">Each file can have both a long and short file name.</span></span> <span data-ttu-id="b08ae-113">在此範例中，您可以將下列資訊新增至檔案 [資料表](file-table.md)。</span><span class="sxs-lookup"><span data-stu-id="b08ae-113">In the case of this example, the following information can be added to the [File Table](file-table.md).</span></span>

    <span data-ttu-id="b08ae-114">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b08ae-114">[File Table](file-table.md) (partial)</span></span>

    

    | <span data-ttu-id="b08ae-115">檔案</span><span class="sxs-lookup"><span data-stu-id="b08ae-115">File</span></span>        | <span data-ttu-id="b08ae-116">元件\_</span><span class="sxs-lookup"><span data-stu-id="b08ae-116">Component\_</span></span>     | <span data-ttu-id="b08ae-117">FileName</span><span class="sxs-lookup"><span data-stu-id="b08ae-117">FileName</span></span>                     |
    |-------------|-----------------|------------------------------|
    | <span data-ttu-id="b08ae-118">msimsgmuija</span><span class="sxs-lookup"><span data-stu-id="b08ae-118">msimsgmuija</span></span> | <span data-ttu-id="b08ae-119">MSIMSG \_ MUI \_ JA-JP</span><span class="sxs-lookup"><span data-stu-id="b08ae-119">MSIMSG\_MUI\_JA</span></span> | <span data-ttu-id="b08ae-120">msimsgja.dll\|msimsg.dll mui</span><span class="sxs-lookup"><span data-stu-id="b08ae-120">msimsgja.dll\|msimsg.dll.mui</span></span> |
    | <span data-ttu-id="b08ae-121">msimsgmuics</span><span class="sxs-lookup"><span data-stu-id="b08ae-121">msimsgmuics</span></span> | <span data-ttu-id="b08ae-122">MSIMSG \_ MUI \_ CS</span><span class="sxs-lookup"><span data-stu-id="b08ae-122">MSIMSG\_MUI\_CS</span></span> | <span data-ttu-id="b08ae-123">msimsgcs.dll\|msimsg.dll mui</span><span class="sxs-lookup"><span data-stu-id="b08ae-123">msimsgcs.dll\|msimsg.dll.mui</span></span> |
    | <span data-ttu-id="b08ae-124">msimsgmuien</span><span class="sxs-lookup"><span data-stu-id="b08ae-124">msimsgmuien</span></span> | <span data-ttu-id="b08ae-125">MSIMSG \_ MUI \_ EN</span><span class="sxs-lookup"><span data-stu-id="b08ae-125">MSIMSG\_MUI\_EN</span></span> | <span data-ttu-id="b08ae-126">msimsgen.dll\|msimsg.dll mui</span><span class="sxs-lookup"><span data-stu-id="b08ae-126">msimsgen.dll\|msimsg.dll.mui</span></span> |
    | <span data-ttu-id="b08ae-127">msimsgdll</span><span class="sxs-lookup"><span data-stu-id="b08ae-127">msimsgdll</span></span>   | <span data-ttu-id="b08ae-128">MSIMSG</span><span class="sxs-lookup"><span data-stu-id="b08ae-128">MSIMSG</span></span>          | <span data-ttu-id="b08ae-129">msimsg.dll</span><span class="sxs-lookup"><span data-stu-id="b08ae-129">msimsg.dll</span></span>                   |

    

     

2.  <span data-ttu-id="b08ae-130">將資訊新增至這些元件的 [元件資料表](component-table.md) 中。</span><span class="sxs-lookup"><span data-stu-id="b08ae-130">Add information to the [Component table](component-table.md) for these components.</span></span> <span data-ttu-id="b08ae-131">每個元件都有唯一的 GUID 識別碼，應該輸入至元件資料表的 [元件識別碼] 欄位。</span><span class="sxs-lookup"><span data-stu-id="b08ae-131">Each component has a unique GUID identifier that should be entered into the ComponentId field of the Component table.</span></span> <span data-ttu-id="b08ae-132">屬於元件的檔案可作為該元件的 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="b08ae-132">The file belonging to the component can serve as the KeyPath for that component.</span></span> <span data-ttu-id="b08ae-133">您可以在 [目錄] 欄位中指定包含每個元件的目錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b08ae-133">The directory that contains each component can be specified in the Directory\_ field.</span></span> <span data-ttu-id="b08ae-134">您可以將下列資訊加入元件資料表中。</span><span class="sxs-lookup"><span data-stu-id="b08ae-134">The following information can be added to the Component table.</span></span>

    <span data-ttu-id="b08ae-135">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b08ae-135">[Component Table](component-table.md) (partial)</span></span>

    

    | <span data-ttu-id="b08ae-136">元件</span><span class="sxs-lookup"><span data-stu-id="b08ae-136">Component</span></span>       | <span data-ttu-id="b08ae-137">目錄\_</span><span class="sxs-lookup"><span data-stu-id="b08ae-137">Directory\_</span></span>   | <span data-ttu-id="b08ae-138">KeyPath</span><span class="sxs-lookup"><span data-stu-id="b08ae-138">KeyPath</span></span>     |
    |-----------------|---------------|-------------|
    | <span data-ttu-id="b08ae-139">MSIMSG \_ MUI \_ JA-JP</span><span class="sxs-lookup"><span data-stu-id="b08ae-139">MSIMSG\_MUI\_JA</span></span> | <span data-ttu-id="b08ae-140">MUIFolder \_ ja-jp</span><span class="sxs-lookup"><span data-stu-id="b08ae-140">MUIFolder\_JA</span></span> | <span data-ttu-id="b08ae-141">msimsgmuija</span><span class="sxs-lookup"><span data-stu-id="b08ae-141">msimsgmuija</span></span> |
    | <span data-ttu-id="b08ae-142">MSIMSG \_ MUI \_ CS</span><span class="sxs-lookup"><span data-stu-id="b08ae-142">MSIMSG\_MUI\_CS</span></span> | <span data-ttu-id="b08ae-143">MUIFolder \_ CS</span><span class="sxs-lookup"><span data-stu-id="b08ae-143">MUIFolder\_CS</span></span> | <span data-ttu-id="b08ae-144">msimsgmuics</span><span class="sxs-lookup"><span data-stu-id="b08ae-144">msimsgmuics</span></span> |
    | <span data-ttu-id="b08ae-145">MSIMSG \_ MUI \_ EN</span><span class="sxs-lookup"><span data-stu-id="b08ae-145">MSIMSG\_MUI\_EN</span></span> | <span data-ttu-id="b08ae-146">MUIFolder \_ EN</span><span class="sxs-lookup"><span data-stu-id="b08ae-146">MUIFolder\_EN</span></span> | <span data-ttu-id="b08ae-147">msimsgmuien</span><span class="sxs-lookup"><span data-stu-id="b08ae-147">msimsgmuien</span></span> |
    | <span data-ttu-id="b08ae-148">MSIMSG</span><span class="sxs-lookup"><span data-stu-id="b08ae-148">MSIMSG</span></span>          | <span data-ttu-id="b08ae-149">MUIFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-149">MUIFolder</span></span>     | <span data-ttu-id="b08ae-150">msimsgdll</span><span class="sxs-lookup"><span data-stu-id="b08ae-150">msimsgdll</span></span>   |

    

     

3.  <span data-ttu-id="b08ae-151">編輯 [目錄](directory-table.md) 資料表，讓元件安裝在正確的目錄中。</span><span class="sxs-lookup"><span data-stu-id="b08ae-151">Edit the [Directory](directory-table.md) table so that the components are installed into the correct directories.</span></span> <span data-ttu-id="b08ae-152">請務必包含要安裝快捷方式之目錄的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b08ae-152">Be sure to include information about the directory where the shortcut will be installed.</span></span> <span data-ttu-id="b08ae-153">例如，下列資訊可能會新增至封裝的目錄資料表，以安裝元件和位於 DesktopFolder 目錄中的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="b08ae-153">For example, the following information might be added to the Directory table of a package that installs the components and a shortcut located in the DesktopFolder directory.</span></span>

    <span data-ttu-id="b08ae-154">[目錄資料表](directory-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b08ae-154">[Directory Table](directory-table.md) (partial)</span></span>

    

    | <span data-ttu-id="b08ae-155">目錄</span><span class="sxs-lookup"><span data-stu-id="b08ae-155">Directory</span></span>     | <span data-ttu-id="b08ae-156">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="b08ae-156">Directory\_Parent</span></span> | <span data-ttu-id="b08ae-157">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="b08ae-157">DefaultDir</span></span> |
    |---------------|-------------------|------------|
    | <span data-ttu-id="b08ae-158">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b08ae-158">TARGETDIR</span></span>     |                   | <span data-ttu-id="b08ae-159">SourceDir</span><span class="sxs-lookup"><span data-stu-id="b08ae-159">SourceDir</span></span>  |
    | <span data-ttu-id="b08ae-160">MsiTest</span><span class="sxs-lookup"><span data-stu-id="b08ae-160">MsiTest</span></span>       | <span data-ttu-id="b08ae-161">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b08ae-161">TARGETDIR</span></span>         | <span data-ttu-id="b08ae-162">MsiTest:.</span><span class="sxs-lookup"><span data-stu-id="b08ae-162">MsiTest:.</span></span>  |
    | <span data-ttu-id="b08ae-163">MUIFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-163">MUIFolder</span></span>     | <span data-ttu-id="b08ae-164">MsiTest</span><span class="sxs-lookup"><span data-stu-id="b08ae-164">MsiTest</span></span>           | <span data-ttu-id="b08ae-165">梅</span><span class="sxs-lookup"><span data-stu-id="b08ae-165">MUI</span></span>        |
    | <span data-ttu-id="b08ae-166">MUIFolder \_ CS</span><span class="sxs-lookup"><span data-stu-id="b08ae-166">MUIFolder\_CS</span></span> | <span data-ttu-id="b08ae-167">MUIFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-167">MUIFolder</span></span>         | <span data-ttu-id="b08ae-168">cs-CZ</span><span class="sxs-lookup"><span data-stu-id="b08ae-168">cs-CZ</span></span>      |
    | <span data-ttu-id="b08ae-169">MUIFolder \_ EN</span><span class="sxs-lookup"><span data-stu-id="b08ae-169">MUIFolder\_EN</span></span> | <span data-ttu-id="b08ae-170">MUIFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-170">MUIFolder</span></span>         | <span data-ttu-id="b08ae-171">en-US</span><span class="sxs-lookup"><span data-stu-id="b08ae-171">en-US</span></span>      |
    | <span data-ttu-id="b08ae-172">MUIFolder \_ ja-jp</span><span class="sxs-lookup"><span data-stu-id="b08ae-172">MUIFolder\_JA</span></span> | <span data-ttu-id="b08ae-173">MUIFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-173">MUIFolder</span></span>         | <span data-ttu-id="b08ae-174">ja-JP</span><span class="sxs-lookup"><span data-stu-id="b08ae-174">ja-JP</span></span>      |
    | <span data-ttu-id="b08ae-175">DesktopFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-175">DesktopFolder</span></span> | <span data-ttu-id="b08ae-176">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b08ae-176">TARGETDIR</span></span>         | <span data-ttu-id="b08ae-177">.</span><span class="sxs-lookup"><span data-stu-id="b08ae-177">.</span></span>          |

    

     

4.  <span data-ttu-id="b08ae-178">將資料列新增至每個快捷方式的 [快速鍵](shortcut-table.md) 對應表。</span><span class="sxs-lookup"><span data-stu-id="b08ae-178">Add a row to the [Shortcut](shortcut-table.md) table for each shortcut.</span></span> <span data-ttu-id="b08ae-179">例如，此 [快捷方式](shortcut-table.md) 表可以針對安裝在 DirectoryFolder 目錄中的兩個快捷方式（Quick1 和 Quick2），包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="b08ae-179">For example, the [Shortcut](shortcut-table.md) table could contain the following information for two shortcuts, Quick1 and Quick2, installed into the DirectoryFolder directory.</span></span> <span data-ttu-id="b08ae-180">每個快捷方式都屬於目標欄位中指定的功能。</span><span class="sxs-lookup"><span data-stu-id="b08ae-180">Each shortcut belongs to the feature specified in the Target field.</span></span> <span data-ttu-id="b08ae-181">與快捷方式相關聯的圖示可以在圖示 \_ 欄位和 [圖示](icon-table.md) 表格中指定。</span><span class="sxs-lookup"><span data-stu-id="b08ae-181">The icon associated with the shortcut can be specified in the Icon\_ field and the [Icon](icon-table.md) table.</span></span>

    <span data-ttu-id="b08ae-182"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="b08ae-182">[Shortcut Table](shortcut-table.md) (partial)</span></span>

    

    | <span data-ttu-id="b08ae-183">快速鍵</span><span class="sxs-lookup"><span data-stu-id="b08ae-183">Shortcut</span></span> | <span data-ttu-id="b08ae-184">目錄\_</span><span class="sxs-lookup"><span data-stu-id="b08ae-184">Directory\_</span></span>   | <span data-ttu-id="b08ae-185">元件\_</span><span class="sxs-lookup"><span data-stu-id="b08ae-185">Component\_</span></span> | <span data-ttu-id="b08ae-186">目標</span><span class="sxs-lookup"><span data-stu-id="b08ae-186">Target</span></span>               | <span data-ttu-id="b08ae-187">圖示</span><span class="sxs-lookup"><span data-stu-id="b08ae-187">Icon</span></span>             |
    |----------|---------------|-------------|----------------------|------------------|
    | <span data-ttu-id="b08ae-188">Quick1</span><span class="sxs-lookup"><span data-stu-id="b08ae-188">Quick1</span></span>   | <span data-ttu-id="b08ae-189">DesktopFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-189">DesktopFolder</span></span> | <span data-ttu-id="b08ae-190">MSIMSG</span><span class="sxs-lookup"><span data-stu-id="b08ae-190">MSIMSG</span></span>      | <span data-ttu-id="b08ae-191">FeatureChild1 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b08ae-191">FeatureChild1\_Local</span></span> | <span data-ttu-id="b08ae-192">HelpFileIcon.exe</span><span class="sxs-lookup"><span data-stu-id="b08ae-192">HelpFileIcon.exe</span></span> |
    | <span data-ttu-id="b08ae-193">Quick2</span><span class="sxs-lookup"><span data-stu-id="b08ae-193">Quick2</span></span>   | <span data-ttu-id="b08ae-194">DesktopFolder</span><span class="sxs-lookup"><span data-stu-id="b08ae-194">DesktopFolder</span></span> | <span data-ttu-id="b08ae-195">MSIMSG</span><span class="sxs-lookup"><span data-stu-id="b08ae-195">MSIMSG</span></span>      | <span data-ttu-id="b08ae-196">FeatureChild1 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b08ae-196">FeatureChild1\_Local</span></span> | <span data-ttu-id="b08ae-197">HelpFileIcon.exe</span><span class="sxs-lookup"><span data-stu-id="b08ae-197">HelpFileIcon.exe</span></span> |

    

     

5.  <span data-ttu-id="b08ae-198">將資訊加入功能 [資料表](feature-table.md) 資料表中，該功能擁有的快捷方式屬於。</span><span class="sxs-lookup"><span data-stu-id="b08ae-198">Add information to the [Feature Table](feature-table.md) table for the feature owns shortcut belongs.</span></span> <span data-ttu-id="b08ae-199">當快捷方式啟動時，安裝程式會先確認所有屬於這項功能的元件都已安裝，然後才會啟動 \_ [快速鍵](shortcut-table.md) 表格之 component 資料行中所指定元件的金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="b08ae-199">When the shortcut is activated, the installer verifies that all the components belonging to this feature are installed before launching the key file of the component specified in the Component\_ column of the [Shortcut](shortcut-table.md) table.</span></span> <span data-ttu-id="b08ae-200">在此範例中，您可以將下列資訊加入至 FeatureParent1 本機功能的功能資料表資料表中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b08ae-200">In the case of this example, the following information can be added to the Feature Table table for the FeatureParent1\_Local feature.</span></span>

    <span data-ttu-id="b08ae-201">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="b08ae-201">[Feature Table](feature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="b08ae-202">功能</span><span class="sxs-lookup"><span data-stu-id="b08ae-202">Feature</span></span>               | <span data-ttu-id="b08ae-203">功能 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="b08ae-203">Feature\_Parent</span></span>       | <span data-ttu-id="b08ae-204">標題</span><span class="sxs-lookup"><span data-stu-id="b08ae-204">Title</span></span>                 | <span data-ttu-id="b08ae-205">屬性</span><span class="sxs-lookup"><span data-stu-id="b08ae-205">Attributes</span></span> |
    |-----------------------|-----------------------|-----------------------|------------|
    | <span data-ttu-id="b08ae-206">FeatureParent1 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b08ae-206">FeatureParent1\_Local</span></span> |                       | <span data-ttu-id="b08ae-207">FeatureParent1 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b08ae-207">FeatureParent1\_Local</span></span> | <span data-ttu-id="b08ae-208">16</span><span class="sxs-lookup"><span data-stu-id="b08ae-208">16</span></span>         |
    | <span data-ttu-id="b08ae-209">FeatureChild1 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b08ae-209">FeatureChild1\_Local</span></span>  | <span data-ttu-id="b08ae-210">FeatureParent1 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b08ae-210">FeatureParent1\_Local</span></span> | <span data-ttu-id="b08ae-211">FeatureParent1 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b08ae-211">FeatureParent1\_Local</span></span> | <span data-ttu-id="b08ae-212">0</span><span class="sxs-lookup"><span data-stu-id="b08ae-212">0</span></span>          |

    

     

6.  <span data-ttu-id="b08ae-213">針對每個新的快捷方式，將資源字串資訊加入至 [快捷方式資料表](shortcut-table.md)的 DisplayResourceDLL、DisplayResourceId、DescriptionResourceDLL 和 DescriptionResourceId 欄位中。</span><span class="sxs-lookup"><span data-stu-id="b08ae-213">For each new shortcut, add the resource string information to the DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL, and DescriptionResourceId fields of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="b08ae-214">DisplayResourceDLL 和 DescriptionResourceDLL 欄位包含 [格式化](formatted.md) 字串格式的資源字串。</span><span class="sxs-lookup"><span data-stu-id="b08ae-214">The DisplayResourceDLL and DescriptionResourceDLL fields contain the resource string in the [Formatted](formatted.md) string format.</span></span> <span data-ttu-id="b08ae-215">格式化的字串可以使用 \[ \#  \] [格式化](formatted.md)格式的 filekey 慣例。</span><span class="sxs-lookup"><span data-stu-id="b08ae-215">The formatted string can use the \[\#*filekey*\] convention of the [Formatted](formatted.md) format.</span></span> <span data-ttu-id="b08ae-216">在 [DisplayResourceId] 和 [DescriptionResourceId] 欄位中，加入資源字串的顯示和描述索引。</span><span class="sxs-lookup"><span data-stu-id="b08ae-216">Add the display and description indices for the resource strings in the DisplayResourceId and DescriptionResourceId fields.</span></span>

    <span data-ttu-id="b08ae-217"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="b08ae-217">[Shortcut Table](shortcut-table.md) (partial)</span></span>

    

    | <span data-ttu-id="b08ae-218">快速鍵</span><span class="sxs-lookup"><span data-stu-id="b08ae-218">Shortcut</span></span> | <span data-ttu-id="b08ae-219">DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="b08ae-219">DisplayResourceDLL</span></span> | <span data-ttu-id="b08ae-220">DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="b08ae-220">DisplayResourceId</span></span> | <span data-ttu-id="b08ae-221">DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="b08ae-221">DescriptionResourceDLL</span></span> | <span data-ttu-id="b08ae-222">DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="b08ae-222">DescriptionResourceId</span></span> |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | <span data-ttu-id="b08ae-223">Quick1</span><span class="sxs-lookup"><span data-stu-id="b08ae-223">Quick1</span></span>   | <span data-ttu-id="b08ae-224">\[\#msimsgdll\]</span><span class="sxs-lookup"><span data-stu-id="b08ae-224">\[\#msimsgdll\]</span></span>    | <span data-ttu-id="b08ae-225">36</span><span class="sxs-lookup"><span data-stu-id="b08ae-225">36</span></span>                | <span data-ttu-id="b08ae-226">\[\#msimsgdll\]</span><span class="sxs-lookup"><span data-stu-id="b08ae-226">\[\#msimsgdll\]</span></span>        | <span data-ttu-id="b08ae-227">37</span><span class="sxs-lookup"><span data-stu-id="b08ae-227">37</span></span>                    |
    | <span data-ttu-id="b08ae-228">Quick2</span><span class="sxs-lookup"><span data-stu-id="b08ae-228">Quick2</span></span>   | <span data-ttu-id="b08ae-229">\[\#msimsgdll\]</span><span class="sxs-lookup"><span data-stu-id="b08ae-229">\[\#msimsgdll\]</span></span>    | <span data-ttu-id="b08ae-230">38</span><span class="sxs-lookup"><span data-stu-id="b08ae-230">38</span></span>                | <span data-ttu-id="b08ae-231">\[\#msimsgdll\]</span><span class="sxs-lookup"><span data-stu-id="b08ae-231">\[\#msimsgdll\]</span></span>        | <span data-ttu-id="b08ae-232">39</span><span class="sxs-lookup"><span data-stu-id="b08ae-232">39</span></span>                    |

    

     

7.  <span data-ttu-id="b08ae-233">安裝封裝之後，請進行測試以確保多語系消費者介面如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="b08ae-233">After installing the package, test to ensure that the Multilingual User Interface is working as expected.</span></span>

 

 
