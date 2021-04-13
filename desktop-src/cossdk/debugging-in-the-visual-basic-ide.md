---
description: 使用 Microsoft Visual Basic 整合式開發環境 (IDE) 進行偵錯工具，可讓 Visual Basic 開發人員存取熟悉的工具和易用的工具。
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Visual Basic IDE 中的調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385896"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Visual Basic IDE 中的調試

使用 Microsoft Visual Basic 整合式開發環境 (IDE) 進行偵錯工具，可讓 Visual Basic 開發人員存取熟悉的工具和易用的工具。 雖然許多元件最終需要使用 Microsoft Visual C++ 環境進行更完整的調試，但是有一項策略可能會先使用 Visual Basic 盡可能地進行最多的功能偵測。 例如，您可能會想要使用 Visual Basic IDE，以在您尚未進行多執行緒處理、元件追蹤、遠端呼叫或進程隔離時，于 COM + 內進行的偵錯工具。

一般來說，當您使用 Visual Basic 環境進行偵錯工具時，您必須先編譯專案，並將 DLL 加入至 COM + 應用程式。 然後，您可以設定專案的二進位相容性、參考您所建立的 DLL，然後啟動專案開始進行偵錯工具。

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>在 Visual Basic 環境中進行偵錯工具的一般指導方針

-   當您使用 Visual Basic 進行偵錯工具時，COM + 會將 Visual Basic 元件視為屬於程式庫應用程式，即使元件已註冊為屬於伺服器應用程式。 因為它是以程式庫應用程式的形式執行，所以 [元件服務] 系統管理工具中的元件圖示不會在元件進行調試時旋轉。
-   如果您在偵錯工具期間變更元件的交易屬性，或變更需要 Visual Basic 產生新 CLSID 或 ProgID 的原始程式碼，請務必刪除並重新安裝包含該元件的 COM + 應用程式。 如果您已設定元件的二進位相容性，系統會警告您已發生變更。

## <a name="notes-on-debugging-within-a-com-application"></a>COM + 應用程式內的偵錯工具注意事項

-   如果您在元件介面、類別名稱、專案名稱、交易式支援或其他設定的 Visual Basic IDE 中進行變更，[元件服務] explorer 中的設定資料與在 Visual Basic 偵錯工具中執行的實際設定之間可能不相符。
-   當您在應用程式中對元件進行偵錯工具時，請勿匯出 COM + 應用程式。 COM + 會將 Visual Basic 開發環境視為元件。
-   如果您在偵錯工具外部執行元件，然後決定開始進行偵錯工具，則當您在偵錯工具中啟動元件的實例時，該元件的實例可能仍在 COM + 中執行。 COM + 會偵測到此狀況，並嘗試以無訊息方式關閉它所控制的實例。 若要避免這個問題，請先從 [元件服務] 系統管理工具移除元件，再開始進行調試。

**使用 Visual Basic 環境進行調試**

1.  在 Visual Basic 中開啟元件專案。

2.  編譯您的元件，然後將專案中的二進位相容性設定為已編譯的元件。

3.  將 MTSTransactionMode 屬性設定為 0-NotAnMTSObject 以外的值。 當您啟動專案時，此設定會提示 Visual Basic 在 COM + 內啟動您的元件。

4.  從 [ **專案** ] 功能表按一下 [ **屬性**]，然後在 [ **調試** 程式] 索引標籤上輸入啟動程式。啟動程式是呼叫此元件的用戶端可執行檔。

    > [!Note]  
    > 啟動程式必須在您要進行調試的元件的本機上。

     

5.  按 F5 鍵開始對元件進行調試。

按下 F5 之後，Visual Basic 會啟動用戶端應用程式，並在 [偵測] 模式中執行該元件。 您可以將中斷點放置在元件的程式碼中，並在變數上設定監看式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + Visual Basic 支援與 MTS 對比](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[已編譯的 Visual Basic 元件的調試](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



