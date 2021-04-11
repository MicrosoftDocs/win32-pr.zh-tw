---
description: 開發安全的高階網路基礎結構是大部分網路應用程式開發人員的優先考慮。 不過，在考慮完全安全的解決方案時，通常會忽略通訊端安全性，儘管非常重要。
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: 使用 SO_REUSEADDR 和 SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa4024f031102cbd634c235bb39f4c7860e6c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693307"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>使用 \_ REUSEADDR 等 \_ EXCLUSIVEADDRUSE

開發安全的高階網路基礎結構是大部分網路應用程式開發人員的優先考慮。 不過，在考慮完全安全的解決方案時，通常會忽略通訊端安全性，儘管非常重要。 通訊端安全性特別是處理系結至先前由另一個應用程式進程所系結之相同埠的處理常式。 在過去，網路應用程式可能會「劫持」另一個應用程式的埠，而這可能會造成「阻絕服務」攻擊或資料遭竊。

通常，通訊端安全性適用于伺服器端進程。 更具體來說，通訊端安全性適用于接受連線並接收 IP 資料包流量的任何網路應用程式。 這些應用程式通常會系結至知名的埠，且為惡意網路程式碼的常見目標。

用戶端應用程式較不可能是這類攻擊的目標，因為它們較不容易受到影響，但因為大部分的用戶端系結至「暫時」本機埠，而不是靜態「服務」埠。 用戶端網路應用程式應該一律系結至暫時埠 (方法是在呼叫系結函式時，于 *name* 參數所 [](/windows/win32/api/winsock/nf-winsock-bind)指向的 [**SOCKADDR**](sockaddr-2.md)結構中指定埠0，) 除非有吸引人的架構原因。 暫時本機埠是由埠49151以上的埠所組成。 專用服務的大部分伺服器應用程式都會系結至小於或等於埠49151的知名保留埠。 因此，在大部分的應用程式中，用戶端與伺服器應用程式之間的系結要求通常不會發生衝突。

本節說明各種 Microsoft Windows 平臺上的預設安全性層級，以及特定通訊端選項 **\_ REUSEADDR** 和 [ \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) 的影響，以及對網路應用程式安全性的影響。 Windows Server 2003 和更新版本上提供另一項稱為增強通訊端安全性的功能。 這些通訊端選項和增強通訊端安全性的可用性會因不同的 Microsoft 作業系統版本而異，如下表所示。

| 平台            | \_REUSEADDR | \_EXCLUSIVEADDRUSE                  | 增強通訊端安全性 |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | 可用     | 無法使用                         | 無法使用            |
| Windows 98          | 可用     | 無法使用                         | 無法使用            |
| Windows Me          | 可用     | 無法使用                         | 無法使用            |
| Windows NT 4.0      | 可用     | 可在 Service Pack 4 和更新版本中使用 | 無法使用            |
| Windows 2000        | 可用     | 可用                             | 無法使用            |
| Windows XP          | 可用     | 可用                             | 無法使用            |
| Windows Server 2003 | 可用     | 可用                             | 可用                |
| Windows Vista       | 可用     | 可用                             | 可用                |
| Windows Server 2008 | 可用     | 可用                             | 可用                |
| Windows 7and 更新版本  | 可用     | 可用                             | 可用                |

## <a name="using-so_reuseaddr"></a>使用 \_ REUSEADDR

**SO \_ REUSEADDR** 通訊端選項可讓通訊端強制系結至另一個通訊端使用的埠。 第二個通訊端會呼叫 [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) ，並將 *optname* 參數設定為 **\_ REUSEADDR** ，並將 *optval* 參數設定為布林值 **TRUE** ，然後再于與原始通訊端相同的 [**埠上呼叫**](/windows/win32/api/winsock/nf-winsock-bind) 系結。 第二個通訊端成功系結之後，系結至該通訊埠的所有通訊端行為都不確定。 例如，如果相同埠上的所有通訊端都提供 TCP 服務，則透過埠的任何連入 TCP 連線要求都無法保證由正確的通訊端處理，因為行為是不具決定性的。 惡意的程式可以使用 **\_ REUSEADDR** 強制系結已用於標準網路通訊協定服務的通訊端，以拒絕存取這些服務。 使用這個選項不需要任何特殊許可權。

如果用戶端應用程式在伺服器應用程式能夠系結至相同的埠之前系結至埠，則可能會產生問題。 如果伺服器應用程式使用 **\_ REUSEADDR** 通訊端選項強制系結至相同的埠，則系結至該埠的所有通訊端行為都不確定。

