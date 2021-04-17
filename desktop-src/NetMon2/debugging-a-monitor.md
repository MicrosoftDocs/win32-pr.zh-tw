---
description: 下列程式示範如何對監視器進行偵錯工具。
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: 偵測監視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513340"
---
# <a name="debugging-a-monitor"></a><span data-ttu-id="1aa97-103">偵測監視</span><span class="sxs-lookup"><span data-stu-id="1aa97-103">Debugging a Monitor</span></span>

<span data-ttu-id="1aa97-104">下列程式示範如何對監視器進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="1aa97-104">The following procedure demonstrates how to debug a monitor.</span></span>

<span data-ttu-id="1aa97-105">**若要對監視器進行調試**</span><span class="sxs-lookup"><span data-stu-id="1aa97-105">**To debug a monitor**</span></span>

1.  <span data-ttu-id="1aa97-106">當您在正確的位置中編譯監視器時，請安裝監視 DLL 和程式資料庫 ( .pdb) 檔案。</span><span class="sxs-lookup"><span data-stu-id="1aa97-106">Install the monitor DLL and the program database (.pdb) file generated when you compiled the monitor in the correct location.</span></span> <span data-ttu-id="1aa97-107">如需進一步的詳細資料，請參閱 [安裝監視器以網路監視器](installing-a-monitor-to-network-monitor.md) 。</span><span class="sxs-lookup"><span data-stu-id="1aa97-107">See [Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) for further details.</span></span>
2.  <span data-ttu-id="1aa97-108">選取 [主控台]、[服務]，確認監視器控制服務已設定為伺服器，而不是服務。</span><span class="sxs-lookup"><span data-stu-id="1aa97-108">Verify that the Monitor Control Service is configured as a server instead of a service by selecting Control Panel, Services.</span></span>
3.  <span data-ttu-id="1aa97-109">開啟命令提示字元，然後移至網路監視器目錄。</span><span class="sxs-lookup"><span data-stu-id="1aa97-109">Open a command prompt and go to the Network Monitor directory.</span></span> <span data-ttu-id="1aa97-110">輸入：</span><span class="sxs-lookup"><span data-stu-id="1aa97-110">Type:</span></span>

    <span data-ttu-id="1aa97-111">**Mcsvc.exe/RegServer**</span><span class="sxs-lookup"><span data-stu-id="1aa97-111">**Mcsvc.exe /RegServer**</span></span>

    <span data-ttu-id="1aa97-112">在監視的偵錯工具完成之後，您可以輸入下列命令，將 MCSVC 傳回到其預設條件：</span><span class="sxs-lookup"><span data-stu-id="1aa97-112">After the monitor debugging session is complete, you can return the MCSVC to its default condition by typing:</span></span>

    <span data-ttu-id="1aa97-113">**Mcsvc.exe/Service**</span><span class="sxs-lookup"><span data-stu-id="1aa97-113">**Mcsvc.exe /Service**</span></span>

4.  <span data-ttu-id="1aa97-114">在 Microsoft Visual Studio 中，啟動 Microsoft Visual C++。</span><span class="sxs-lookup"><span data-stu-id="1aa97-114">In Microsoft Visual Studio, launch Microsoft Visual C++.</span></span>
5.  <span data-ttu-id="1aa97-115">從 [**檔案] 的 [\*\*\*\*開啟** 功能表] 選項中，選取您的監視器 DLL 名稱。</span><span class="sxs-lookup"><span data-stu-id="1aa97-115">From the **File**, **Open** menu option, select the name of your monitor DLL.</span></span>
6.  <span data-ttu-id="1aa97-116">Microsoft Visual C++ 載入之後，請按一下 [ **專案**]、[ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="1aa97-116">After Microsoft Visual C++ loads, click **Project**, **Settings**.</span></span>
7.  <span data-ttu-id="1aa97-117">按一下 [**可執行檔**] 下的 [**調試** 程式] 索引標籤來進行 debug session，然後輸入 Mcsvc.exe 的完整路徑</span><span class="sxs-lookup"><span data-stu-id="1aa97-117">Click the **Debug** tab under **Executable** for debug session and type the full path of Mcsvc.exe.</span></span> <span data-ttu-id="1aa97-118">例如，C： \\ Program files \\ Netmon2 \\Mcsvc.exe。</span><span class="sxs-lookup"><span data-stu-id="1aa97-118">For example, C:\\Program files\\Netmon2\\Mcsvc.exe.</span></span>
8.  <span data-ttu-id="1aa97-119">在程式碼中設定中斷點。</span><span class="sxs-lookup"><span data-stu-id="1aa97-119">Set the breakpoints in the code.</span></span>

> [!Note]  
> <span data-ttu-id="1aa97-120">請勿使用訊息方塊來監視偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="1aa97-120">Do not use a message box for monitor debugging.</span></span> <span data-ttu-id="1aa97-121">如果 MCSVC 是以服務的形式執行，您將不會看到快顯視窗，而且 MCSVC 會顯示為「停止回應」。</span><span class="sxs-lookup"><span data-stu-id="1aa97-121">If the MCSVC is running as a service, you will not see the popup, and MCSVC will appear to hang.</span></span>

 

 

 



