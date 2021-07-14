---
title: 資源庫範例
description: 這個程式碼範例會示範使用 Windows 功能區架構中包含的不同資源庫控制項類型所需的標記和程式碼。
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691747"
---
# <a name="gallery-sample"></a><span data-ttu-id="0ea0f-103">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="0ea0f-103">Gallery Sample</span></span>

<span data-ttu-id="0ea0f-104">這個程式碼範例會示範使用 Windows 功能區架構中包含的不同資源庫控制項類型所需的標記和程式碼。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="0ea0f-105">此範例包含的程式碼可以用來以動態方式將專案填入至資源庫，以及處理可支援結果導向 UI 的特殊資源庫預覽事件。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

- [<span data-ttu-id="0ea0f-106">使用量</span><span class="sxs-lookup"><span data-stu-id="0ea0f-106">Usage</span></span>](#usage)
  - [<span data-ttu-id="0ea0f-107">建立範例</span><span class="sxs-lookup"><span data-stu-id="0ea0f-107">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="0ea0f-108">執行範例</span><span class="sxs-lookup"><span data-stu-id="0ea0f-108">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="0ea0f-109">支援</span><span class="sxs-lookup"><span data-stu-id="0ea0f-109">Support</span></span>](#support)
- [<span data-ttu-id="0ea0f-110">最低需求</span><span class="sxs-lookup"><span data-stu-id="0ea0f-110">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="0ea0f-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ea0f-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="0ea0f-112">使用方式</span><span class="sxs-lookup"><span data-stu-id="0ea0f-112">Usage</span></span>

<span data-ttu-id="0ea0f-113">您可以從[Microsoft 下載中心](https://www.microsoft.com/download/details.aspx?id=9620)以獨立 Microsoft Visual Studio 專案形式下載 Windows 功能區架構範例，或將其安裝為[Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/sdk-archive/)的一部分。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-113">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="0ea0f-114">Windows軟體發展工具組 (SDK)  (標準安裝路徑) ：% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ WindowsRibbon 資源 \\ 庫</span><span class="sxs-lookup"><span data-stu-id="0ea0f-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="0ea0f-115">建立範例</span><span class="sxs-lookup"><span data-stu-id="0ea0f-115">Building the Sample</span></span>

<span data-ttu-id="0ea0f-116">下載範例。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-116">Download the sample.</span></span>

<span data-ttu-id="0ea0f-117">安裝 Windows 7 的 Windows SDK，然後開啟其 [組建環境命令] 視窗。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="0ea0f-118">在 [開始] 功能表中，指向 [所有程式]、[Microsoft Windows SDK]，然後按一下 CMD 殼層。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="0ea0f-119">若要組建建置環境命令視窗的範例，您必須先移至範例的來源目錄</span><span class="sxs-lookup"><span data-stu-id="0ea0f-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="0ea0f-120">在命令提示字元中，輸入 MSBUILD。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="0ea0f-121">若要在 Microsoft Visual Studio 中建置範例，請載入範例方案或專案檔，然後按下 CTRL+SHIFT+B。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="0ea0f-122">執行範例</span><span class="sxs-lookup"><span data-stu-id="0ea0f-122">Running the Sample</span></span>

<span data-ttu-id="0ea0f-123">若要從 [建立環境] 命令視窗執行範例，請執行 \\ 範例源資料夾所包含的 bin Debug 或 bin 發行資料夾中的 .exe 檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="0ea0f-124">若要在 Visual Studio 中執行編譯後的範例並進行偵錯，請按 F5。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="0ea0f-125">支援</span><span class="sxs-lookup"><span data-stu-id="0ea0f-125">Support</span></span>

<span data-ttu-id="0ea0f-126">[Windows 功能區開發論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment)可討論主題，並詢問與開發 Windows 功能區應用程式相關的問題。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="0ea0f-127">最低需求</span><span class="sxs-lookup"><span data-stu-id="0ea0f-127">Minimum Requirements</span></span>



| <span data-ttu-id="0ea0f-128">需求</span><span class="sxs-lookup"><span data-stu-id="0ea0f-128">Requirement</span></span> | <span data-ttu-id="0ea0f-129">值</span><span class="sxs-lookup"><span data-stu-id="0ea0f-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea0f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ea0f-130">Minimum supported client</span></span> | <span data-ttu-id="0ea0f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0ea0f-131">Windows 7</span></span><br/> <span data-ttu-id="0ea0f-132">Windowsvista Service Pack 2 (SP2) 和[適用于 Windows Vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea0f-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="0ea0f-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ea0f-133">Minimum supported server</span></span> | <span data-ttu-id="0ea0f-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0ea0f-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="0ea0f-135">Windowsserver 2008 SP2 和[Windows server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea0f-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="0ea0f-136">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0ea0f-136">Windows SDK</span></span>              | <span data-ttu-id="0ea0f-137">7.0</span><span class="sxs-lookup"><span data-stu-id="0ea0f-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="0ea0f-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0ea0f-138">Visual Studio</span></span>            | <span data-ttu-id="0ea0f-139">2008</span><span class="sxs-lookup"><span data-stu-id="0ea0f-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="0ea0f-140">標頭檔和 IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="0ea0f-140">Header and IDL files</span></span>     | <span data-ttu-id="0ea0f-141">uiribbon .h、uiribbon .idl</span><span class="sxs-lookup"><span data-stu-id="0ea0f-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="0ea0f-142">適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)的 Windows Vista 和 platform update 的[平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)是一組執行時間程式庫，可讓開發人員將 Windows 功能區應用程式的目標設為 Windows Vista 和 Windows 伺服器2008。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0ea0f-143">所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得平臺更新。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="0ea0f-144">需要適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)或平臺更新的協力廠商應用程式，可以讓 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。</span><span class="sxs-lookup"><span data-stu-id="0ea0f-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0ea0f-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ea0f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ea0f-146">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="0ea0f-146">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="0ea0f-147">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="0ea0f-147">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="0ea0f-148">下拉式圖庫</span><span class="sxs-lookup"><span data-stu-id="0ea0f-148">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="0ea0f-149">功能區中的資源庫</span><span class="sxs-lookup"><span data-stu-id="0ea0f-149">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="0ea0f-150">分割按鈕資源庫</span><span class="sxs-lookup"><span data-stu-id="0ea0f-150">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="0ea0f-151">集合屬性</span><span class="sxs-lookup"><span data-stu-id="0ea0f-151">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





