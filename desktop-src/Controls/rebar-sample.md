---
title: Rebar 範例
ms.assetid: f26c0819-523d-42a5-be2f-3cd75748b4a6
description: 深入瞭解： Rebar 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72b58a66c22b0ef8cc60d97c0965a8ae29a20fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936103"
---
# <a name="rebar-sample"></a><span data-ttu-id="97cbc-103">Rebar 範例</span><span class="sxs-lookup"><span data-stu-id="97cbc-103">Rebar Sample</span></span>

<span data-ttu-id="97cbc-104">本主題描述 Rebar 範例程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="97cbc-104">This topic describes the Rebar Sample code sample.</span></span> <span data-ttu-id="97cbc-105">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="97cbc-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="97cbc-106">說明</span><span class="sxs-lookup"><span data-stu-id="97cbc-106">Description</span></span>](#description)
-   [<span data-ttu-id="97cbc-107">最低需求</span><span class="sxs-lookup"><span data-stu-id="97cbc-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="97cbc-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="97cbc-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="97cbc-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="97cbc-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="97cbc-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="97cbc-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="97cbc-111">Description</span><span class="sxs-lookup"><span data-stu-id="97cbc-111">Description</span></span>

<span data-ttu-id="97cbc-112">Rebar 範例顯示如何在應用程式中執行簡單的 Rebar 通用控制項。</span><span class="sxs-lookup"><span data-stu-id="97cbc-112">The Rebar Sample shows how to implement a simple rebar common control in an application.</span></span> <span data-ttu-id="97cbc-113">這個範例會建立一個具有兩個帶的 Rebar 控制項。</span><span class="sxs-lookup"><span data-stu-id="97cbc-113">This example creates a rebar control that has two bands.</span></span> <span data-ttu-id="97cbc-114">其中一個包含下拉式方塊，另一個則包含推播按鈕。</span><span class="sxs-lookup"><span data-stu-id="97cbc-114">One contains a combo box and the other contains a push button.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="97cbc-115">最低需求</span><span class="sxs-lookup"><span data-stu-id="97cbc-115">Minimum Requirements</span></span>



| <span data-ttu-id="97cbc-116">產品</span><span class="sxs-lookup"><span data-stu-id="97cbc-116">Product</span></span>          | <span data-ttu-id="97cbc-117">版本</span><span class="sxs-lookup"><span data-stu-id="97cbc-117">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="97cbc-118">DLL</span><span class="sxs-lookup"><span data-stu-id="97cbc-118">DLL</span></span>              | <span data-ttu-id="97cbc-119">comctl32.dll 版本4.71</span><span class="sxs-lookup"><span data-stu-id="97cbc-119">comctl32.dll version 4.71</span></span>             |
| <span data-ttu-id="97cbc-120">作業系統</span><span class="sxs-lookup"><span data-stu-id="97cbc-120">Operating System</span></span> | <span data-ttu-id="97cbc-121">具有 Internet Explorer 4.0 的 Windows 95</span><span class="sxs-lookup"><span data-stu-id="97cbc-121">Windows 95 with Internet Explorer 4.0</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="97cbc-122">下載範例</span><span class="sxs-lookup"><span data-stu-id="97cbc-122">Downloading the Sample</span></span>

<span data-ttu-id="97cbc-123">Rebar 範例會安裝為 [Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx) 的一部分，並可在下列位置中取得。</span><span class="sxs-lookup"><span data-stu-id="97cbc-123">The Rebar Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="97cbc-124">Location</span><span class="sxs-lookup"><span data-stu-id="97cbc-124">Location</span></span>    | <span data-ttu-id="97cbc-125">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="97cbc-125">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97cbc-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="97cbc-126">Windows SDK</span></span> | <span data-ttu-id="97cbc-127">% Program Files% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ 控制 \\ 通用 \\ Rebar</span><span class="sxs-lookup"><span data-stu-id="97cbc-127">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\rebar</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="97cbc-128">建立範例</span><span class="sxs-lookup"><span data-stu-id="97cbc-128">Building the Sample</span></span>

<span data-ttu-id="97cbc-129">若要使用命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="97cbc-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="97cbc-130">開啟 [命令提示字元] 視窗，並流覽至專案目錄。</span><span class="sxs-lookup"><span data-stu-id="97cbc-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="97cbc-131">輸入 `msbuild [project file]`。</span><span class="sxs-lookup"><span data-stu-id="97cbc-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="97cbc-132">若要使用 Visual Studio 建立範例：</span><span class="sxs-lookup"><span data-stu-id="97cbc-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="97cbc-133">開啟 Windows 檔案總管並流覽至專案目錄。</span><span class="sxs-lookup"><span data-stu-id="97cbc-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="97cbc-134">按兩下 vcproj 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="97cbc-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="97cbc-135">從 [ **組建** ] 功能表中，選取 [ **建立方案** ] 來建立方案。</span><span class="sxs-lookup"><span data-stu-id="97cbc-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97cbc-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="97cbc-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97cbc-137">Rebar 控制項</span><span class="sxs-lookup"><span data-stu-id="97cbc-137">Rebar Controls</span></span>](rebar-controls.md)
</dt> </dl>

 

 




