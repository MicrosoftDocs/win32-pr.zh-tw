---
title: 關於 WER
description: Windows 錯誤報告 (WER) 是一種彈性的事件型回饋基礎結構，其設計目的是要收集 Windows 可以偵測的硬體和軟體問題的相關資訊、向 Microsoft 回報資訊，以及為使用者提供任何可用的解決方案。 如需有關 WER 改進的詳細資訊，請參閱 WER 的新功能。
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Windows 錯誤報告 Windows 錯誤報告，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301331"
---
# <a name="about-wer"></a><span data-ttu-id="cc062-105">關於 WER</span><span class="sxs-lookup"><span data-stu-id="cc062-105">About WER</span></span>

<span data-ttu-id="cc062-106">Windows 錯誤報告 (WER) 是一種彈性的事件型回饋基礎結構，其設計目的是要收集 Windows 可以偵測的硬體和軟體問題的相關資訊、向 Microsoft 回報資訊，以及為使用者提供任何可用的解決方案。</span><span class="sxs-lookup"><span data-stu-id="cc062-106">Windows Error Reporting (WER) is a flexible event-based feedback infrastructure designed to gather information about the hardware and software problems that Windows can detect, report the information to Microsoft, and provide users with any available solutions.</span></span> <span data-ttu-id="cc062-107">如需有關 WER 改進的詳細資訊，請參閱 [wer 的新功能](what-s-new-in-wer.md)。</span><span class="sxs-lookup"><span data-stu-id="cc062-107">For information about the improvements to WER, see [What's New in WER](what-s-new-in-wer.md).</span></span>

<span data-ttu-id="cc062-108">從 Windows Vista 開始，Windows 預設會提供損毀、無回應和核心錯誤報表，而不需要變更您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cc062-108">Beginning with Windows Vista, Windows provides crash, no response, and kernel fault error reporting by default without requiring changes to your application.</span></span> <span data-ttu-id="cc062-109">應用程式會改為使用 WER API，針對與損毀、非回應或核心錯誤無關的應用程式特定問題，產生錯誤報表。</span><span class="sxs-lookup"><span data-stu-id="cc062-109">Applications instead use the WER API to generate error reports for application-specific issues that are not related to crashes, non-responses, or kernel faults.</span></span>

<span data-ttu-id="cc062-110">若要產生應用程式特定問題的錯誤報表，應用程式必須使用一些稱為 *報表參數* 的基本資訊來建立問題的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="cc062-110">To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called *report parameters*.</span></span> <span data-ttu-id="cc062-111">報表參數包括應用程式名稱、應用程式版本、模組名稱、模組版本和錯誤碼等資訊。</span><span class="sxs-lookup"><span data-stu-id="cc062-111">Report parameters include information such as the application name, application version, module name, module version, and error code.</span></span> <span data-ttu-id="cc062-112">這些報表參數的組合說明了唯一的問題。</span><span class="sxs-lookup"><span data-stu-id="cc062-112">The combination of these report parameters describes a unique problem.</span></span>

<span data-ttu-id="cc062-113">當 WER 檢查解決方案時，它會先詢問問題是否已經知道，以在 Microsoft 與 WER 伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="cc062-113">When WER checks for a solution, it communicates with the WER server at Microsoft by first asking if the problem is already known.</span></span> <span data-ttu-id="cc062-114">伺服器會以下列其中一種方式回應：</span><span class="sxs-lookup"><span data-stu-id="cc062-114">The server responds in one of the following ways:</span></span>

-   <span data-ttu-id="cc062-115">如果已知問題和解決方法，伺服器會將解決方案傳送給用戶端電腦，而 WER 會將這項資訊顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="cc062-115">If the problem is known and there is a solution, the server sends the solution to the client computer and WER displays this information to the user.</span></span>
-   <span data-ttu-id="cc062-116">如果問題正在調查中，伺服器可能會傳送指出狀態的回應。</span><span class="sxs-lookup"><span data-stu-id="cc062-116">If the problem is being investigated, the server may send a response that indicates the status.</span></span> <span data-ttu-id="cc062-117">如果開發人員需要更多的資訊來解決問題，伺服器會從 WER 要求其他資訊，而 WER 會要求使用者提供傳送此資訊的許可權。</span><span class="sxs-lookup"><span data-stu-id="cc062-117">If the developer needs more information to solve the problem, the server requests additional information from WER and WER asks the user for permission to send this information.</span></span>
-   <span data-ttu-id="cc062-118">如果問題不明，伺服器會建立一個問題，讓開發人員調查並傳送表示狀態的回應給 WER。</span><span class="sxs-lookup"><span data-stu-id="cc062-118">If the problem is not known, the server creates an issue for a developer to investigate and sends WER a response that indicates the status.</span></span>

<span data-ttu-id="cc062-119">使用此程式時，如果需要，則 WER 會收集更多的資訊，或將方案傳送給使用者（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="cc062-119">Using this process, WER gathers more information if needed or sends a solution to the user when available.</span></span> <span data-ttu-id="cc062-120">在 Windows Vista 中，使用者可以隨時前往 **問題報告和解決方案** 來查看可用的解決方案、檢查是否有新的解決方案可供使用，或管理其他的 WER 報告和設定。</span><span class="sxs-lookup"><span data-stu-id="cc062-120">On Windows Vista, the user can go to **Problem Reports and Solutions** at any time to view available solutions, check whether new solutions are available, or manage their other WER reports and settings.</span></span> <span data-ttu-id="cc062-121">在 Windows 7 上， **問題報告和解決方案** 現在稱為「 **動作中心**」。</span><span class="sxs-lookup"><span data-stu-id="cc062-121">On Windows 7, the **Problem Reports and Solutions** is now called the **Action Center**.</span></span> <span data-ttu-id="cc062-122">按一下 [ **開始** ]，在 [ **搜尋程式及** 檔案] 中輸入 "view"，然後選取 [ **查看所有問題報告**]、[ **查看可靠性歷程記錄**] 或 [ **查看問題的解決方案**]。</span><span class="sxs-lookup"><span data-stu-id="cc062-122">Click **Start** and enter "view" in **Search programs and files** and then select **View all problem reports**, **View reliability history**, or **View solutions to problems**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc062-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc062-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc062-124">Windows 錯誤報告</span><span class="sxs-lookup"><span data-stu-id="cc062-124">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 




