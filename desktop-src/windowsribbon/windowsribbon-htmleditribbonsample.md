---
title: HTMLEditRibbon 範例
description: 這個程式碼範例會示範將現有的 Microsoft Foundation 類別 (MFC) 應用程式，以使用 Windows 功能區所需的標記和程式碼。
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024809"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="1908c-103">HTMLEditRibbon 範例</span><span class="sxs-lookup"><span data-stu-id="1908c-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="1908c-104">這個程式碼範例會示範將現有的 Microsoft Foundation 類別 (MFC) 應用程式，以使用 Windows 功能區所需的標記和程式碼。</span><span class="sxs-lookup"><span data-stu-id="1908c-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="1908c-105">其建立方式是取得現有的 MFC HTMLEdit 範例應用程式，並修改其程式碼和資源以使用 Windows 功能區。</span><span class="sxs-lookup"><span data-stu-id="1908c-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

-   [<span data-ttu-id="1908c-106">備註</span><span class="sxs-lookup"><span data-stu-id="1908c-106">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="1908c-107">使用量</span><span class="sxs-lookup"><span data-stu-id="1908c-107">Usage</span></span>](#usage)
    -   [<span data-ttu-id="1908c-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="1908c-108">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="1908c-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="1908c-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="1908c-110">支援</span><span class="sxs-lookup"><span data-stu-id="1908c-110">Support</span></span>](#support)
-   [<span data-ttu-id="1908c-111">最低需求</span><span class="sxs-lookup"><span data-stu-id="1908c-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="1908c-112">備註</span><span class="sxs-lookup"><span data-stu-id="1908c-112">Remarks</span></span>

<span data-ttu-id="1908c-113">針對 MFC 範例，請參閱 [HTMLEdit 範例：包裝 INTERNET EXPLORER MSHTML 編輯控制項](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx)。</span><span class="sxs-lookup"><span data-stu-id="1908c-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="1908c-114">使用方式</span><span class="sxs-lookup"><span data-stu-id="1908c-114">Usage</span></span>

<span data-ttu-id="1908c-115">HTMLEditRibbon 範例可從 [Microsoft 下載中心](https://www.microsoft.com/DOWNLOADS/en/default.aspx) 下載為獨立 Microsoft Visual Studio 專案，或安裝為 [Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx)的一部分。</span><span class="sxs-lookup"><span data-stu-id="1908c-115">The HTMLEditRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="1908c-116">Microsoft 下載中心： [Windows 功能區範例](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="1908c-116">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="1908c-117">Windows 軟體開發套件 (SDK)  (標準安裝路徑) ：% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="1908c-117">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="1908c-118">建立範例</span><span class="sxs-lookup"><span data-stu-id="1908c-118">Building the Sample</span></span>

<span data-ttu-id="1908c-119">將範例下載至您的硬碟。</span><span class="sxs-lookup"><span data-stu-id="1908c-119">Download the sample to your hard disk.</span></span>

<span data-ttu-id="1908c-120">安裝適用于 Windows 7 的 Windows SDK，然後開啟其 [組建環境命令] 視窗。</span><span class="sxs-lookup"><span data-stu-id="1908c-120">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="1908c-121">在 [開始] 功能表中，指向 [所有程式]、[Microsoft Windows SDK]，然後按一下 CMD 殼層。</span><span class="sxs-lookup"><span data-stu-id="1908c-121">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="1908c-122">若要組建建置環境命令視窗的範例，您必須先移至範例的來源目錄</span><span class="sxs-lookup"><span data-stu-id="1908c-122">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="1908c-123">在命令提示字元中，輸入 MSBUILD。</span><span class="sxs-lookup"><span data-stu-id="1908c-123">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="1908c-124">若要在 Microsoft Visual Studio 中建置範例，請載入範例方案或專案檔，然後按下 CTRL+SHIFT+B。</span><span class="sxs-lookup"><span data-stu-id="1908c-124">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="1908c-125">執行範例</span><span class="sxs-lookup"><span data-stu-id="1908c-125">Running the Sample</span></span>

<span data-ttu-id="1908c-126">若要從 [組建環境] 命令視窗執行範例，請執行 \\ 範例源資料夾所包含的 bin Debug 或 bin 發行資料夾中的 .exe 檔案。 \\</span><span class="sxs-lookup"><span data-stu-id="1908c-126">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="1908c-127">若要在 Visual Studio 中執行編譯後的範例並進行偵錯，請按 F5。</span><span class="sxs-lookup"><span data-stu-id="1908c-127">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="1908c-128">支援</span><span class="sxs-lookup"><span data-stu-id="1908c-128">Support</span></span>

<span data-ttu-id="1908c-129">[Windows 功能區開發論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment)可以討論主題，並詢問與開發 Windows 功能區應用程式相關的問題。</span><span class="sxs-lookup"><span data-stu-id="1908c-129">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="1908c-130">最低需求</span><span class="sxs-lookup"><span data-stu-id="1908c-130">Minimum Requirements</span></span>



| <span data-ttu-id="1908c-131">需求</span><span class="sxs-lookup"><span data-stu-id="1908c-131">Requirement</span></span> | <span data-ttu-id="1908c-132">值</span><span class="sxs-lookup"><span data-stu-id="1908c-132">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1908c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1908c-133">Minimum supported client</span></span> | <span data-ttu-id="1908c-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1908c-134">Windows 7</span></span><br/> <span data-ttu-id="1908c-135">Windows Vista Service Pack 2 (SP2) 和 [Windows vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="1908c-135">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="1908c-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1908c-136">Minimum supported server</span></span> | <span data-ttu-id="1908c-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1908c-137">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="1908c-138">Windows server 2008 SP2 和 [Windows server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="1908c-138">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="1908c-139">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1908c-139">Windows SDK</span></span>              | <span data-ttu-id="1908c-140">7.0</span><span class="sxs-lookup"><span data-stu-id="1908c-140">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="1908c-141">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1908c-141">Visual Studio</span></span>            | <span data-ttu-id="1908c-142">2008</span><span class="sxs-lookup"><span data-stu-id="1908c-142">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="1908c-143">標頭檔和 IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="1908c-143">Header and IDL files</span></span>     | <span data-ttu-id="1908c-144">uiribbon .h、uiribbon .idl</span><span class="sxs-lookup"><span data-stu-id="1908c-144">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="1908c-145">Windows [vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 和 [windows Server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 是一組執行時間程式庫，可讓開發人員將 windows 功能區應用程式的目標設為 Windows vista 和 windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="1908c-145">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="1908c-146">所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得平臺更新。</span><span class="sxs-lookup"><span data-stu-id="1908c-146">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="1908c-147">需要 [適用于 Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) 或 [Windows Server 2008 平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 的協力廠商應用程式，可以 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。</span><span class="sxs-lookup"><span data-stu-id="1908c-147">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





