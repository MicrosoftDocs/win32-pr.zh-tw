---
description: 您可以使用下列程式，來對以 Microsoft Visual C++ 撰寫的專家進行 debug 錯。
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: 錯專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985205"
---
# <a name="debugging-an-expert"></a><span data-ttu-id="da340-103">錯專家</span><span class="sxs-lookup"><span data-stu-id="da340-103">Debugging an Expert</span></span>

<span data-ttu-id="da340-104">您可以使用下列程式，來對以 Microsoft Visual C++ 撰寫的專家進行 debug 錯。</span><span class="sxs-lookup"><span data-stu-id="da340-104">Use the following procedure to debug experts written in Microsoft Visual C++.</span></span>

<span data-ttu-id="da340-105">**錯專家**</span><span class="sxs-lookup"><span data-stu-id="da340-105">**Debugging an Expert**</span></span>

1.  <span data-ttu-id="da340-106">將專家 (DLL 檔) 和程式資料庫檔案 ( .pdb) 當您在正確的位置中編譯專家時產生。</span><span class="sxs-lookup"><span data-stu-id="da340-106">Install the expert (DLL file) and the program database file (.pdb) generated when you compiled the expert in the correct location.</span></span> <span data-ttu-id="da340-107">如需詳細資訊，請參閱 [安裝專家至網路監視器 2.1](installing-an-expert-to-network-monitor-2-1.md)。</span><span class="sxs-lookup"><span data-stu-id="da340-107">For further details, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="da340-108">開始 Microsoft Visual C++。</span><span class="sxs-lookup"><span data-stu-id="da340-108">Start Microsoft Visual C++.</span></span>
3.  <span data-ttu-id="da340-109">**在 [檔案] 功能表中**，按一下 [**開啟**]，然後選取您的專家 DLL 名稱。</span><span class="sxs-lookup"><span data-stu-id="da340-109">From the **File** menu, click **Open** and select the name of your expert DLL.</span></span>
4.  <span data-ttu-id="da340-110">Microsoft Visual C++ 載入之後，請按一下 [ **專案** ] 功能表，然後按一下 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="da340-110">After Microsoft Visual C++ loads, click the **Project** menu and then click **Settings**.</span></span>
5.  <span data-ttu-id="da340-111">按一下 [ **Debug**]。</span><span class="sxs-lookup"><span data-stu-id="da340-111">Click **Debug**.</span></span> <span data-ttu-id="da340-112">在 [ **可執行檔**] 下，輸入 Netmon.exe 的完整路徑，例如：</span><span class="sxs-lookup"><span data-stu-id="da340-112">Under **Executable for debug session**, type the full path of Netmon.exe, for example:</span></span>

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  <span data-ttu-id="da340-113">在您的程式碼中設定中斷點。</span><span class="sxs-lookup"><span data-stu-id="da340-113">Set the breakpoints in your code.</span></span>

 

 



