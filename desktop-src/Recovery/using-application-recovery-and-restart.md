---
title: 使用應用程式修復並重新啟動
description: 應用程式可以使用應用程式復原，並重新啟動 (ARR) ，以在應用程式因未處理的例外狀況或應用程式停止回應之前結束之前儲存資料和狀態資訊。 如果要求，也會重新開機應用程式。
ms.assetid: 28cbb4c0-a287-4302-b3a9-daddc69adb40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5bf0b9bd0e0f6cc257ee785ab5df6febc8fef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842364"
---
# <a name="using-application-recovery-and-restart"></a><span data-ttu-id="a998d-104">使用應用程式修復並重新啟動</span><span class="sxs-lookup"><span data-stu-id="a998d-104">Using Application Recovery and Restart</span></span>

<span data-ttu-id="a998d-105">應用程式可以使用應用程式復原，並重新啟動 (ARR) ，以在應用程式因未處理的例外狀況或應用程式停止回應之前結束之前儲存資料和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="a998d-105">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="a998d-106">如果要求，也會重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="a998d-106">The application is also restarted, if requested.</span></span>

<span data-ttu-id="a998d-107">當您註冊復原或重新開機時，系統會將註冊資訊新增至進程。</span><span class="sxs-lookup"><span data-stu-id="a998d-107">When you register for recovery or restart, the registration information is added to the process.</span></span> <span data-ttu-id="a998d-108">[Windows 錯誤報告 (WER) ](/windows/desktop/wer/windows-error-reporting) 使用註冊資訊來呼叫您的復原回呼，然後重新開機您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a998d-108">[Windows Error Reporting (WER)](/windows/desktop/wer/windows-error-reporting) uses the registration information to call your recovery callback and restart your application.</span></span> <span data-ttu-id="a998d-109">例如，如果您註冊復原，而您的應用程式遇到未處理的例外狀況，則 WER 會向使用者顯示一個對話方塊，讓使用者可以選擇是否要在線上檢查方案、關閉程式，或將程式進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="a998d-109">For example, if you register for recovery and your application encounters an unhandled exception, WER displays a dialog to the user that gives the user the option of checking for a solution online, closing the program, or debugging the program.</span></span> <span data-ttu-id="a998d-110">如果使用者選擇檢查解決方案或關閉程式，則 WER 會呼叫已註冊的回呼，並讓應用程式有機會儲存資料和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="a998d-110">If the user chooses to either check for a solution or close the program, WER calls the registered callback and gives the application the chance to save data and state information.</span></span> <span data-ttu-id="a998d-111">當復原完成時，應用程式就會終止。</span><span class="sxs-lookup"><span data-stu-id="a998d-111">When the recovery is complete, the application is terminated.</span></span>

<span data-ttu-id="a998d-112">如果您註冊重新開機，而您的應用程式遇到未處理的例外狀況，則 WER 會顯示相同的對話給使用者，但會提供重新開機程式的選項，而不是關閉程式。</span><span class="sxs-lookup"><span data-stu-id="a998d-112">If you register for restart and your application encounters an unhandled exception, WER displays the same dialog to the user but gives the option of restarting the program instead of closing the program.</span></span> <span data-ttu-id="a998d-113">如果您同時註冊復原和重新開機，則會先進行復原;然後，應用程式會終止並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="a998d-113">If you register for both recovery and restart, recovery occurs first; the application is then terminated and restarted.</span></span>

<span data-ttu-id="a998d-114">沒有回應的應用程式是以類似的方式處理。</span><span class="sxs-lookup"><span data-stu-id="a998d-114">An unresponsive application is handled in a similar fashion.</span></span> <span data-ttu-id="a998d-115">如果應用程式沒有回應 Windows 訊息五秒，使用者接著嘗試與應用程式互動，則會被視為沒有回應;使用者會在標題列中看到)  (沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a998d-115">An application is considered unresponsive if it does not respond to Windows messages for five seconds and the user then tries to interact with the application; the user will see (Not Responding) in the title bar.</span></span> <span data-ttu-id="a998d-116">當使用者按一下 [系統關閉] 按鈕時，會啟用 WER。</span><span class="sxs-lookup"><span data-stu-id="a998d-116">WER is activated when the user clicks the system close button.</span></span>

<span data-ttu-id="a998d-117">您必須在應用程式沒有回應或遇到未處理的例外狀況之前，註冊以進行復原或重新開機，或移除註冊。</span><span class="sxs-lookup"><span data-stu-id="a998d-117">You must register for recovery or restart, or remove the registration, before the application becomes unresponsive or encounters an unhandled exception.</span></span> <span data-ttu-id="a998d-118">不過，您可以在復原回呼中變更重新開機命令列。</span><span class="sxs-lookup"><span data-stu-id="a998d-118">However, in your recovery callback, you can change the restart command line.</span></span>

<span data-ttu-id="a998d-119">如需註冊修復或重新開機的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="a998d-119">For details on registering for recovery or restart, see the following topics:</span></span>

-   [<span data-ttu-id="a998d-120">註冊應用程式復原</span><span class="sxs-lookup"><span data-stu-id="a998d-120">Registering for Application Recovery</span></span>](registering-for-application-recovery.md)
-   [<span data-ttu-id="a998d-121">註冊應用程式重新開機</span><span class="sxs-lookup"><span data-stu-id="a998d-121">Registering for Application Restart</span></span>](registering-for-application-restart.md)

<span data-ttu-id="a998d-122">如需執行復原和重新開機功能的範例，請參閱 Windows SDK 位於 WinBase WindowsErrorReporting 資料夾中的 AppRecovery 和 AppRestart 範例 \\ 。</span><span class="sxs-lookup"><span data-stu-id="a998d-122">For samples that implement the recovery and restart features, see the AppRecovery and AppRestart samples in the Windows SDK located in the WinBase\\WindowsErrorReporting folder.</span></span>

 

 