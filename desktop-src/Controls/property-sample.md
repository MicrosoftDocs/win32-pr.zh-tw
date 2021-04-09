---
title: 屬性範例
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 深入瞭解：屬性範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110152"
---
# <a name="property-sample"></a><span data-ttu-id="f5b08-103">屬性範例</span><span class="sxs-lookup"><span data-stu-id="f5b08-103">Property Sample</span></span>

<span data-ttu-id="f5b08-104">本主題說明屬性範例程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="f5b08-104">This topic describes the Property Sample code sample.</span></span> <span data-ttu-id="f5b08-105">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="f5b08-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="f5b08-106">說明</span><span class="sxs-lookup"><span data-stu-id="f5b08-106">Description</span></span>](#description)
-   [<span data-ttu-id="f5b08-107">最低需求</span><span class="sxs-lookup"><span data-stu-id="f5b08-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="f5b08-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="f5b08-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f5b08-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="f5b08-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f5b08-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5b08-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="f5b08-111">Description</span><span class="sxs-lookup"><span data-stu-id="f5b08-111">Description</span></span>

<span data-ttu-id="f5b08-112">屬性範例會示範如何執行三種不同的屬性工作表樣式：強制回應、非模式和 wizard。</span><span class="sxs-lookup"><span data-stu-id="f5b08-112">The Property Sample shows how to implement three different styles of property sheets: modal, modeless, and wizard.</span></span> <span data-ttu-id="f5b08-113">它也會示範如何使用 [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) 函式來修改建立之前或之後的屬性工作表對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f5b08-113">It also shows how to use the [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) function to modify the property sheet dialog before or after it is created.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="f5b08-114">最低需求</span><span class="sxs-lookup"><span data-stu-id="f5b08-114">Minimum Requirements</span></span>



| <span data-ttu-id="f5b08-115">產品</span><span class="sxs-lookup"><span data-stu-id="f5b08-115">Product</span></span>          | <span data-ttu-id="f5b08-116">版本</span><span class="sxs-lookup"><span data-stu-id="f5b08-116">Version</span></span>                              |
|------------------|--------------------------------------|
| <span data-ttu-id="f5b08-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b08-117">DLL</span></span>              | <span data-ttu-id="f5b08-118">comctl32.dll 版本4。0</span><span class="sxs-lookup"><span data-stu-id="f5b08-118">comctl32.dll version 4.0</span></span>             |
| <span data-ttu-id="f5b08-119">作業系統</span><span class="sxs-lookup"><span data-stu-id="f5b08-119">Operating System</span></span> | <span data-ttu-id="f5b08-120">Windows 95、Microsoft Windows NT 3。1</span><span class="sxs-lookup"><span data-stu-id="f5b08-120">Windows 95, Microsoft Windows NT 3.1</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f5b08-121">下載範例</span><span class="sxs-lookup"><span data-stu-id="f5b08-121">Downloading the Sample</span></span>

<span data-ttu-id="f5b08-122">屬性範例會安裝為 [Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx) 的一部分，並可在下列位置中取得。</span><span class="sxs-lookup"><span data-stu-id="f5b08-122">The Property Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="f5b08-123">Location</span><span class="sxs-lookup"><span data-stu-id="f5b08-123">Location</span></span>    | <span data-ttu-id="f5b08-124">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="f5b08-124">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b08-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f5b08-125">Windows SDK</span></span> | <span data-ttu-id="f5b08-126">% Program Files% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ 控制項 \\ 通用 \\ 屬性</span><span class="sxs-lookup"><span data-stu-id="f5b08-126">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\property</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="f5b08-127">建立範例</span><span class="sxs-lookup"><span data-stu-id="f5b08-127">Building the Sample</span></span>

<span data-ttu-id="f5b08-128">若要使用命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="f5b08-128">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="f5b08-129">開啟 [命令提示字元] 視窗，並流覽至專案目錄。</span><span class="sxs-lookup"><span data-stu-id="f5b08-129">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="f5b08-130">輸入 `msbuild [project file]`。</span><span class="sxs-lookup"><span data-stu-id="f5b08-130">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="f5b08-131">若要使用 Visual Studio 建立範例：</span><span class="sxs-lookup"><span data-stu-id="f5b08-131">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="f5b08-132">開啟 Windows 檔案總管並流覽至專案目錄。</span><span class="sxs-lookup"><span data-stu-id="f5b08-132">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="f5b08-133">按兩下 vcproj 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="f5b08-133">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="f5b08-134">從 [ **組建** ] 功能表中，選取 [ **建立方案** ] 來建立方案。</span><span class="sxs-lookup"><span data-stu-id="f5b08-134">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5b08-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5b08-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5b08-136">關於屬性工作表</span><span class="sxs-lookup"><span data-stu-id="f5b08-136">About Property Sheets</span></span>](property-sheets.md)
</dt> </dl>

 

 




