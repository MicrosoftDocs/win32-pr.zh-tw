---
description: 示範如何透過 System.AppUserModel.ID 屬性控制應用程式視窗的工作列群組行為。
title: 應用程式使用者模型識別碼視窗屬性範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973544"
---
# <a name="application-user-model-id-appid-window-property-sample"></a><span data-ttu-id="fc15b-103">應用程式使用者模型識別碼 (AppID) 視窗屬性範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-103">Application User Model ID (AppID) Window Property Sample</span></span>

<span data-ttu-id="fc15b-104">示範如何透過 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性控制應用程式視窗的工作列群組行為。</span><span class="sxs-lookup"><span data-stu-id="fc15b-104">Demonstrates how to control the taskbar grouping behavior of an application's windows through the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property.</span></span>

<span data-ttu-id="fc15b-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="fc15b-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fc15b-106">說明</span><span class="sxs-lookup"><span data-stu-id="fc15b-106">Description</span></span>](#description)
-   [<span data-ttu-id="fc15b-107">需求</span><span class="sxs-lookup"><span data-stu-id="fc15b-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="fc15b-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="fc15b-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="fc15b-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="fc15b-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc15b-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="fc15b-112">Description</span><span class="sxs-lookup"><span data-stu-id="fc15b-112">Description</span></span>

<span data-ttu-id="fc15b-113">這個範例會示範如何使用透過 [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)取得的視窗 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)實作為來設定 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="fc15b-113">This sample shows how to set the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property through the use of the window's [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, which is obtained through [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc15b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc15b-114">Requirements</span></span>



| <span data-ttu-id="fc15b-115">產品</span><span class="sxs-lookup"><span data-stu-id="fc15b-115">Product</span></span>                                | <span data-ttu-id="fc15b-116">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="fc15b-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="fc15b-117">Windows</span><span class="sxs-lookup"><span data-stu-id="fc15b-117">Windows</span></span>                                | <span data-ttu-id="fc15b-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc15b-118">Windows 7</span></span>               |
| <span data-ttu-id="fc15b-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="fc15b-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="fc15b-120">7.0</span><span class="sxs-lookup"><span data-stu-id="fc15b-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="fc15b-121">下載範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-121">Downloading the Sample</span></span>

| <span data-ttu-id="fc15b-122">Location</span><span class="sxs-lookup"><span data-stu-id="fc15b-122">Location</span></span>      | <span data-ttu-id="fc15b-123">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="fc15b-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc15b-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="fc15b-124">GitHub</span></span>  | [<span data-ttu-id="fc15b-125">AppUserModelIDWindowProperty 範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-125">AppUserModelIDWindowProperty sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a><span data-ttu-id="fc15b-126">建立範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-126">Building the Sample</span></span>

<span data-ttu-id="fc15b-127">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="fc15b-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="fc15b-128">開啟 [命令提示字元] 視窗，並流覽至 **AppUserModelIDWindowProperty** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="fc15b-128">Open the command prompt window and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="fc15b-129">輸入 `msbuild AppUserModelIDWindowProperty.sln`。</span><span class="sxs-lookup"><span data-stu-id="fc15b-129">Enter `msbuild AppUserModelIDWindowProperty.sln`.</span></span>

<span data-ttu-id="fc15b-130">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="fc15b-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="fc15b-131">開啟 Windows 檔案總管，然後流覽至 **AppUserModelIDWindowProperty** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="fc15b-131">Open Windows Explorer and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="fc15b-132">按兩下 AppUserModelIDWindowProperty .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="fc15b-132">Double-click the icon for the AppUserModelIDWindowProperty.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="fc15b-133">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="fc15b-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="fc15b-134">執行範例</span><span class="sxs-lookup"><span data-stu-id="fc15b-134">Running the Sample</span></span>

1.  <span data-ttu-id="fc15b-135">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="fc15b-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="fc15b-136">在命令列中，輸入 `AppUserModelIDWindowProperty.exe` 。</span><span class="sxs-lookup"><span data-stu-id="fc15b-136">At the command line, enter `AppUserModelIDWindowProperty.exe`.</span></span> <span data-ttu-id="fc15b-137">或者，從 Windows 檔案總管按兩下 AppUserModelIDWindowProperty.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="fc15b-137">Alternatively, from Windows Explorer double-click the icon for AppUserModelIDWindowProperty.exe.</span></span>
3.  <span data-ttu-id="fc15b-138">若要示範應用程式使用者模型識別碼的效果 (AppUserModelIDs) 在工作列群組上，請同時啟動至少三個應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="fc15b-138">To demonstrate the effect Application User Model IDs (AppUserModelIDs) have on taskbar grouping, launch at least three instances of the application at the same time.</span></span>
4.  <span data-ttu-id="fc15b-139">使用功能表在三個視窗中設定不同的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="fc15b-139">Use the menu to set a different AppUserModelID on each of the three windows.</span></span> <span data-ttu-id="fc15b-140">請注意，每個不同的 AppUserModelID 都會產生個別的工作列按鈕，而且 windows 可以在執行時間變更其身分識別。</span><span class="sxs-lookup"><span data-stu-id="fc15b-140">Notice that each separate AppUserModelID results in a separate taskbar button and that windows can change their identity at runtime.</span></span>
5.  <span data-ttu-id="fc15b-141">將至少兩個視窗設定為第二個 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="fc15b-141">Set at least two windows to the second AppUserModelID.</span></span> <span data-ttu-id="fc15b-142">請注意，它們都會移至相同的工作列群組。</span><span class="sxs-lookup"><span data-stu-id="fc15b-142">Notice that they both move into the same taskbar group.</span></span>
6.  <span data-ttu-id="fc15b-143">在工作列上按一下滑鼠右鍵，**然後在內容功能表中選取**[內容]，以開啟 [**工作列] 和 [開始] 功能表 [屬性**] 視窗。</span><span class="sxs-lookup"><span data-stu-id="fc15b-143">Open the **Taskbar and Start Menu Properties** window by right-clicking the taskbar and selecting **Properties** in the context menu.</span></span> <span data-ttu-id="fc15b-144">變更 **工作列按鈕：** [ **當工作列已滿時組合** ] 與 [ **永遠不合並** 值] 之間的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="fc15b-144">Change the **Taskbar buttons:** drop-down between the **Combine when taskbar is full** and **Never combine** values.</span></span> <span data-ttu-id="fc15b-145">請注意，每個視窗都可以取得個別的按鈕，但按鈕會依 AppUserModelID 分組。</span><span class="sxs-lookup"><span data-stu-id="fc15b-145">Notice that each window can get a separate button, but that the buttons are grouped by AppUserModelID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc15b-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc15b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc15b-147">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="fc15b-147">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
