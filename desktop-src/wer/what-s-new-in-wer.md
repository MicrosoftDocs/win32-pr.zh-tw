---
title: WER 的新功能
description: 此頁面摘要說明每個版本 Windows 錯誤報告 (WER) 的新功能。
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Windows 錯誤報告 Windows 錯誤報告，新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314647"
---
# <a name="whats-new-in-wer"></a>WER 的新功能

此頁面摘要說明每個版本 Windows 錯誤報告 (WER) 的新功能。

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 與 Windows Server 2008 R2

下列清單摘要說明適用于 Windows 7 和 Windows Server 2008 R2 的新 WER 功能。

-   新增引發例外狀況的功能，以略過所有例外狀況處理常式，進而立即終止應用程式並叫用 Windows 錯誤報告。 如需詳細資訊，請參閱 [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) 函數。
-   加入註冊跨進程例外狀況處理常式的功能，當發生損毀時，會呼叫 WER，以收集事件名稱、報告參數和偵錯工具啟動選項。 如需詳細資訊，請參閱 [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) 函數。

已新增的函式：

-   [**OutOfProcessExceptionEventCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [**OutOfProcessExceptionEventSignatureCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [**OutOfProcessExceptionEventDebuggerLaunchCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))
-   [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [**WerUnregisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

已新增的結構：

-   [**WER \_ 執行時間 \_ 例外狀況 \_ 資訊**](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 和 Windows Vista SP1

下列清單摘要說明 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 之 WER 的新功能。

-   您可以設定 WER，如此一來，使用者模式應用程式損毀時，就會收集完整的使用者模式傾印，並將其儲存在本機上 (應用程式，這些應用程式會自行自訂損毀報告，包括 .NET 應用程式) 。 如需詳細資訊，請參閱 [收集 User-Mode](collecting-user-mode-dumps.md)傾印。

## <a name="windows-vista"></a>Windows Vista

下列清單摘要說明適用于 Windows Vista Windows 錯誤報告 (WER) 的新功能：

-   在監視損毀和沒有回應的進程時，已擴充 WER。 WER 包含許多新的非重大事件種類支援，例如效能問題。 這可讓開發人員深入瞭解其客戶所開發之應用程式的體驗。
-   新函式讓開發人員能夠彈性地建立、自訂和提交問題報表。 如需詳細資訊，請參閱 [WER 函數](wer-functions.md)。
-   改良的 [Windows 品質線上服務](https://www.microsoft.com/?ref=go) 讓開發人員能夠存取客戶提交給其應用程式的問題資訊，以及提供解決方案給這些客戶的機制。
-   [應用程式復原和重新](/windows/desktop/Recovery/application-recovery-and-restart-portal)啟動和[重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal)所引進的功能，可讓應用程式在發生重大失敗時自動復原資訊並重新啟動。 開發人員可以在其應用程式中使用這些功能，以大幅改善使用者體驗。
-   **Windows Vista 或 windows 7 上的行動中心的問題報告和解決方案** ，是使用者與 WER 互動的中心位置。 使用者可以檢查是否有新的解決方案、管理報表歷程記錄、查看問題報告的詳細資料，以及管理報告設定，包括讓 WER 自動檢查解決方案，而不會中斷使用者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 錯誤報告](windows-error-reporting.md)
</dt> </dl>

 

 