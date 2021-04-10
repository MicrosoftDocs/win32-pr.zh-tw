---
title: 網路延遲和輸送量
description: 遠端程序呼叫 (RPC) 的網路延遲和輸送量。
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183992"
---
# <a name="network-latency-and-throughput"></a>網路延遲和輸送量

有三個主要問題與網路的最佳使用有關：

-   網路延遲
-   網路飽和
-   封包處理的含意

本節介紹需要使用 RPC 的程式設計工作，然後設計兩個解決方案：其中一個撰寫不佳，而且撰寫了一個妥善的解決方案。 這兩個解決方案都會經過檢查，而且會討論其對網路效能的影響。

在討論這兩種解決方案之前，接下來的幾節將討論和說明網路相關的效能問題。

## <a name="network-latency"></a>網路延遲

網路頻寬和網路延遲是不同的詞彙。 頻寬高的網路不保證會有低延遲。 例如，雖然輸送量很高，但往返附屬連結的網路路徑通常會有高延遲。 網路來回行程若有五個或更多秒的延遲，並不罕見。 這種延遲的含意如下：設計用來傳送要求、等候回復、傳送另一個要求、等候另一個回復等等的應用程式，將會針對每個封包交換等候至少五秒，不論伺服器的速度有多快。 儘管電腦的速度越來越快，衛星傳輸和網路媒體仍以光線的速度為基礎，這通常會維持不變。 因此，不太可能發生現有附屬網路的延遲改進。

## <a name="network-saturation"></a>網路飽和

許多網路中都會出現一些飽和度。 最簡單的網路變得較慢的數據機連結，例如標準的56k 類比數據機。 不過，在單一區段上具有許多電腦的乙太網路連結也會變成飽和。 這同樣適用于具有低頻寬或非負載過重連結的廣域網路，例如可處理有限流量數量的路由器或交換器。 在這種情況下，如果網路傳送的封包數超過其最弱的連結可處理的數量，則會捨棄封包。 為了避免擁塞，當偵測到捨棄的封包時，Windows TCP 堆疊會相應減少，進而導致顯著的延遲。

## <a name="packet-processing-implications"></a>封包處理的含意

當程式是針對較高層級的環境開發，例如 RPC、COM 甚至 Windows 通訊端時，開發人員通常會忘記在幕後針對每個已傳送或已接收的封包進行多少工作。 當封包從網路抵達時，電腦就會提供網路卡的插斷。 然後， (DPC) 的延遲程序呼叫已排入佇列，而且必須透過驅動程式來進行。 如果使用任何形式的安全性，封包可能必須解密，或是經過驗證的密碼編譯雜湊。 您也必須在每個狀態執行一些有效性檢查。 只有當封包抵達最終目的地：伺服器程式碼時。 傳送許多小型資料區塊會導致每個小型資料區塊的封包處理負荷。 傳送一個大型資料區塊通常會耗用整個系統的 CPU 時間，即使與一個大型區塊相較之下，相較于一個大型區塊的執行成本，也可能與伺服器應用程式相同。

## <a name="example-1-a-poorly-designed-rpc-server"></a>範例1：設計不良的 RPC 伺服器

想像一下必須存取遠端檔案的應用程式，而手上的工作是設計用來操作遠端檔案的 RPC 介面。 最簡單的解決方案是為本機檔案鏡像 studio 檔案常式。 這樣做可能會導致好像很的乾淨且熟悉的介面。 以下是簡短的 .idl 檔：

``` syntax
typedef [context_handle] void *remote_file;
... .
interface remote_file
{
    remote_file remote_fopen(file_name);
    void remote_fclose(remote_file ...);
    size_t remote_fread(void *, size_t, size_t, remote_file ...);
    size_t remote_fwrite(const void *, size_t, size_t, remote_file ...);
    size_t remote_fseek(remote_file ..., long, int);
}
```

