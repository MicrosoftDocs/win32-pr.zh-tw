---
description: Internet Explorer 8-使用者代理程式字串
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-使用者代理程式字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94d60930466b7243ad6ecc2b2d8d9c799e0e3da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088236"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8-使用者代理程式字串

## <a name="affected-platforms"></a>受影響的平臺

 **客戶** 端-windows XP、windows Vista、windows 7  
**伺服器** -windows server 2003、windows server 2008、windows Server 2008 R2  










## <a name="feature-impact"></a>功能影響

**嚴重性** -中  
**頻率** -高  











## <a name="description"></a>Description

使用者代理字串是 Internet Explorer 的識別碼，可提供其版本和其他屬性的相關資料給 web 伺服器。 許多 web 應用程式都依賴和操作 IE 使用者代理字串。 這樣做並相依于較早的版本號碼將會受到影響。 使用者代理程式字串現在包含字串 ' Trident/4.0 '，以便在 Internet Explorer 7 相容性檢視中執行時，允許 Internet Explorer 7 的使用者代理程式字串和 Internet Explorer 8 的使用者代理程式字串之間的差異。 如需詳細資訊，請參閱瞭解使用者代理字串。

## <a name="manifestation-of-impact"></a>影響的表現

有兩個受影響的區域：

-   明確檢查使用者代理程式字串並不支援 Internet Explorer 8 使用者代理程式字串的網頁可能無法正常執行。 在大部分的情況下，這表示頁面將會封鎖使用者嘗試存取的內容，或顯示不正確或格式不正確的內容。
-   裝載 Trident (查看裝載和重複使用) 的應用程式，會使用 Web 選擇性元件預設為 Internet Explorer 7，但無法存取 Internet Explorer 8 功能。

## <a name="solution"></a>解決方法

確定您的應用程式在使用者代理程式字串中正確處理新的 ' MSIE 8.0 ' 版本。 您也可以根據 Internet Explorer 7，加入宣告這些應用程式的 Internet Explorer 7 相容性檢視。 這可以透過中繼標記來完成。 如需詳細資訊，請參閱瞭解使用者代理字串的討論。

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

-   在 Windows Vista 或 Windows XP 的 Internet Explorer 8 環境中執行您的應用程式和網頁，以確保它們會以預期的方式運作。
-   或者，您可以使用應用程式相容性工具組所提供的 Internet Explorer 相容性測試控管 (IECTT)  (ACT) 找出因安全性功能更新而可能發生的任何問題。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [瞭解使用者代理程式字串](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Internet Explorer 8 User-Agent 字串](/archive/blogs/ie/)
-   [使用者代理程式字串和版本向量](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [裝載和重複使用](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [應用程式相容性工具組下載](/windows-hardware/get-started/adk-install)
-   [已知 Internet Explorer 安全性功能問題](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
