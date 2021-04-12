---
description: 下列清單包含 TAPI MSP 支援的功能。
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: 支援的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191368"
---
# <a name="features-supported"></a><span data-ttu-id="3abb3-103">支援的功能</span><span class="sxs-lookup"><span data-stu-id="3abb3-103">Features Supported</span></span>

<span data-ttu-id="3abb3-104">下列清單包含 TAPI MSP 支援的功能。</span><span class="sxs-lookup"><span data-stu-id="3abb3-104">The following list contains the TAPI MSP supported features.</span></span>

-   <span data-ttu-id="3abb3-105">執行 MSP，以處理每個 MSP 實例的單一位址。</span><span class="sxs-lookup"><span data-stu-id="3abb3-105">Implements an MSP that handles a single address per instance of the MSP.</span></span> <span data-ttu-id="3abb3-106">多個類似的位址是藉由具現化 MSP 多次來處理。</span><span class="sxs-lookup"><span data-stu-id="3abb3-106">Multiple like addresses are handled by instantiating the MSP multiple times.</span></span> <span data-ttu-id="3abb3-107">這可大幅簡化 MSP 和基類的執行。</span><span class="sxs-lookup"><span data-stu-id="3abb3-107">This greatly simplifies the implementation of the MSP and the base classes.</span></span>
-   <span data-ttu-id="3abb3-108">會實 MSPI 介面，包括 [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)、 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)、 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)和 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)。</span><span class="sxs-lookup"><span data-stu-id="3abb3-108">Implements all the MSPI interfaces, including [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>
-   <span data-ttu-id="3abb3-109">針對音訊和影片執行立即可用的靜態終端機。</span><span class="sxs-lookup"><span data-stu-id="3abb3-109">Implements ready-to-use static terminals for both audio and video.</span></span>
-   <span data-ttu-id="3abb3-110">實作為泛型終端基類。</span><span class="sxs-lookup"><span data-stu-id="3abb3-110">Implements generic terminal base classes.</span></span> <span data-ttu-id="3abb3-111">上述的靜態終端機和 Termmgr.dll 中找到的動態終端機，都使用這些終端基類。</span><span class="sxs-lookup"><span data-stu-id="3abb3-111">These terminal base classes are used by both the above-mentioned static terminal implementations and the implementations of dynamic terminals that are found in Termmgr.dll.</span></span> <span data-ttu-id="3abb3-112">MSP 也可以使用它們來執行額外的終端機。</span><span class="sxs-lookup"><span data-stu-id="3abb3-112">The MSP can also use them to implement additional terminals.</span></span>
-   <span data-ttu-id="3abb3-113">使用終端機管理員來處理動態終端。</span><span class="sxs-lookup"><span data-stu-id="3abb3-113">Uses the Terminal Manager to handle dynamic terminals.</span></span> <span data-ttu-id="3abb3-114">使用訊息泵 (在背景工作執行緒上建立動態終端機，讓主控台應用程式不必處理影片轉譯終端機的視窗訊息，也可以簡化) 的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="3abb3-114">Creates dynamic terminals on a worker thread with a message pump (to free console applications from having to process window messages for video render terminals and to simplify synchronization issues).</span></span>
-   <span data-ttu-id="3abb3-115">支援針對每個資料流程使用篩選圖形的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3abb3-115">Supports calls that use a filter graph per stream.</span></span>
-   <span data-ttu-id="3abb3-116">實行圖形事件的處理。</span><span class="sxs-lookup"><span data-stu-id="3abb3-116">Implements handling of graph events.</span></span>
-   <span data-ttu-id="3abb3-117">會搭配本身的背景工作執行緒使用執行緒共用 Api 來處理事件。</span><span class="sxs-lookup"><span data-stu-id="3abb3-117">Uses the thread pooling APIs, in conjunction with a worker thread of its own, to handle events.</span></span>
-   <span data-ttu-id="3abb3-118">使用原本針對路由) 專案開發的 Windows 2000 (追蹤 Api，以及額外的邏輯來提供有彈性的一般記錄機制，可同時登入下列任何組合：使用者或核心模式的偵錯工具;以元件分隔記錄訊息的個別主控台視窗;記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3abb3-118">Uses the tracing APIs of Windows 2000 (originally developed for the Routing project) along with additional logic to provide a flexible, generic logging mechanism that can simultaneously log to any combination of the following: a user or kernel-mode debugger; a separate console window with log messages separated by component; a log file.</span></span>
-   <span data-ttu-id="3abb3-119">執行無限制執行緒。</span><span class="sxs-lookup"><span data-stu-id="3abb3-119">Runs free-threaded.</span></span>

 

 
