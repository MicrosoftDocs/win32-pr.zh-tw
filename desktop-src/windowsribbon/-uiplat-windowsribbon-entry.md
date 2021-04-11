---
title: Windows 功能區架構
description: Windows 功能區架構是一種豐富的命令呈現系統，提供了傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的新式替代方案。
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows 功能區
- 功能區
- Windows 功能區檔
- 功能區檔
- Windows 功能區 API
- 功能區 API
- Windows 功能區，架構
- 功能區，架構
- Windows 功能區，關於
- 功能區，關於
- Windows 功能區，元件
- 功能區、元件
- Windows 功能區，views
- 功能區、視圖
- Windows 功能區，架構
- 功能區，架構
- Windows 功能區，Api
- 功能區，Api
- Windows 功能區，安全性
- 功能區，安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6906401573cb244ddc4386faf8c283d7938a0ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934223"
---
# <a name="windows-ribbon-framework"></a><span data-ttu-id="8de36-123">Windows 功能區架構</span><span class="sxs-lookup"><span data-stu-id="8de36-123">Windows Ribbon Framework</span></span>

<span data-ttu-id="8de36-124">Windows 功能區架構是一種豐富的命令呈現系統，提供了傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的新式替代方案。</span><span class="sxs-lookup"><span data-stu-id="8de36-124">The Windows Ribbon framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span> <span data-ttu-id="8de36-125">類似于 Microsoft Office 2007 流暢的使用者介面的功能和外觀，功能區架構是由功能區命令列所組成，可透過應用程式視窗頂端的一系列索引標籤來公開應用程式的主要功能，以及內容功能表系統。</span><span class="sxs-lookup"><span data-stu-id="8de36-125">Similar in functionality and appearance to the Microsoft Office 2007 Fluent user interface, the Ribbon framework is composed of a ribbon command bar that exposes the major features of an application through a series of tabs at the top of an application window, and a context menu system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8de36-126">本節內容</span><span class="sxs-lookup"><span data-stu-id="8de36-126">In this section</span></span>



