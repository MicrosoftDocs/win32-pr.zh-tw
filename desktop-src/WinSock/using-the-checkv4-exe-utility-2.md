---
description: 使用 Checkv4.exe 公用程式來修改您的 IPv4 應用程式，以支援 IPv6。
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: 使用 Checkv4.exe 公用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3377e62e5a874910f91857b6c5dc64df3c3cccddbe405ab6ca199241038a4ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121062"
---
# <a name="using-the-checkv4exe-utility"></a>使用 Checkv4.exe 公用程式

> [!IMPORTANT]
> *Checkv4.exe* 公用程式不會隨附于 Windows 8 的 Windows 軟體開發套件 (SDK) ，也不會隨附于較新版本的 Windows SDK。

*Checkv4.exe* 公用程式是設計來提供程式碼移植夥伴;此公用程式會逐步引導您使用您的程式碼基底、找出潛在的問題，或反白顯示可受益于支援 IPv6 的函式或結構的程式碼，並提出建議。 使用 Checkv4.exe 公用程式，修改現有 IPv4 應用程式以支援 IPv6 的工作會變得更容易。

*Checkv4.exe* 公用程式會安裝為 Windows Vista 和更新版本 sdk) 發行的 Microsoft Windows 軟體開發套件 (sdk， (Windows 軟體開發套件 () SDK Windows 8。

較舊版本的 *Checkv4.exe* 公用程式具有更有限的功能，也提供為 Windows 2000 的舊版 Microsoft IPv6 技術預覽的一部分。

下列各節說明如何使用 *Checkv4.exe* 公用程式，然後說明修改現有 IPv4 應用程式以支援 IPv6 的建議方法。

## <a name="recommendations-for-running-checkv4exe"></a>執行 Checkv4.exe 的建議

-   *Checkv4.exe* 公用程式很簡單。 只要在命令列上執行 *Checkv4.exe* ，並以您想要檢查的檔案名作為參數。 *Checkv4.exe* 會剖析檔案，並提供該檔案中的 IPv6 移植問題所在的意見反應。 將 *Checkv4.exe* 放入電腦的路徑，可讓您更輕鬆地從原始程式碼目錄結構中的任何位置執行 *Checkv4.exe* 公用程式。 例如，將 *Checkv4.exe* 放入% windir%，可讓您從電腦上的任何目錄啟動 *Checkv4.exe* ，而不包含其路徑。

-   在命令提示字元中發出下列命令，以剖析 Simplec 檔案：

    **Checkv4 simplec c。**

    請注意， *Checkv4.exe* 公用程式所做的某些建議只需要最新版本的 *Ws2tcpip .h* 標頭檔中的結構，例如 **SOCKADDR \_ IN6** 結構。 這些標頭檔包含在 Windows Vista 和更新版本中發行的 Windows SDK。 這些標頭檔也包含在舊版平臺軟體發展工具組中， (SDK) 為 Windows Server 2003 發行。 這些標頭檔也會包含在 MSDN 訂用帳戶或下載中。

    下列螢幕擷取畫面顯示在附錄 A 中所包含的 Simplec 檔案上使用 *Checkv4.exe* 公用程式的結果：

    ![checkv4.exe 報告 simplec 中的 ipv6 不相容問題](images/portingguide002.jpg)

    下列螢幕擷取畫面顯示在 Simples 上使用 *Checkv4.exe* 公用程式的結果，也包含在附錄 A：

    ![checkv4.exe 報告 simples 中的 ipv6 不相容問題](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>應用程式修改程式：要從何處著手

有一個建議的程式，與將 IPv6 功能新增至應用程式相關聯。 遵循此順序會很有説明，因為它可讓開發人員確保修改現有 IPv4 應用程式所需的所有步驟都是採用 IPv6。 某些應用程式可能需要更廣泛地注意其中一個序列;例如，系統服務可能會有比圖形檔案傳輸程式 (FTP) 更少的使用者介面問題。

**修改 IPv4 應用程式以支援 IPv6**

1.  修正結構和宣告，以啟用 IPv6 和 IPv4 相容性。
2.  修改函式呼叫以利用具備 IPv6 功能的函式，例如 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 函數。
3.  請參閱原始程式碼，以使用硬式編碼的 IPv4 位址，例如回送位址，或使用其他常值字串。
4.  執行完整的使用者介面檢查，包括資訊對話方塊。 請考慮它是否適用于已啟用 IPv6 的應用程式，以指定或提供以 IP 位址為基礎的資訊。
5.  判斷您的應用程式是否依賴基礎通訊協定（例如 RPC），並進行適當的程式設計變更來處理 IPv6 位址。
6.  在 Windows XP 和更新版本上編譯應用程式時，請使用編譯時期旗標 IPV6STRICT。 此旗標會導致不相容的程式碼編譯失敗，如下所示：

    Windows具有不相容程式碼的通訊端1.x 應用程式無法進行編譯，並傳回錯誤訊息「需要的 WINSOCK2」。

    Windows具有不相容程式碼的 socket 2.x 應用程式會導致每個不相容程式碼實例的編譯時間錯誤。 系統會以下列格式產生錯誤訊息：

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    例如：

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



