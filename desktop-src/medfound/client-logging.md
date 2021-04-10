---
description: 用戶端記錄
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: '用戶端記錄 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191082"
---
# <a name="client-logging-microsoft-media-foundation"></a>用戶端記錄 (Microsoft 媒體基礎) 

網路來源支援用戶端記錄，可讓媒體伺服器追蹤連接到該用戶端的用戶端活動。 用戶端記錄檔可讓伺服器記錄連接、轉譯和串流處理統計資料。 這些記錄可供各種案例中的內容提供者使用，例如，用來追蹤媒體伺服器使用量和產生帳單，或根據用戶端網路的速度傳遞適當品質的內容。

記錄檔包含數個用戶端事件專案。 每個記錄專案都包含一些以空格分隔的欄位。 用戶端記錄有兩種 *類型：轉譯* (播放) ，以及接收) 的 *串流* (。 由於內容可以同時播放和串流，因此用戶端可以同時傳送這兩種記錄資料類型的組合。 在某些情況下，相同的會話可以有兩個記錄專案。 例如，啟用 [快速快取] 時，用戶端可以在完成轉譯後，先完成接收資料流程處理的內容。 在此情況下，會在轉譯記錄資料之前傳送串流記錄資料。

用戶端會在用戶端從任何播放狀態變更時，傳送轉譯記錄資料到伺服器 (播放、向前快轉或倒轉) 至非播放狀態 (停止、暫停、串流結束，以及串流) 開頭。 提交轉譯記錄檔的資料時，會直接連接到媒體伺服器或設定的 proxy 伺服器。

如果內容儲存在執行用戶端之電腦上的暫存本機快取檔案中，則用戶端可以從其本機快取讀取檔案，並提交轉譯記錄資料，以指出它已播放內容。 在此情況下，用戶端會從其本機快取讀取檔案、轉譯記錄專案不包含任何網路統計資料，且通訊協定設定為快取。

用戶端會將串流記錄資料傳送到伺服器，以指出用戶端如何接收內容，但不會呈現其轉譯方式。 用戶端可以在用戶端完成轉譯內容之前，傳送串流記錄的時間長度。

本主題不提供所有記錄欄位的相關資訊。 如需完整的參考，請參閱 [Windows Media 記錄資料結構](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84)。

## <a name="configuring-log-fields"></a>設定記錄欄位

媒體基礎可讓用戶端使用屬性來設定網路來源。 應用程式必須在屬性存放區中設定適當的屬性，並將其傳遞給其中一個來源解析程式方法。 來源解析程式會依要求建立網路來源，並開啟與伺服器的連接。 如果連接成功，用戶端會傳送本身的相關資訊。

下表描述的是應用程式可以透過來源解析程式設定的記錄欄位和對應的屬性。 此資訊不會在會話期間變更。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>記錄欄位</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>c-playerid</td>
<td>播放程式的唯一識別。 這項資訊會在連接開始時傳送。 一般來說，這是用戶端的 GUID。 用戶端可以將此資訊傳送到 <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> 屬性中的伺服器。<br/> 用戶端會在連線開始時將此資訊傳送至伺服器。<br/> 範例值： &quot; {c579d042-cecc-11d1-bb31-00a0c9603954}&quot;<br/></td>
</tr>
<tr class="even">
<td>c-playerversion</td>
<td>在連接開始時傳送的播放程式版本號碼。 用戶端可以將此資訊傳送到 <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> 屬性中的伺服器。<br/> 用戶端會在連線開始時將此資訊傳送至伺服器。<br/></td>
</tr>
<tr class="odd">
<td>cs (使用者代理程式) </td>
<td>當播放程式內嵌在瀏覽器中時，所使用的瀏覽器類型。 用戶端可以在 <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> 屬性中設定這個值。<br/> 如果播放程式未內嵌，此欄位會參考產生記錄之用戶端的使用者代理程式。 在此情況下，用戶端必須設定 <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> 屬性。<br/> 用戶端會在連線開始時將此資訊傳送至伺服器。<br/> 範例值： &quot; Mozilla/4.0 _ (相容; _MSIE_4 01; _Windows_98) &quot;<br/></td>
</tr>
<tr class="even">
<td>cs (推薦者) </td>
<td>內嵌播放程式之網頁的 URL (如果內嵌) 。 用戶端可以將此資訊傳送到 <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> 屬性中的伺服器。<br/> 用戶端會在連接結束時將此資訊傳送至伺服器。<br/> 範例值： &quot; https://www.example.microsoft.com&quot ;<br/></td>
</tr>
<tr class="odd">
<td>c-hostexe</td>
<td>若為播放程式記錄檔專案，則為執行的主機程式 ( .exe) 。 例如，瀏覽器中的網頁、Microsoft Visual Basic 小程式或獨立播放機。 用戶端可以將此資訊傳送到 <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> 屬性中的伺服器。<br/> 用戶端會在連接結束時將此資訊傳送至伺服器。<br/> 範例值：<br/>
<ul>
<li>&quot;iexplore.exe&quot;</li>
<li>&quot;myplayer.exe&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td>c-hostexever</td>
<td>主機程式 ( .exe) 版本號碼。 用戶端可以將此資訊傳送到 <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> 屬性中的伺服器。<br/> 用戶端會在連接結束時將此資訊傳送至伺服器。<br/></td>
</tr>
</tbody>
</table>



 

下列程式碼範例顯示用戶端應用程式如何設定網路來源。 此範例會設定 "hostexe" 記錄欄位。


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a>正在抓取網路統計資料

當應用程式呼叫其中一個來源解析程式方法時，它會建立網路來源、設定屬性存放區中指定的屬性，以及開啟媒體伺服器的會話。 除了上一節所述的可設定資訊之外，還會在會話開始、串流期間以及會話關閉時，在伺服器與用戶端之間傳送額外的資料。

應用程式可以使用 **MFNETSOURCE \_ statistics \_ service** 服務識別碼來取得網路統計資料。 若要使用這項服務，應用程式可以呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 函數，以取得在 [**MFNETSOURCE \_ statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) 屬性中包含網路統計資料的屬性存放區。 藉由提供 **MFNETSOURCE \_ STATISTICS \_ id** 列舉中所定義的對應識別碼，即可抓取特定的值。

下列程式碼範例示範如何使用服務來取得用戶端收到的封包數目。


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



下列清單描述 [**MFNETSOURCE \_ 統計資料 \_**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)識別碼中所定義的部分網路統計資料識別碼。



| 網路統計資料識別碼              | Description                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFNETSOURCE \_ AVGBANDWIDTHBPS \_ 識別碼**       | 用戶端連接到伺服器的平均每秒頻寬 (單位) 。 此值會在連接的整個持續時間內計算。                                                              |
| **MFNETSOURCE \_ BUFFERINGCOUNT \_ 識別碼**        | 用戶端播放資料流程時緩衝處理的次數。                                                                                                                                                              |
| **MFNETSOURCE \_ BYTESRECEIVED \_ 識別碼**         | 用戶端從伺服器接收的位元組數目。 此值不包含網路堆疊所新增的任何額外負荷。 使用不同通訊協定來串流處理的相同內容，可能會產生不同的值。 |
| **MFNETSOURCE \_ LINKBANDWIDTH \_ 識別碼**         | 用戶端的最大可用頻寬（以每秒位數為單位）。                                                                                                                                                              |
| **MFNETSOURCE \_ LOSTPACKETS \_ 識別碼**           | 伺服器傳送的封包數，但在傳輸期間遺失，用戶端永遠不會播放。 此值不包含 TCP 或 UDP 封包。                                                                          |
| **MFNETSOURCE \_ RECVPACKETS \_ 識別碼**           | 從伺服器收到的封包數，其值不包括 TCP 或 UDP 封包。                                                                                                                                  |
| **MFNETSOURCE \_ RECOVEREDBYECCPACKETS \_ 識別碼** | 網路中的封包會在用戶端層修復和復原。 此值不包含 TCP 或 UDP 封包。                                                                                          |
| **MFNETSOURCE \_ RESENDSREQUESTED \_ 識別碼**      | 用戶端接收新封包所提出的要求數目。 此值不包含 TCP 或 UDP 封包。                                                                                                          |
| **MFNETSOURCE \_ RECOVEREDPACKETS \_ 識別碼**      | 已復原的封包數，因為它們是透過 UDP 重新傳送。 此值不包含 TCP 或 UDP 封包。 此欄位包含零，除非用戶端使用 UDP 重新傳送。                                        |
| **MFNETSOURCE \_ BUFFERPROGRESS \_ 識別碼**        | 在緩衝處理期間填滿的播放緩衝區百分比。                                                                                                                                                              |
| **MFNETSOURCE \_ 通訊協定 \_ 識別碼**              | 用來存取資料流程的通訊協定。 這可能與用戶端所要求的通訊協定不同。                                                                                                                             |
| **MFNETSOURCE \_ 傳輸 \_ 識別碼**             | 用來傳遞資料流程的傳輸通訊協定。 這必須是 UDP 或 TCP。                                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路來源功能](network-source-features.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