這種不具決定性行為的例外狀況是多播通訊端。 如果有兩個通訊端系結至相同的介面和埠，而且是相同多播群組的成員，則會將資料傳遞給這兩個通訊端，而非任意選。

## <a name="using-so_exclusiveaddruse"></a>使用 \_ EXCLUSIVEADDRUSE

在引進 **\_ EXCLUSIVEADDRUSE** 通訊端選項之前，有幾個網路應用程式開發人員可以避免惡意的程式系結到網路應用程式有自己的通訊端系結的埠。 為了解決此安全性問題，Windows 通訊端引進了 **\_ EXCLUSIVEADDRUSE** 通訊端選項，此選項可在 Windows NT 4.0 Service PACK 4 (SP4) 和更新版本中取得。

**\_ EXCLUSIVEADDRUSE** 通訊端選項只可供 Windows XP 及更早版本上的 Administrators 安全性群組成員使用。 本文稍後將討論這項需求在 Windows Server 2003 和更新版本上的變更原因。

**\_ EXCLUSIVEADDRUSE** 選項的設定方式是呼叫 [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt)函數，並將 *optname* 參數設定為 **\_ EXCLUSIVEADDRUSE** ，並在系結器之前，將 *optval* 參數設定為布林值 **TRUE** 。 設定選項之後，後續系 **結呼叫的** 行為會視每個系 [**結呼叫中**](/windows/win32/api/winsock/nf-winsock-bind)指定的網路位址而有所不同。

下表說明當第二個通訊端嘗試系結至使用特定通訊端選項的第一個通訊端之前所系結的位址時，Windows XP 及更早版本中發生的行為。

> [!NOTE]  
> 在下表中，"萬用字元" 代表指定通訊協定 (的萬用字元位址，例如 IPv4 的 "0.0.0.0" 和 IPv6) 的 "：："。 「特定」代表指派了介面的特定 IP 位址。 資料表資料格指出系結是否成功 ( 「成功」 ) ，或針對 [WSAEADDRINUSE](windows-sockets-error-codes-2.md) 錯誤傳回 ( "INUSE" 的錯誤; [WSAEACCES](windows-sockets-error-codes-2.md) 錯誤) 的「存取」。

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>一個</strong></a> 系結呼叫</td>
        <td bgcolor="#C0C0C0" colspan="6">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>二</strong></a> 個系結呼叫</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">預設</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">預設</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

當兩個通訊端系結至相同的埠號碼時，但在不同的明確介面上，就不會發生衝突。 例如，在電腦有兩個 IP 介面10.0.0.1 和10.99.99.99 的情況下，如果第一次呼叫系結的位置是10.0.0.1，且埠設定為5150，**而 \_ EXCLUSIVEADDRUSE** 指定了，則第二次 **呼叫在10.99.99.99 上系**[**結時，**](/windows/win32/api/winsock/nf-winsock-bind)埠也會設定為5150，而未指定任何選項則會成功。 但是，如果第一個通訊端系結至萬用字元位址和埠5150，則任何後續對埠5150的系結呼叫（ **\_ EXCLUSIVEADDRUSE** 設定）都會失敗，並傳回系結作業 **所傳回的** [WSAEADDRINUSE](windows-sockets-error-codes-2.md)或 [WSAEACCES](windows-sockets-error-codes-2.md) 。

在第一次呼叫系 [**結設定為**](/windows/win32/api/winsock/nf-winsock-bind) **\_ REUSEADDR** 或沒有通訊端選項的情況下，第二個系結呼叫將會「劫持」埠，而應用程式將無法判斷 **哪一個套** 接字收到傳送至「共用」埠的特定封包。

除非在呼叫系結函式之前呼叫 **\_ EXCLUSIVEADDRUSE** 通訊端選項，否則呼叫 [**bind**](/windows/win32/api/winsock/nf-winsock-bind)函式的一般應用程式不會配置系結的通訊端來進行獨佔使用。 如果用戶端應用程式在伺服器應用程式系結至相同的埠之前，系結至暫時埠或特定埠，則可能會產生問題。 在呼叫系結函式之前，伺服器應用程式可以使用通訊端上的 **SO \_ REUSEADDR** 通訊端選項， 強制系結至相同的埠，但系結至該埠之所有通訊端的行為則為不定。 如果伺服器應用程式嘗試使用 **\_ EXCLUSIVEADDRUSE** 通訊端選項來獨佔使用埠，要求將會失敗。

相反地，在通訊端關閉之後，就不一定要立即重複使用具有 **\_ EXCLUSIVEADDRUSE** 設定的通訊端。 例如，如果具有 **\_ EXCLUSIVEADDRUSE** 設定的接聽通訊端接受連接，之後再關閉，另一個通訊端也 (另一個通訊端，也就是 **\_ EXCLUSIVEADDRUSE**) 無法系結至與第一個通訊端相同的埠，直到原始連接變成非使用中。

