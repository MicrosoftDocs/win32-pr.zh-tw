---
title: 安裝專案嚮導
description: 安裝專案嚮導
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player 線上商店、外掛程式
- 線上商店、外掛程式
- 類型2線上商店、外掛程式
- Windows Media Player 線上商店、外掛程式嚮導
- 線上商店、外掛程式嚮導
- 輸入2線上商店、外掛程式嚮導
- 專案嚮導 Windows Media Player 線上商店
- project wizard、線上商店
- 輸入2線上商店、專案嚮導
- Windows Media Player 線上商店，安裝外掛程式嚮導
- 線上商店，安裝外掛程式嚮導
- 輸入2個線上商店，安裝外掛程式 wizard
- Windows Media Player 線上商店，安裝專案嚮導
- 線上商店，安裝專案嚮導
- 輸入2個線上商店，安裝專案嚮導
- 外掛程式，Windows Media Player 線上商店
- 外掛程式，線上商店
- 外掛程式，輸入2個線上商店
- 外掛程式，安裝外掛程式 wizard
- 外掛程式、外掛程式嚮導
- 外掛程式，安裝專案嚮導
- 外掛程式，專案嚮導
- Windows Media Player 外掛程式，請輸入2個線上商店
- Windows Media Player 外掛程式，線上商店
- Windows Media Player 外掛程式，Windows Media Player 線上商店
- Windows Media Player 外掛程式，安裝外掛程式嚮導
- Windows Media Player 外掛程式，外掛程式嚮導
- Windows Media Player 外掛程式，安裝專案嚮導
- 專案嚮導 Windows Media Player 外掛程式
- 安裝外掛程式嚮導
- 外掛程式嚮導
- 安裝專案嚮導
- 專案嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674192"
---
# <a name="installing-the-project-wizard"></a><span data-ttu-id="1f500-136">安裝專案嚮導</span><span class="sxs-lookup"><span data-stu-id="1f500-136">Installing the Project Wizard</span></span>

<span data-ttu-id="1f500-137">若要設定開發環境以建立 type 2 online store 外掛程式，您必須安裝下列專案：</span><span class="sxs-lookup"><span data-stu-id="1f500-137">To set up your development environment for creating type 2 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="1f500-138">Microsoft Visual Studio .NET 2003 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1f500-138">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="1f500-139">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1f500-139">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="1f500-140">Windows SDK，其中包含 Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="1f500-140">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="1f500-141">線上商店外掛程式嚮導</span><span class="sxs-lookup"><span data-stu-id="1f500-141">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="1f500-142">安裝精靈</span><span class="sxs-lookup"><span data-stu-id="1f500-142">Installing the Wizard</span></span>

<span data-ttu-id="1f500-143">使用下列步驟，在 Visual Studio 中安裝線上商店外掛程式 wizard。</span><span class="sxs-lookup"><span data-stu-id="1f500-143">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="1f500-144">找出安裝 Windows SDK 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f500-144">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="1f500-145">展開資料夾以查看其子資料夾，並流覽至 [範例 \\ 多媒體 \\ WMP \\ 嚮導服務] \\ 。</span><span class="sxs-lookup"><span data-stu-id="1f500-145">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="1f500-146">找出下列三個檔案：</span><span class="sxs-lookup"><span data-stu-id="1f500-146">Locate the following three files:</span></span>
    -   <span data-ttu-id="1f500-147">wmpservices .vsz</span><span class="sxs-lookup"><span data-stu-id="1f500-147">wmpservices.vsz</span></span>
    -   <span data-ttu-id="1f500-148">wmpservices 的 vsdir</span><span class="sxs-lookup"><span data-stu-id="1f500-148">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="1f500-149">wmpservices .ico</span><span class="sxs-lookup"><span data-stu-id="1f500-149">wmpservices.ico</span></span>
3.  <span data-ttu-id="1f500-150">使用 [記事本] 之類的文字編輯器來編輯 wmpservices .vsz 檔。</span><span class="sxs-lookup"><span data-stu-id="1f500-150">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="1f500-151">尋找下列程式碼行：</span><span class="sxs-lookup"><span data-stu-id="1f500-151">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="1f500-152">`<VsWizardEngine version goes here>`根據您已安裝的 Visual Studio 版本，變更為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1f500-152">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="1f500-153">值</span><span class="sxs-lookup"><span data-stu-id="1f500-153">Value</span></span>              | <span data-ttu-id="1f500-154">Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="1f500-154">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="1f500-155">VsWizardEngine 7。1</span><span class="sxs-lookup"><span data-stu-id="1f500-155">VsWizardEngine.7.1</span></span> | <span data-ttu-id="1f500-156">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="1f500-156">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="1f500-157">VsWizardEngine 8。0</span><span class="sxs-lookup"><span data-stu-id="1f500-157">VsWizardEngine.8.0</span></span> | <span data-ttu-id="1f500-158">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="1f500-158">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="1f500-159">VsWizardEngine 9。0</span><span class="sxs-lookup"><span data-stu-id="1f500-159">VsWizardEngine.9.0</span></span> | <span data-ttu-id="1f500-160">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="1f500-160">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="1f500-161">尋找下列程式碼行：</span><span class="sxs-lookup"><span data-stu-id="1f500-161">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="1f500-162">切換 `<path to wmpservices directory goes here>` 至 wizard 檔案所在的路徑。</span><span class="sxs-lookup"><span data-stu-id="1f500-162">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="1f500-163">例如，假設您有 Visual Studio 2008，而您的 wizard 檔案位於這裡： C： \\ Program files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ 範例 \\ 多媒體 \\ WMP \\ 的 \\ 服務。</span><span class="sxs-lookup"><span data-stu-id="1f500-163">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="1f500-164">然後您的 wmpservices .vsz 檔案看起來會像這樣：</span><span class="sxs-lookup"><span data-stu-id="1f500-164">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="1f500-165">找出安裝 Visual Studio 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f500-165">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="1f500-166">展開資料夾以查看其子資料夾，並尋找名為 vcprojects 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f500-166">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="1f500-167">將步驟2中列出的三個檔案複製到 vcprojects 資料夾。</span><span class="sxs-lookup"><span data-stu-id="1f500-167">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="1f500-168">現在已安裝精靈。</span><span class="sxs-lookup"><span data-stu-id="1f500-168">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f500-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f500-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f500-170">**建立 Type 2 線上商店的外掛程式**</span><span class="sxs-lookup"><span data-stu-id="1f500-170">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




