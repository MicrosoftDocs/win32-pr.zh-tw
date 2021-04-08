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
# <a name="using-application-recovery-and-restart"></a>使用應用程式修復並重新啟動

應用程式可以使用應用程式復原，並重新啟動 (ARR) ，以在應用程式因未處理的例外狀況或應用程式停止回應之前結束之前儲存資料和狀態資訊。 如果要求，也會重新開機應用程式。

當您註冊復原或重新開機時，系統會將註冊資訊新增至進程。 [Windows 錯誤報告 (WER) ](/windows/desktop/wer/windows-error-reporting) 使用註冊資訊來呼叫您的復原回呼，然後重新開機您的應用程式。 例如，如果您註冊復原，而您的應用程式遇到未處理的例外狀況，則 WER 會向使用者顯示一個對話方塊，讓使用者可以選擇是否要在線上檢查方案、關閉程式，或將程式進行偵錯工具。 如果使用者選擇檢查解決方案或關閉程式，則 WER 會呼叫已註冊的回呼，並讓應用程式有機會儲存資料和狀態資訊。 當復原完成時，應用程式就會終止。

如果您註冊重新開機，而您的應用程式遇到未處理的例外狀況，則 WER 會顯示相同的對話給使用者，但會提供重新開機程式的選項，而不是關閉程式。 如果您同時註冊復原和重新開機，則會先進行復原;然後，應用程式會終止並重新啟動。

沒有回應的應用程式是以類似的方式處理。 如果應用程式沒有回應 Windows 訊息五秒，使用者接著嘗試與應用程式互動，則會被視為沒有回應;使用者會在標題列中看到)  (沒有回應。 當使用者按一下 [系統關閉] 按鈕時，會啟用 WER。

您必須在應用程式沒有回應或遇到未處理的例外狀況之前，註冊以進行復原或重新開機，或移除註冊。 不過，您可以在復原回呼中變更重新開機命令列。

如需註冊修復或重新開機的詳細資訊，請參閱下列主題：

-   [註冊應用程式復原](registering-for-application-recovery.md)
-   [註冊應用程式重新開機](registering-for-application-restart.md)

如需執行復原和重新開機功能的範例，請參閱 Windows SDK 位於 WinBase WindowsErrorReporting 資料夾中的 AppRecovery 和 AppRestart 範例 \\ 。

 

 