這個問題可能會變得很複雜，因為基礎傳輸通訊協定可能不會終止連接，即使通訊端已關閉也一樣。 即使應用程式關閉通訊端之後，系統仍必須傳輸任何緩衝的資料、將無訊息的中斷連線訊息傳送給對等，並等候對等的適當無訊息中斷連線訊息。 基礎傳輸通訊協定可能永遠不會釋放連接;例如，參與原始連接的對等可能會通告零大小的視窗，或是其他形式的「攻擊」設定。 在這種情況下，用戶端連線會保持作用中狀態，儘管要求關閉它，因為未確認的資料會保留在緩衝區中。

為了避免這種情況，網路應用程式應該透過使用 SD 傳送旗標集呼叫 [**shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) 來確保正常關機 \_ ，然後等候 [**接收**](/windows/win32/api/winsock/nf-winsock-recv) 迴圈，直到透過連接傳回零個位元組為止。 這可確保對等端接收所有資料，並同樣確認其已接收到所有傳輸的資料，以及避免前述的埠重複使用問題。

您可以 \_ 在通訊端上設定 wait socket 選項，以防止埠轉換為「作用中」的等候狀態; 不過，這不建議您這麼做，因為它可能會導致所需的效果，例如重設連接。 例如，如果資料是由對等接收，但是仍維持未認可狀態，而且本機電腦關閉通訊端，並 \_ 在其上進行設定，則兩部電腦之間的連線會重設，且對等會捨棄未認可的資料。 挑選適當的延遲時間很難，因為較小的超時值通常會導致突然中止的連接，而較大的超時值會讓系統容易遭受拒絕服務攻擊 (藉由建立許多連線，以及可能會) 拖延/封鎖應用程式執行緒。 關閉具有非零延遲超時值的通訊端，也可能導致 [**導致 closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) 呼叫封鎖。

## <a name="enhanced-socket-security"></a>增強通訊端安全性

增強通訊端安全性是隨著 Windows Server 2003 的發行而新增的。 在舊版的 Microsoft server 作業系統版本中，預設的通訊端安全性可輕易地讓程式從不受信任的應用程式劫持埠。 在 Windows Server 2003 中，通訊端預設不會處於可共用狀態。 因此，如果應用程式想要允許其他進程重複使用通訊端已系結的埠，則必須特別啟用它。 如果是這種情況，則在埠上呼叫 [**bind**](/windows/win32/api/winsock/nf-winsock-bind) 的第一個通訊端必須在通訊端上設定 **\_ REUSEADDR** 。 這種情況的唯一例外狀況是，當 **第二** 個系結呼叫是由進行原始 **呼叫進行系** 結的相同使用者帳戶執行時。 這個例外狀況僅為了提供回溯相容性而存在。

下表說明當第二個通訊端嘗試系結至使用特定通訊端選項的第一個通訊端之前系結的位址時，在 Windows Server 2003 和更新版本作業系統中發生的行為。

> [!NOTE]
> 在下表中，"萬用字元" 代表指定通訊協定 (的萬用字元位址，例如 IPv4 的 "0.0.0.0" 和 IPv6) 的 "：："。 「特定」代表指派了介面的特定 IP 位址。 資料表資料格指出系結是否成功 ( 「成功」 ) 或針對 [WSAEADDRINUSE](windows-sockets-error-codes-2.md) 錯誤傳回 ( "INUSE" 的錯誤; [WSAEACCES](windows-sockets-error-codes-2.md) 錯誤) 的「存取」。
>
> 另請注意，在這個特定的資料表中，這兩個系結 [**呼叫都是**](/windows/win32/api/winsock/nf-winsock-bind) 在同一個使用者帳戶下進行。

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>一個</strong></a> 系結呼叫</td>
        <td bgcolor="#C0C0C0" colspan="6">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>二</strong></a> 個系結呼叫</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">預設</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">預設</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>Success</td>
        <td>ACCESS</td>
        <td>Success</td>
        <td>INUSE</td>
        <td>Success</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>Success</td>
        <td>INUSE</td>
        <td>Success</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>成功</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>Success</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>Success</td>
        <td>INUSE</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>Success</td>
        <td>INUSE</td>
        <td>Success</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

上表中的幾個專案有提供說明。