這看起來很簡潔，但其實這是一項符合時間的配方，可應付效能嚴重損壞。 相較于熱門的意見，遠端程序呼叫並不只是在呼叫端和被呼叫端之間使用網路的本機程序呼叫。

若要查看此食譜如何消耗效能，請考慮2K 檔案，其中20個位元組從一開始讀取，最後20個位元組，並查看其執行方式。 在用戶端上，為了簡潔) 起見，已省略許多程式碼路徑來進行下列呼叫 (：

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

現在假設伺服器是透過附屬連結與用戶端分開，而且有五秒的來回行程時間。 每個呼叫都必須等待回應，才能繼續進行，這表示執行此25秒的最小值是絕對最小值。 考慮我們只抓取40個位元組，這會 outrageously 效能變慢。 此應用程式的客戶會極了。

現在假設網路已飽和，因為在網路路徑中某個位置的路由器容量會過重。 如果我們沒有安全性，則此設計會強制路由器處理至少10個封包， (每個要求各一個，並針對每個回復) 。 這也不是好事。

這種設計也會強制服務器接收五封包，並傳送五封包。 同樣地，這不是很好的執行。

## <a name="example-2-a-better-designed-rpc-server"></a>範例2：設計更好的 RPC 伺服器

讓我們重新設計範例1中所討論的介面，並查看我們是否能讓它更好。 要注意的是，讓此伺服器真的很好，需要知道指定檔案的使用模式：此範例不會假設這類知識。 因此，這是較佳設計的 RPC 伺服器，但不是以最佳方式設計的 RPC 伺服器。

此範例中的概念是盡可能將許多遠端作業折迭成一項作業。 第一次嘗試如下所示：

``` syntax
typedef [context_handle] void *remote_file;
typedef struct
{
    long position;
    int origin;
} remote_seek_instruction;
... .
interface remote_file
{
    remote_fread(file_name, void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
    size_t remote_fwrite(file_name, const void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
}
```

此範例會將所有作業折迭為讀取和寫入，以允許在相同的作業上選擇性開啟，以及選擇性的關閉和搜尋。

以縮寫形式寫入的相同作業順序如下所示：

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

當考慮到設計更好的 RPC 伺服器時，在第二次呼叫時，伺服器會檢查 *檔案名 \_* 是否為 **Null**，並在 rfp 中使用儲存的開啟檔案。 接著，它會看到搜尋指示，並在讀取前將檔案指標放在結尾之前的20個位元組。 完成時，它會辨識 **CloseWhenDone** 旗標設定為 **TRUE**，並將關閉該檔案，然後關閉 rfp。

在高延遲的網路上，此較佳的版本需要10秒鐘的時間，以加快 (2.5 倍的) ，而且只需要處理四封封包;從伺服器接收兩次，而從伺服器傳送兩次。 相較于其他所有專案，伺服器執行的額外 *ifs* 和取消封送也可說是微不足道。

如果正確指定了因果順序，介面甚至可以是非同步，而這兩個呼叫可以平行傳送。 當使用順序時，呼叫仍會依序分派，這表示在高延遲的網路上，即使傳送和接收的封包數量相同，也只會遷就五秒的延遲。

我們可以建立一個採用結構陣列的方法（陣列的每個成員分別描述特定的檔案作業），以進一步折迭這項作業;散佈/收集 i/o 的遠端變化。 只要每項作業的結果不需要在用戶端上進行進一步的處理，此方法就會隨之付費。換句話說，應用程式將會讀取最後20個位元組，而不考慮前20個位元組的讀取量。

但是，如果必須在讀取後的前20個位元組執行某些處理，以判斷下一項作業，則將所有專案折迭至一項作業將無法運作 (至少在所有情況下都不會) 。 RPC 的簡潔性是，應用程式可以在介面中同時有這兩種方法，並視需要呼叫這兩種方法。

一般而言，在涉及網路時，最好盡可能將多個呼叫合併到單一呼叫。 如果應用程式有兩個獨立的活動，請使用非同步作業，並讓它們平行執行。 基本上，讓管線保持完整。

 

 




