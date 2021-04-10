---
title: 使用 Windows Media Player SDK 開始使用
description: 使用 Windows Media Player SDK 開始使用
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player 行動裝置、外掛程式
- Windows Media Player 行動裝置、使用者介面外掛程式
- Windows Media Player Mobile 外掛程式
- 外掛程式，使用者介面
- 外掛程式，Windows Media Player Mobile
- 使用者介面外掛程式，Windows Media Player Mobile
- UI 外掛程式，Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685358"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a><span data-ttu-id="33e5d-110">使用 Windows Media Player SDK 開始使用</span><span class="sxs-lookup"><span data-stu-id="33e5d-110">Getting Started with the Windows Media Player SDK</span></span>

<span data-ttu-id="33e5d-111">若要建立外掛程式，您必須先安裝 Microsoft eMbedded Visual C++ 4.0 和 Visual Studio 2003。</span><span class="sxs-lookup"><span data-stu-id="33e5d-111">To create your plug-in, you first need to install Microsoft eMbedded Visual C++ 4.0 and Visual Studio 2003.</span></span> <span data-ttu-id="33e5d-112">您也必須安裝 Pocket PC 2003 SDK 或 Smartphone 2003 SDK （個別下載）。</span><span class="sxs-lookup"><span data-stu-id="33e5d-112">You must also install the Pocket PC 2003 SDK or the Smartphone 2003 SDK, which are separate downloads.</span></span> <span data-ttu-id="33e5d-113">若要編譯並執行專案，執行 Windows Mobile 2003 第二版作業系統的 Pocket PC 或 Smartphone 裝置必須使用 Microsoft ActiveSync®3.7.1 或更新版本，與開發電腦進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="33e5d-113">To compile and run the project, a Pocket PC or Smartphone device running the Windows Mobile 2003 Second Edition operating system must be synchronized with the development computer by using Microsoft ActiveSync® 3.7.1 or later.</span></span>

<span data-ttu-id="33e5d-114">因為 Windows Mobile 裝置上的 UI 外掛程式會使用與桌上出版本相同的外掛程式模型，所以您可以在建立可與 Windows Media Player 10 行動裝置搭配運作的背景 UI 外掛程式時，使用 Windows Media Player 外掛程式嚮導作為起點。</span><span class="sxs-lookup"><span data-stu-id="33e5d-114">Because UI plug-ins on Windows Mobile devices use the same plug-in model as the desktop versions, you can use the Windows Media Player Plug-in Wizard as a starting point when creating a background UI plug-in that will work with Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="33e5d-115">若要建立 UI 外掛程式程式碼，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="33e5d-115">To create UI plug-in code, do the following:</span></span>

1.  <span data-ttu-id="33e5d-116">開啟 Visual Studio 2003，並在 Visual C++ 中啟動新專案。</span><span class="sxs-lookup"><span data-stu-id="33e5d-116">Open Visual Studio 2003, and start a new project in Visual C++.</span></span>
2.  <span data-ttu-id="33e5d-117">從 [**範本**] 窗格中選取 [ **Windows Media Player 外掛程式]** 。</span><span class="sxs-lookup"><span data-stu-id="33e5d-117">Select **Windows Media Player Plug-in Wizard** from the **Templates** pane.</span></span>
3.  <span data-ttu-id="33e5d-118">命名您的專案 NetworkPlugin，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="33e5d-118">Name your project NetworkPlugin and click **OK**.</span></span>
4.  <span data-ttu-id="33e5d-119">選取 **UI 外掛程式** ，然後按 **[下一步**]。</span><span class="sxs-lookup"><span data-stu-id="33e5d-119">Select **UI Plug-in** and click **Next**.</span></span>
5.  <span data-ttu-id="33e5d-120">選取 **背景** ，然後按一下 **[下一步]**。</span><span class="sxs-lookup"><span data-stu-id="33e5d-120">Select **Background** and click **Next**.</span></span>
6.  <span data-ttu-id="33e5d-121">按 **[下一步]** 完成精靈。</span><span class="sxs-lookup"><span data-stu-id="33e5d-121">Click **Next** to finish the wizard.</span></span> <span data-ttu-id="33e5d-122">如果您要使用外掛程式來監視事件，您必須先核取 [ **接聽事件** ] 再完成嚮導，而且您應該閱讀 **IWMPEvents** 介面的檔，以瞭解 Windows Media Player 10 行動裝置支援哪些事件。</span><span class="sxs-lookup"><span data-stu-id="33e5d-122">If you are going to monitor events with your plug-in, you must check **Listen to events** before finishing the wizard, and you should read the documentation for the **IWMPEvents** interface to find out which events are supported on Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="33e5d-123">現在您已建立 UI 外掛程式程式碼，您必須在 eMbedded Visual C++ 4.0 中建立空的 Windows CE DLL 專案。</span><span class="sxs-lookup"><span data-stu-id="33e5d-123">Now that you have created your UI plug-in code, you need to create an empty Windows CE DLL project in eMbedded Visual C++ 4.0.</span></span> <span data-ttu-id="33e5d-124">然後將您的 wizard 產生的原始程式檔複製到該新專案，以便使用 ARM4 編譯器進行編譯。</span><span class="sxs-lookup"><span data-stu-id="33e5d-124">Then copy your wizard-generated source files to that new project so that they will compile with the ARM4 compiler.</span></span>

<span data-ttu-id="33e5d-125">若要建立空白專案</span><span class="sxs-lookup"><span data-stu-id="33e5d-125">To create an empty project</span></span>

1.  <span data-ttu-id="33e5d-126">在 eMbedded Visual C++ 中啟動新的專案，然後從 [**專案**] 窗格中選取 [ **WCE Dynamic-Link 程式庫**]。</span><span class="sxs-lookup"><span data-stu-id="33e5d-126">Start a new project in eMbedded Visual C++, and then select **WCE Dynamic-Link Library** from the **Projects** pane.</span></span>
2.  <span data-ttu-id="33e5d-127">命名您的專案，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="33e5d-127">Name your project and click **OK**.</span></span>
3.  <span data-ttu-id="33e5d-128">確認已選取 **空白的 WINDOWS CE DLL 專案** ，然後按一下 **[完成]**。</span><span class="sxs-lookup"><span data-stu-id="33e5d-128">Make sure **An empty Windows CE DLL project** is selected, and then click **Finish**.</span></span>
4.  <span data-ttu-id="33e5d-129">按一下 [ **專案** ] 功能表項目。</span><span class="sxs-lookup"><span data-stu-id="33e5d-129">Click the **Project** menu item.</span></span>
5.  <span data-ttu-id="33e5d-130">選取 [ **加入至專案**]，然後 **按一下 [** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="33e5d-130">Select **Add to Project**, and then click **Files**.</span></span>
6.  <span data-ttu-id="33e5d-131">選取您使用外掛程式嚮導建立的 c + + 檔案，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="33e5d-131">Select the C++ files you created with the plug-in wizard, and then click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33e5d-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="33e5d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33e5d-133">**建立 Windows Media Player 10 行動裝置版的消費者介面外掛程式**</span><span class="sxs-lookup"><span data-stu-id="33e5d-133">**Creating a User Interface Plug-in for Windows Media Player 10 Mobile**</span></span>](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[<span data-ttu-id="33e5d-134">**IWMPEvents 介面**</span><span class="sxs-lookup"><span data-stu-id="33e5d-134">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




