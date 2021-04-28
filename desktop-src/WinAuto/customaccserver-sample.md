---
title: CustomAccServer 範例
description: CustomAccServer 範例
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088006"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="fa2bf-103">CustomAccServer 範例</span><span class="sxs-lookup"><span data-stu-id="fa2bf-103">CustomAccServer Sample</span></span>

<span data-ttu-id="fa2bf-104">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fa2bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa2bf-105">Description</span></span>](#description)
-   [<span data-ttu-id="fa2bf-106">下載資訊</span><span class="sxs-lookup"><span data-stu-id="fa2bf-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="fa2bf-107">最低需求</span><span class="sxs-lookup"><span data-stu-id="fa2bf-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="fa2bf-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="fa2bf-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="fa2bf-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="fa2bf-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="fa2bf-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa2bf-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="fa2bf-111">Description</span><span class="sxs-lookup"><span data-stu-id="fa2bf-111">Description</span></span>

<span data-ttu-id="fa2bf-112">這個範例示範如何針對簡單自訂控制項來執行 Microsoft Active Accessibility server。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="fa2bf-113">控制項的可存取物件包含 (清單方塊) 的根項目，以及 (清單專案的子系。 ) </span><span class="sxs-lookup"><span data-stu-id="fa2bf-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="fa2bf-114">下載資訊</span><span class="sxs-lookup"><span data-stu-id="fa2bf-114">Download Information</span></span>

<span data-ttu-id="fa2bf-115">CustomAccServer 範例會安裝為 [Microsoft Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx) 的一部分，並可在下列位置中取得。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="fa2bf-116">Location</span><span class="sxs-lookup"><span data-stu-id="fa2bf-116">Location</span></span>    | <span data-ttu-id="fa2bf-117">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="fa2bf-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2bf-118">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="fa2bf-118">Windows SDK</span></span> | <span data-ttu-id="fa2bf-119">% Program Files% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ msaa</span><span class="sxs-lookup"><span data-stu-id="fa2bf-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="fa2bf-120">最低需求</span><span class="sxs-lookup"><span data-stu-id="fa2bf-120">Minimum Requirements</span></span>



| <span data-ttu-id="fa2bf-121">產品</span><span class="sxs-lookup"><span data-stu-id="fa2bf-121">Product</span></span>          | <span data-ttu-id="fa2bf-122">版本</span><span class="sxs-lookup"><span data-stu-id="fa2bf-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="fa2bf-123">作業系統</span><span class="sxs-lookup"><span data-stu-id="fa2bf-123">Operating System</span></span> | <span data-ttu-id="fa2bf-124">Windows XP、Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa2bf-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="fa2bf-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="fa2bf-125">Windows SDK</span></span>      | <span data-ttu-id="fa2bf-126">7.0</span><span class="sxs-lookup"><span data-stu-id="fa2bf-126">7.0</span></span>                             |
| <span data-ttu-id="fa2bf-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fa2bf-127">Visual Studio</span></span>    | <span data-ttu-id="fa2bf-128">2008</span><span class="sxs-lookup"><span data-stu-id="fa2bf-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="fa2bf-129">建立範例</span><span class="sxs-lookup"><span data-stu-id="fa2bf-129">Building the Sample</span></span>

<span data-ttu-id="fa2bf-130">若要使用 Visual Studio 2008 建立範例：</span><span class="sxs-lookup"><span data-stu-id="fa2bf-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="fa2bf-131">執行 SDK 隨附的 Microsoft Windows 軟體開發套件 (SDK) 設定工具，以將 SDK include 目錄新增至 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="fa2bf-132">開啟 Windows 檔案總管並流覽至專案目錄。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="fa2bf-133">按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="fa2bf-134">在 [ **組建** ] 功能表上，選取 [ **建立方案** ] 來建立方案。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="fa2bf-135">應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="fa2bf-136">若要從命令列建立範例，請參閱下列位置的 Windows SDK 版本資訊中建立範例：% Program Files% \\ Microsoft sdk \\ Windows \\ 7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="fa2bf-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="fa2bf-137">執行範例</span><span class="sxs-lookup"><span data-stu-id="fa2bf-137">Running the Sample</span></span>

<span data-ttu-id="fa2bf-138">若要執行範例：</span><span class="sxs-lookup"><span data-stu-id="fa2bf-138">To run the sample:</span></span>

1.  <span data-ttu-id="fa2bf-139">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="fa2bf-140">在命令列中輸入 AccServer.exe，或按兩下 AccServer.exe 的圖示，從 Windows 檔案總管啟動它。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="fa2bf-141">若要從 Visual Studio 執行，請按 F5 或按一下 [**調試**] 功能表中的 [**開始調試**]。</span><span class="sxs-lookup"><span data-stu-id="fa2bf-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa2bf-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa2bf-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa2bf-143">範例</span><span class="sxs-lookup"><span data-stu-id="fa2bf-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




