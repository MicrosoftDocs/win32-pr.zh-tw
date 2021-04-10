---
title: 使用 Visual Studio 編譯範例應用程式
description: 使用 Visual Studio 編譯範例應用程式
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- 桌面應用程式、範例
- Windows Media 裝置管理員，桌面應用程式範例
- 裝置管理員，桌面應用程式範例
- 範例，桌面應用程式
- 範例，使用 Visual Studio 編譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021218"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a><span data-ttu-id="86f25-110">使用 Visual Studio 編譯範例應用程式</span><span class="sxs-lookup"><span data-stu-id="86f25-110">Compiling the Sample Application Using Visual Studio</span></span>

<span data-ttu-id="86f25-111">Windows Media 裝置管理員 SDK 包含與 Microsoft Visual Studio 2005 相容的 Visual Studio 解決方案。</span><span class="sxs-lookup"><span data-stu-id="86f25-111">The Windows Media Device Manager SDK includes a Visual Studio solution that is compatible with Microsoft Visual Studio 2005.</span></span>

<span data-ttu-id="86f25-112">在編譯範例應用程式之前，您必須將標頭檔 shtypes.idl 重新命名，以避免與 Microsoft Platform SDK 中的相同名稱的檔案發生衝突。</span><span class="sxs-lookup"><span data-stu-id="86f25-112">Before you compile the sample application, you must rename the header file shtypes.h to prevent conflicts with a file of the same name that is found in the Microsoft Platform SDK.</span></span> <span data-ttu-id="86f25-113">例如，您可以重新命名 <*sdk 安裝路徑* > \\ WMFSDK11 \\ 包含 \\ shtypes.idl，以 <*SDK 安裝路徑* > \\ WMFSDK11 \\ 包括 \\ shtypes.idl.. h. 備份。</span><span class="sxs-lookup"><span data-stu-id="86f25-113">For example, you could rename <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h to <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h.backup.</span></span>

<span data-ttu-id="86f25-114">若要建立應用程式，請啟動 Visual Studio 2005 的實例、開啟方案檔 wmdmapp .sln （位於資料夾 <*SDK 安裝路徑* > \\ WMFSDK11 apps wmdmapp 中）， \\ \\ 然後選擇 [**組建/組建] 方案** 選項。</span><span class="sxs-lookup"><span data-stu-id="86f25-114">To build the application, start an instance of Visual Studio 2005, open the solution file, wmdmapp.sln, which is found in the folder <*SDK installation path*>\\WMFSDK11\\apps\\wmdmapp and choose the **Build/Build Solution** option.</span></span> <span data-ttu-id="86f25-115">這會建立兩個專案檔： helper 專案、proghelp vcproj，以及主要應用程式 wmdmapp。 vcproj。</span><span class="sxs-lookup"><span data-stu-id="86f25-115">This will create two project files: the helper project, proghelp.vcproj, as well as the main application wmdmapp.vcproj.</span></span> <span data-ttu-id="86f25-116">此外，它還會建立進度協助程式 DLL 和主應用程式 (WMDMApp.exe) 。</span><span class="sxs-lookup"><span data-stu-id="86f25-116">In addition, it will create the progress helper DLL and the main application (WMDMApp.exe).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86f25-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="86f25-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f25-118">**桌面應用程式範例**</span><span class="sxs-lookup"><span data-stu-id="86f25-118">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




