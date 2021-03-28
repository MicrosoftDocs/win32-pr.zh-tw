---
description: 示範如何撰寫用來在 Windows 檔案總管預覽窗格或其他預覽處理常式主機內顯示檔案預覽的處理常式。
title: 配方預覽處理常式範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973496"
---
# <a name="recipe-preview-handler-sample"></a><span data-ttu-id="56371-103">配方預覽處理常式範例</span><span class="sxs-lookup"><span data-stu-id="56371-103">Recipe Preview Handler Sample</span></span>

<span data-ttu-id="56371-104">示範如何撰寫用來在 Windows 檔案總管預覽窗格或其他預覽處理常式主機內顯示檔案預覽的處理常式。</span><span class="sxs-lookup"><span data-stu-id="56371-104">Demonstrates how to write a handler used to display a file preview inside the Windows Explorer preview pane or other preview handler hosts.</span></span>

<span data-ttu-id="56371-105">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="56371-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="56371-106">需求</span><span class="sxs-lookup"><span data-stu-id="56371-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="56371-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="56371-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="56371-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="56371-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="56371-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="56371-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="56371-110">取消註冊範例預覽處理常式 DLL</span><span class="sxs-lookup"><span data-stu-id="56371-110">Unregistering the Sample Preview Handler DLL</span></span>](#unregistering-the-sample-preview-handler-dll)
-   [<span data-ttu-id="56371-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="56371-111">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="56371-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="56371-112">Requirements</span></span>



| <span data-ttu-id="56371-113">產品</span><span class="sxs-lookup"><span data-stu-id="56371-113">Product</span></span>                                | <span data-ttu-id="56371-114">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="56371-114">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="56371-115">Windows</span><span class="sxs-lookup"><span data-stu-id="56371-115">Windows</span></span>                                | <span data-ttu-id="56371-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56371-116">Windows Vista</span></span>           |
| <span data-ttu-id="56371-117">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="56371-117">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="56371-118">7.0</span><span class="sxs-lookup"><span data-stu-id="56371-118">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="56371-119">下載範例</span><span class="sxs-lookup"><span data-stu-id="56371-119">Downloading the Sample</span></span>

| <span data-ttu-id="56371-120">Location</span><span class="sxs-lookup"><span data-stu-id="56371-120">Location</span></span>      | <span data-ttu-id="56371-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="56371-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56371-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="56371-122">GitHub</span></span>  | [<span data-ttu-id="56371-123">RecipePreviewHandler 範例</span><span class="sxs-lookup"><span data-stu-id="56371-123">RecipePreviewHandler sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a><span data-ttu-id="56371-124">建立範例</span><span class="sxs-lookup"><span data-stu-id="56371-124">Building the Sample</span></span>

<span data-ttu-id="56371-125">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="56371-125">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="56371-126">開啟 [命令提示字元] 視窗，並流覽至 **RecipePreviewHandler** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="56371-126">Open the command prompt window and navigate to the **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="56371-127">例如： `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler` 。</span><span class="sxs-lookup"><span data-stu-id="56371-127">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span></span>
2.  <span data-ttu-id="56371-128">輸入 `msbuild PreviewHandlerSDKSample.sln`。</span><span class="sxs-lookup"><span data-stu-id="56371-128">Enter `msbuild PreviewHandlerSDKSample.sln`.</span></span>

<span data-ttu-id="56371-129">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="56371-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="56371-130">開啟 Windows 檔案總管，然後流覽至 **RecipePreviewHandler** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="56371-130">Open Windows Explorer and navigate to the **RecipePreviewHandler** project directory.</span></span>
2.  <span data-ttu-id="56371-131">按兩下 PreviewHandlerSDKSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="56371-131">Double-click the icon for the PreviewHandlerSDKSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="56371-132">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="56371-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="56371-133">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="56371-133">In that situation, it can be identified by its unique icon or by its type description "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="56371-134">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="56371-134">From the **Build** menu, select **Build Solution**.</span></span>

> [!Note]  
> <span data-ttu-id="56371-135">如果目標系統是64位 (x64) ，此範例預覽處理常式必須建立為64位應用程式。</span><span class="sxs-lookup"><span data-stu-id="56371-135">If the target system is 64-bit (x64), this sample preview handler must be built as a 64-bit application.</span></span>

 

## <a name="running-the-sample"></a><span data-ttu-id="56371-136">執行範例</span><span class="sxs-lookup"><span data-stu-id="56371-136">Running the Sample</span></span>

1.  <span data-ttu-id="56371-137">開啟 [命令提示字元] 視窗，並流覽至內建的 **RecipePreviewHandler** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="56371-137">Open the command prompt window and navigate to the built **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="56371-138">例如： `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler` 。</span><span class="sxs-lookup"><span data-stu-id="56371-138">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span></span> <span data-ttu-id="56371-139">輸入 `regsvr32.exe PreviewHandlerSDKSample.dll` 以註冊處理常式。</span><span class="sxs-lookup"><span data-stu-id="56371-139">Enter `regsvr32.exe PreviewHandlerSDKSample.dll` to register the handler.</span></span>
2.  <span data-ttu-id="56371-140">開啟 Windows 檔案總管，並顯示 [預覽] 窗格（如果尚未顯示）。</span><span class="sxs-lookup"><span data-stu-id="56371-140">Open Windows Explorer and show the preview pane if it is not already displayed.</span></span>
    -   <span data-ttu-id="56371-141">**Windows 7**：按一下 [預覽] 窗格按鈕。</span><span class="sxs-lookup"><span data-stu-id="56371-141">**Windows 7**: Click the preview pane button.</span></span>
    -   <span data-ttu-id="56371-142">**Windows Vista**：按一下 [ **組織** ] 功能表，移至 [ **版面** 配置] 子功能表，然後選取 [ **預覽窗格]**。</span><span class="sxs-lookup"><span data-stu-id="56371-142">**Windows Vista**: Click the **Organize** menu, go to the **Layout** submenu and select **Preview Pane**.</span></span>
3.  <span data-ttu-id="56371-143">使用 Windows 檔案總管流覽至 **RecipePreviewHandler** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="56371-143">Use Windows Explorer to navigate to the **RecipePreviewHandler** project directory.</span></span>
4.  <span data-ttu-id="56371-144">選取範例檔案。</span><span class="sxs-lookup"><span data-stu-id="56371-144">Select the example .recipe file.</span></span>

<span data-ttu-id="56371-145">若要讓32位 (x86) 和64位 (x64) 輸出可在64位版本的 Windows 上運作，請將 **AppId** 值設定為 WOW64 代理主機 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` ，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="56371-145">To make both the 32-bit (x86) and 64-bit (x64) output work on a 64-bit version of Windows, set the **AppId** value to the WOW64 surrogate host `{534A1E02-D58F-44f0-B58B-36CBED287C7C}`, as shown in the following code.</span></span>


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a><span data-ttu-id="56371-146">取消註冊範例預覽處理常式 DLL</span><span class="sxs-lookup"><span data-stu-id="56371-146">Unregistering the Sample Preview Handler DLL</span></span>

-   <span data-ttu-id="56371-147">開啟 [命令提示字元] 視窗，然後輸入 `regsvr32.exe /u PreviewHandlerSDKSample.dll` 以取消註冊處理常式。</span><span class="sxs-lookup"><span data-stu-id="56371-147">Open the command prompt window and enter `regsvr32.exe /u PreviewHandlerSDKSample.dll` to unregister the handler.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56371-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="56371-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56371-149">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="56371-149">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[<span data-ttu-id="56371-150">**IPreviewHandlerFrame**</span><span class="sxs-lookup"><span data-stu-id="56371-150">**IPreviewHandlerFrame**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[<span data-ttu-id="56371-151">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="56371-151">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
