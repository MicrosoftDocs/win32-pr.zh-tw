---
description: '簡介 (Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊) '
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: '簡介 (Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb61f41644f74e22f8e4117854db90cc1bea025b3ff5399819eaa580eee39f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994918"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>簡介 (Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊) 

在世界各地，許多公司都採用 Windows 7，因為其企業功能和能力。 IT 部門也會改變其長期平臺需要支援新式桌面的方式。 Windows 7 作業系統可協助使用者在任何地方保持生產力、增強安全性和控制，以及簡化整個組織的桌面管理，以協助降低擁有權總成本。 Windows 7 也包含以標準為基礎的新式瀏覽器，Windows Internet Explorer 8，可提供改善的安全性和增強的流覽功能。 這兩個平臺可提高 IT 效率，並且強化組織的靈活性和安全性。

不過，遷移至新的作業系統會產生獨特的挑戰，主要是需要支援舊版 web 應用程式。 公司可能會有針對舊版 Windows Internet Explorer 所建立的應用程式，例如 Windows Internet Explorer 7 或 Microsoft Internet Explorer 6。 這些 web 應用程式可能會遇到 Internet Explorer 8 的相容性問題。 此外 Internet Explorer 6 原本就不會在 Windows 7 上執行，而且 Windows 不支援同時執行兩個版本的 Internet Explorer。 如需詳細資訊，請參閱 Microsoft 知識庫文章：「[不支援在單一作業系統上執行多個版本的 Internet Explorer](https://support.microsoft.com/kb/2020599)。」

許多公司仍然使用以 Internet Explorer 6 為基礎的 web 應用程式，這些應用程式是過去十年來建立和自訂的。 打算部署 Windows 7 的公司必須有全方位的策略和執行計畫，才能將舊版 web 應用程式遷移至 Internet Explorer 8。 本檔詳細說明 Internet Explorer 8 相容性問題、討論如何遷移 web 應用程式，以及引進相關的工具和程式。

Internet Explorer 8 版著重于三個主要主題：

-   提供與其他瀏覽器和現有網站相容性的真實世界互通性。
-   使用內建的開發人員工具，更快且更輕鬆地進行 網頁程式開發。
-   透過將使用者連線到創新 web 服務的新瀏覽器功能，讓您可以在網頁以外的範圍提供經驗。

除了標準支援的顯著進展之外，Internet Explorer 8 還包含開發人員的額外平臺投資。 Internet Explorer 8 改善許多 Internet Explorer 子系統的效能，例如 HTML 剖析器、級聯樣式表 (CSS) 規則處理、標記樹操作、JavaScript 剖析器、垃圾收集行程執行時間，以及記憶體管理。 其他開發人員投資包括：

-   CSS 2.1：您可以撰寫您的頁面一次，讓它們更輕鬆地在不同的瀏覽器之間轉譯，因為 Internet Explorer 8 完全支援 CSS 2.1 規格。
-   檔物件模型 (DOM) 和 HTML 4.01 改良功能： Internet Explorer 8 提供額外的 HTML 4.01 增強功能和完整的 CSS 2.1 合規性。 Internet Explorer 8 也可修正許多跨瀏覽器的不一致。 例如，get/set/remove 屬性的執行現在可與其他瀏覽器互通，並以非同步 JavaScript 和 XML (AJAX) 設計模式來改善效能。
-   新興標準： Internet Explorer 8 納入未來的標準，例如 W3C's HTML5 Draft DOM 儲存體 standard、Web 應用程式工作群組的選取器 API，以及 ECMAScript 3.1 背書語法。
-   AJAX 應用程式的新流覽功能：您可以從 AJAX 應用程式更新瀏覽器的上一頁和 forward 導覽堆疊和位址列，讓這些瀏覽器功能在您的應用程式中正確運作。
-   Acid2： Internet Explorer 8 會正確轉譯 Acid2 browser 測試。
-   相容性： Internet Explorer 8 包含更符合標準的版面配置引擎，可讓您建立多個瀏覽器的標準網站。 若要更輕鬆地將您的網站遷移至符合標準規範的新配置引擎，Internet Explorer 8 可讓您藉由將簡單的 **中繼** 元素插入您的程式碼，或在您的伺服器上新增單一 HTTP 標頭，來使用 Internet Explorer 7 的版面配置引擎。
-   開發人員工具： Internet Explorer (中的開發人員工具，您可以按 F12) 鍵來存取這些工具，讓您快速地在視覺效果環境中偵測 HTML、CSS 和 JavaScript 程式碼。 這些工具會直接包含在 Internet Explorer 8 中，並具有擴充的功能，包括在您流覽網頁時，選擇要使用哪一個應用程式的王小姐選項。 您可以快速找出並解決問題，因為工具提供至 DOM 的深度見解。
-   如需 Internet Explorer 8 的新功能和增強功能的詳細資訊，請參閱 MSDN Library 中 [Internet Explorer 8 的新](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) 功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在遷移至 Internet Explorer 8 時解決應用程式相容性問題](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



