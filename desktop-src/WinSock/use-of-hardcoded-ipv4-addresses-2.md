---
description: IPv4 的壽命導致硬式編碼許多知名的 IPv4 位址，例如 (127. x. x. x) 的回送位址、整數常數（例如 INADDR \_ 回送）等等。
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: 使用硬式編碼的 IPv4 位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318359"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>使用硬式編碼的 IPv4 位址

IPv4 的壽命導致硬式編碼許多知名的 IPv4 位址，例如 (127. x. x. x) 的回送位址、整數常數（例如 INADDR \_ 回送）等等。 在修改和現有的應用程式以支援 IPv6 或建立與新的 IP 版本無關的程式時，將這些位址進行硬式編碼的做法會帶來明顯的問題。

最佳做法

-   最好的方法是避免硬式編碼任何位址。

要避免的程式碼

-   避免在程式碼中使用硬式編碼的位址。

**從 IPv4 將現有的程式碼基底修改為 IPv4 和 IPv6 互通性**

1.  取得 *Checkv4.exe* 公用程式。 *Checkv4.exe* 公用程式會安裝為 Windows Vista 和更新版本的 Microsoft WINDOWS 軟體開發套件 (SDK) 所發行的一部分。 Windows SDK 可透過 MSDN 訂閱取得，也可以從 Microsoft 網站 (下載 https://msdn.microsoft.com) 。
2.  針對您的程式碼執行 *Checkv4.exe* 公用程式。 瞭解如何在 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)一節中，針對您的檔案執行 *Checkv4.exe* 公用程式。
3.  *Checkv4.exe* 公用程式會警示您是否有 IPv4 位址的通用定義，例如 INADDR \_ 回送。 修改任何使用常值字串的程式碼，以及與通訊協定版本無關的程式碼。
4.  視需要在您的程式碼基底中搜尋其他可能的常值字串。

*Checkv4.exe* 公用程式可協助您尋找常見的常值字串，但您的應用程式可能會有其他特定字串。 您應執行完整的搜尋和測試，以確保您的程式碼基底已 eradicated 與常值字串相關聯的潛在問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于 Windows 通訊端應用程式的 IPv6 指南](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[變更 IPv6 Winsock Html5 應用程式的資料結構](changing-data-structures-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的雙重堆疊通訊端](dual-stack-sockets.md)
</dt> <dt>

[IPv6 Winsock 應用程式的函式呼叫](function-calls-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的消費者介面問題](user-interface-issues-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的基礎通訊協定](underlying-protocols-2.md)
</dt> </dl>

 

 