| <span data-ttu-id="8de36-127">主題</span><span class="sxs-lookup"><span data-stu-id="8de36-127">Topic</span></span>                                                                           | <span data-ttu-id="8de36-128">描述</span><span class="sxs-lookup"><span data-stu-id="8de36-128">Description</span></span>                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8de36-129">功能區架構概述</span><span class="sxs-lookup"><span data-stu-id="8de36-129">Ribbon Framework Overviews</span></span>](windowsribbon-overviews-entry.md)<br/>      | <span data-ttu-id="8de36-130">本節所包含的主題將探索功能區架構的基本概念。</span><span class="sxs-lookup"><span data-stu-id="8de36-130">The topics contained in this section explore the fundamentals of the Ribbon framework.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="8de36-131">功能區架構開發人員指南</span><span class="sxs-lookup"><span data-stu-id="8de36-131">Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)<br/>  | <span data-ttu-id="8de36-132">本節所包含的主題將說明 Windows 功能區架構的特定層面。</span><span class="sxs-lookup"><span data-stu-id="8de36-132">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span> <br/>                                                                                                          |
| [<span data-ttu-id="8de36-133">功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="8de36-133">Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)<br/> | <span data-ttu-id="8de36-134">本章節包含的主題說明功能區架構所包含的控制項集合。</span><span class="sxs-lookup"><span data-stu-id="8de36-134">The topics contained in this section describe the set of controls that are included with the Ribbon framework.</span></span> <span data-ttu-id="8de36-135">此處所列的控制項是功能區中公開命令功能的 UI 物件。</span><span class="sxs-lookup"><span data-stu-id="8de36-135">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span><br/> |
| [<span data-ttu-id="8de36-136">功能區架構參考</span><span class="sxs-lookup"><span data-stu-id="8de36-136">Ribbon Framework Reference</span></span>](windowsribbon-reference-entry.md)<br/>      | <span data-ttu-id="8de36-137">本節所包含的主題會提供功能區架構的參考規格。</span><span class="sxs-lookup"><span data-stu-id="8de36-137">The topics contained in this section provide the Reference specifications for the Ribbon framework.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="8de36-138">功能區架構範例</span><span class="sxs-lookup"><span data-stu-id="8de36-138">Ribbon Framework Samples</span></span>](windowsribbon-samples-entry.md)<br/>          | <span data-ttu-id="8de36-139">本節所包含的主題會提供支援 Windows 功能區架構檔的程式碼範例詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8de36-139">The topics contained in this section provide details about the code samples that support the Windows Ribbon framework documentation.</span></span> <br/>                                                                     |
| [<span data-ttu-id="8de36-140">功能區架構詞彙</span><span class="sxs-lookup"><span data-stu-id="8de36-140">Ribbon Framework Glossary</span></span>](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a><span data-ttu-id="8de36-141">開發人員讀者</span><span class="sxs-lookup"><span data-stu-id="8de36-141">Developer Audience</span></span>

<span data-ttu-id="8de36-142">Windows 功能區架構是設計來供 C/c + + 開發人員和 UI 設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="8de36-142">The Windows Ribbon framework is designed for use by C/C++ developers and UI designers.</span></span>

<span data-ttu-id="8de36-143">建議的 proficiencies：</span><span class="sxs-lookup"><span data-stu-id="8de36-143">Recommended proficiencies:</span></span>

-   <span data-ttu-id="8de36-144">COM 程式設計</span><span class="sxs-lookup"><span data-stu-id="8de36-144">COM programming</span></span>
-   <span data-ttu-id="8de36-145">Windows API 程式設計</span><span class="sxs-lookup"><span data-stu-id="8de36-145">Windows API programming</span></span>
-   <span data-ttu-id="8de36-146">XML/XAML 程式設計</span><span class="sxs-lookup"><span data-stu-id="8de36-146">XML/XAML programming</span></span>

<span data-ttu-id="8de36-147">建議的基本知識：</span><span class="sxs-lookup"><span data-stu-id="8de36-147">Recommended foundational knowledge:</span></span>

-   <span data-ttu-id="8de36-148">UI 程式設計概念</span><span class="sxs-lookup"><span data-stu-id="8de36-148">UI programming concepts</span></span>
-   <span data-ttu-id="8de36-149">一般 UI 概念</span><span class="sxs-lookup"><span data-stu-id="8de36-149">General UI concepts</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="8de36-150">最低需求</span><span class="sxs-lookup"><span data-stu-id="8de36-150">Minimum Requirements</span></span>



| <span data-ttu-id="8de36-151">需求</span><span class="sxs-lookup"><span data-stu-id="8de36-151">Requirement</span></span> | <span data-ttu-id="8de36-152">值</span><span class="sxs-lookup"><span data-stu-id="8de36-152">Value</span></span> |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de36-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8de36-153">Minimum supported client</span></span>               | <span data-ttu-id="8de36-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8de36-154">Windows 7</span></span><br/> <span data-ttu-id="8de36-155">Windows Vista Service Pack 2 (SP2) 和 [Windows vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="8de36-155">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="8de36-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8de36-156">Minimum supported server</span></span>               | <span data-ttu-id="8de36-157">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8de36-157">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="8de36-158">Windows server 2008 SP2 和 [Windows server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="8de36-158">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="8de36-159">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="8de36-159">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="8de36-160">7.0</span><span class="sxs-lookup"><span data-stu-id="8de36-160">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="8de36-161">標頭檔和 IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="8de36-161">Header and IDL files</span></span>                   | <span data-ttu-id="8de36-162">uiribbon .h、uiribbon .idl</span><span class="sxs-lookup"><span data-stu-id="8de36-162">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="8de36-163">Windows [vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 和 [windows Server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 是一組執行時間程式庫，可讓開發人員將 windows 功能區應用程式的目標設為 Windows vista 和 windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="8de36-163">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8de36-164">所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得平臺更新。</span><span class="sxs-lookup"><span data-stu-id="8de36-164">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="8de36-165">需要 [適用于 Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) 或 [Windows Server 2008 平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 的協力廠商應用程式，可以 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。</span><span class="sxs-lookup"><span data-stu-id="8de36-165">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8de36-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8de36-166">See Also</span></span>

[<span data-ttu-id="8de36-167">元件物件模型 (COM)</span><span class="sxs-lookup"><span data-stu-id="8de36-167">Component Object Model (COM)</span></span>](../com/component-object-model--com--portal.md)


<span data-ttu-id="8de36-168">[Windows 應用程式開發介面](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8de36-168">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>


[<span data-ttu-id="8de36-169">XAML</span><span class="sxs-lookup"><span data-stu-id="8de36-169">XAML</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