例如，如果第一個呼叫端將設定為在特定位址 **\_ EXCLUSIVEADDRUSE** ，而第二個呼叫端 [**嘗試使用相同埠上的萬用字元**](/windows/win32/api/winsock/nf-winsock-bind) 位址來呼叫系結，則第二個系 **結呼叫將** 會成功。 在此特定案例中，第二個呼叫端會系結至所有介面，但第一個呼叫端所系結的特定位址除外。 請注意，此案例的反轉不成立：如果第一個呼叫端設定 **\_ EXCLUSIVEADDRUSE** ，並以萬用字元旗標呼叫系結，則第二個呼叫端就 **無法使用相同****的埠呼叫系** 結。

當通訊端系結呼叫是在不同的使用者帳戶下進行時，就會變更通訊端系結行為。 下表指定當第二個通訊端使用特定通訊端選項和不同的使用者帳戶，嘗試系結先前由第一個通訊端所系結的位址時，在 Windows Server 2003 和更新版本的作業系統中發生的行為。

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>一個</strong></a> 系結呼叫</td>
        <td bgcolor="#C0C0C0" colspan="6">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>二</strong></a> 個系結呼叫</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">預設</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td bgcolor="#C0C0C0">特定</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">預設</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>Success</td>
        <td>INUSE</td>
        <td>Success</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>Success</td>
        <td>INUSE</td>
        <td>成功</td>
        <td>成功</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">萬用字元</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">特定</td>
        <td>Success</td>
        <td>INUSE</td>
        <td>Success</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

請注意，當系 [**結呼叫是在不同**](/windows/win32/api/winsock/nf-winsock-bind) 的使用者帳戶下進行時，預設行為會有所不同。 如果第一個呼叫端未在通訊端上設定任何選項，且系結至萬用字元位址，則第二個呼叫端無法設定 **\_ REUSEADDR** 選項，並成功系結至相同的埠。 未設定任何選項的預設行為也會傳回錯誤。

在 Windows Vista 和更新版本上，可以建立可在 IPv6 和 IPv4 上運作的雙重堆疊通訊端。 當雙重堆疊通訊端系結至萬用字元位址時，會將指定的埠保留在 IPv4 和 IPv6 網路堆疊上，以及與 **\_ REUSEADDR** 建立關聯的檢查和 **\_ EXCLUSIVEADDRUSE** (（如果設定) ）。 這兩個網路堆疊上的這些檢查都必須成功。 例如，如果雙堆疊 TCP 通訊端設定為 **\_ EXCLUSIVEADDRUSE** ，然後嘗試系結至埠5000，則其他 TCP 通訊端之前都不能系結至埠 5000 (萬用字元或特定) 。 在此情況下，如果 IPv4 TCP 通訊端之前系結至埠5000上的回送位址，則雙堆疊通訊端的系 [**結呼叫會**](/windows/win32/api/winsock/nf-winsock-bind) 失敗並出現 [WSAEACCES](windows-sockets-error-codes-2.md)。

## <a name="application-strategies"></a>應用程式策略

開發在通訊端層運作的網路應用程式時，請務必考慮需要的通訊端安全性類型。 用戶端應用程式—連接或傳送資料至服務的應用程式，很少需要任何額外的步驟，因為它們系結至隨機的本機 (暫時) 埠。 如果用戶端需要特定的本機埠系結才能正常運作，則您必須考慮通訊端安全性。

**\_ REUSEADDR** 選項在一般應用程式中，除了將資料傳遞至在相同埠上系結至所有通訊端的多播通訊端之外，還很少使用。 否則，任何設定此通訊端選項的應用程式都應該重新設計，以移除相依性，因為它 eminently 易受限於「通訊端劫持」。 只要 **\_ REUSEADDR** 通訊端選項可以用來在伺服器應用程式中劫持埠，就必須將應用程式視為不安全。

所有伺服器應用程式都必須針對強式通訊端安全性設定 **\_ EXCLUSIVEADDRUSE** 。 它不僅會防止惡意軟體劫持埠，也會指出是否有另一個應用程式系結至要求的埠。 例如，如果另一個進程目前系結至特定介面上的相同埠，則使用 **\_ EXCLUSIVEADDRUSE** 通訊端選項設定的 [**進程在萬用字元位址上系**](/windows/win32/api/winsock/nf-winsock-bind)結的呼叫將會失敗。

最後，即使已在 Windows Server 2003 中改善通訊端安全性，應用程式應該一律設定 **\_ EXCLUSIVEADDRUSE** 通訊端選項，以確保它會系結至進程要求的所有特定介面。 Windows Server 2003 中的通訊端安全性為繼承應用程式增加了更高的安全性層級，但應用程式開發人員仍然必須設計其產品，並牢記安全性的所有層面。
