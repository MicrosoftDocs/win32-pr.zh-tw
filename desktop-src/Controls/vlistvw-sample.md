---
title: VListVW 範例
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 深入瞭解： VListVW 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970110"
---
# <a name="vlistvw-sample"></a><span data-ttu-id="d7e53-103">VListVW 範例</span><span class="sxs-lookup"><span data-stu-id="d7e53-103">VListVW Sample</span></span>

<span data-ttu-id="d7e53-104">本主題說明 VListVW 範例程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="d7e53-104">This topic describes the VListVW Sample code sample.</span></span> <span data-ttu-id="d7e53-105">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="d7e53-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="d7e53-106">說明</span><span class="sxs-lookup"><span data-stu-id="d7e53-106">Description</span></span>](#description)
-   [<span data-ttu-id="d7e53-107">最低需求</span><span class="sxs-lookup"><span data-stu-id="d7e53-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="d7e53-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="d7e53-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d7e53-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="d7e53-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d7e53-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7e53-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="d7e53-111">Description</span><span class="sxs-lookup"><span data-stu-id="d7e53-111">Description</span></span>

<span data-ttu-id="d7e53-112">VListVW 範例示範如何在應用程式中執行簡單的虛擬清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="d7e53-112">The VListVW Sample shows how to implement a simple virtual list-view control in an application.</span></span> <span data-ttu-id="d7e53-113">虛擬清單-view 控制項是具有 **lvs) \_ OWNERDATA** 樣式的標準清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="d7e53-113">A virtual list-view control is a standard list-view control with the **LVS\_OWNERDATA** style.</span></span> <span data-ttu-id="d7e53-114">此範例會建立「虛擬」保存100000專案的清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="d7e53-114">This example creates a list-view control that "virtually" holds 100,000 items.</span></span> <span data-ttu-id="d7e53-115">絕不會實際新增專案。</span><span class="sxs-lookup"><span data-stu-id="d7e53-115">The items are never actually added.</span></span> <span data-ttu-id="d7e53-116">相反地，虛擬清單視圖控制項會「告知」它包含 [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) 訊息的專案數目。</span><span class="sxs-lookup"><span data-stu-id="d7e53-116">Instead, the virtual list-view control is "told" how many items it contains with the [**LVM\_SETITEMCOUNT**](lvm-setitemcount.md) message.</span></span> <span data-ttu-id="d7e53-117">當需要繪製專案時，清單視圖控制項會查詢父視窗，以取得 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知的顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="d7e53-117">When an item needs to be drawn, the list-view control queries the parent window for display information with the [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="d7e53-118">最低需求</span><span class="sxs-lookup"><span data-stu-id="d7e53-118">Minimum Requirements</span></span>



| <span data-ttu-id="d7e53-119">產品</span><span class="sxs-lookup"><span data-stu-id="d7e53-119">Product</span></span>          | <span data-ttu-id="d7e53-120">版本</span><span class="sxs-lookup"><span data-stu-id="d7e53-120">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="d7e53-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d7e53-121">DLL</span></span>              | <span data-ttu-id="d7e53-122">comctl32.dll 版本4.70</span><span class="sxs-lookup"><span data-stu-id="d7e53-122">comctl32.dll version 4.70</span></span>             |
| <span data-ttu-id="d7e53-123">作業系統</span><span class="sxs-lookup"><span data-stu-id="d7e53-123">Operating System</span></span> | <span data-ttu-id="d7e53-124">Windows 95、Microsoft Windows NT 3.51</span><span class="sxs-lookup"><span data-stu-id="d7e53-124">Windows 95, Microsoft Windows NT 3.51</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d7e53-125">下載範例</span><span class="sxs-lookup"><span data-stu-id="d7e53-125">Downloading the Sample</span></span>

<span data-ttu-id="d7e53-126">VListVW 範例可在 github 上的 [Windows 傳統範例存放庫](https://github.com/microsoft/Windows-classic-samples)中取得。</span><span class="sxs-lookup"><span data-stu-id="d7e53-126">The VListVW Sample is available on on github in the [Windows Classic Samples repository](https://github.com/microsoft/Windows-classic-samples).</span></span> <span data-ttu-id="d7e53-127">您可以在[這裡](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)找到清單視圖控制項專案範例</span><span class="sxs-lookup"><span data-stu-id="d7e53-127">The list view control items examples can be found at [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="d7e53-128">建立範例</span><span class="sxs-lookup"><span data-stu-id="d7e53-128">Building the Sample</span></span>

<span data-ttu-id="d7e53-129">若要使用命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="d7e53-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="d7e53-130">開啟 [命令提示字元] 視窗，並流覽至專案目錄。</span><span class="sxs-lookup"><span data-stu-id="d7e53-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="d7e53-131">輸入 `msbuild [project file]`。</span><span class="sxs-lookup"><span data-stu-id="d7e53-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="d7e53-132">若要使用 Visual Studio 建立範例：</span><span class="sxs-lookup"><span data-stu-id="d7e53-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="d7e53-133">開啟 Windows 檔案總管並流覽至專案目錄。</span><span class="sxs-lookup"><span data-stu-id="d7e53-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="d7e53-134">按兩下 vcproj 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="d7e53-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="d7e53-135">從 [ **組建** ] 功能表中，選取 [ **建立方案** ] 來建立方案。</span><span class="sxs-lookup"><span data-stu-id="d7e53-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7e53-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7e53-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7e53-137">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="d7e53-137">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> </dl>

 

 




