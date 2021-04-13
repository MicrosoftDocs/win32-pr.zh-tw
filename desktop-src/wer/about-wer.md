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
# <a name="about-wer"></a>關於 WER

Windows 錯誤報告 (WER) 是一種彈性的事件型回饋基礎結構，其設計目的是要收集 Windows 可以偵測的硬體和軟體問題的相關資訊、向 Microsoft 回報資訊，以及為使用者提供任何可用的解決方案。 如需有關 WER 改進的詳細資訊，請參閱 [wer 的新功能](what-s-new-in-wer.md)。

從 Windows Vista 開始，Windows 預設會提供損毀、無回應和核心錯誤報表，而不需要變更您的應用程式。 應用程式會改為使用 WER API，針對與損毀、非回應或核心錯誤無關的應用程式特定問題，產生錯誤報表。

若要產生應用程式特定問題的錯誤報表，應用程式必須使用一些稱為 *報表參數* 的基本資訊來建立問題的簡短描述。 報表參數包括應用程式名稱、應用程式版本、模組名稱、模組版本和錯誤碼等資訊。 這些報表參數的組合說明了唯一的問題。

當 WER 檢查解決方案時，它會先詢問問題是否已經知道，以在 Microsoft 與 WER 伺服器通訊。 伺服器會以下列其中一種方式回應：

-   如果已知問題和解決方法，伺服器會將解決方案傳送給用戶端電腦，而 WER 會將這項資訊顯示給使用者。
-   如果問題正在調查中，伺服器可能會傳送指出狀態的回應。 如果開發人員需要更多的資訊來解決問題，伺服器會從 WER 要求其他資訊，而 WER 會要求使用者提供傳送此資訊的許可權。
-   如果問題不明，伺服器會建立一個問題，讓開發人員調查並傳送表示狀態的回應給 WER。

使用此程式時，如果需要，則 WER 會收集更多的資訊，或將方案傳送給使用者（如果有的話）。 在 Windows Vista 中，使用者可以隨時前往 **問題報告和解決方案** 來查看可用的解決方案、檢查是否有新的解決方案可供使用，或管理其他的 WER 報告和設定。 在 Windows 7 上， **問題報告和解決方案** 現在稱為「 **動作中心**」。 按一下 [ **開始** ]，在 [ **搜尋程式及** 檔案] 中輸入 "view"，然後選取 [ **查看所有問題報告**]、[ **查看可靠性歷程記錄**] 或 [ **查看問題的解決方案**]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 錯誤報告](windows-error-reporting.md)
</dt> </dl>

 

 




