---
description: 佇列的標記是用來以程式設計的方式啟用已排入佇列的元件。
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: 使用佇列的標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973583"
---
# <a name="using-the-queue-moniker"></a>使用佇列的標記

佇列的標記是用來以程式設計的方式啟用已排入佇列的元件。 佇列的標記需要它收到類別識別碼， (要從其右邊的新的標記叫用之物件的 CLSID) 。 當保留在前面時，新的標記會將 CLSID 傳遞給它左邊的標記。

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

不適用。

## <a name="visual-basic"></a>Visual Basic

GetObject 顯示名稱參數為 "queue：/new："，後面接著程式識別碼或字串形式 GUID （包含或不含大括弧），而伺服器物件要具現化。 下列範例顯示具有佇列名字標記之元件的三個有效啟用：

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a>C/C++

[**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject)顯示名稱參數為 "queue：/new："，後面接著程式識別碼或字串形式 GUID （包含或不含大括弧），以具現化的伺服器物件。 下列範例顯示具有佇列名字標記之元件的三個有效啟用：

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a>備註

佇列的標記會接受選擇性參數，以修改傳送至訊息佇列的訊息屬性。 例如，若要讓訊息佇列的訊息以優先權6傳送，已排入佇列的元件將會依照下列方式啟用：

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

下表列出會影響目的地佇列的佇列名字標記參數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>參數</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>ComputerName</em><br/></td>
<td>指定訊息佇列佇列路徑名稱的電腦名稱稱部分。 訊息佇列的佇列路徑名稱會格式化為<em>ComputerName</em> \ <em>QueueName</em>。 如果未指定，則會使用與已設定之應用程式相關聯的電腦名稱稱。<br/></td>
</tr>
<tr class="even">
<td><em>QueueName</em><br/></td>
<td>指定訊息佇列的佇列名稱。 訊息佇列的佇列路徑名稱會格式化為<em>ComputerName</em> \ <em>QueueName</em>。 如果未指定，則會使用與已設定之應用程式相關聯的佇列名稱。<br/> 若要取得非交易式佇列，您可以先指定佇列名稱，然後建立相同名稱的 COM + 應用程式。<br/></td>
</tr>
<tr class="odd">
<td><em>PathName</em><br/></td>
<td>指定完整訊息佇列的佇列路徑名稱。 如果未指定，則會使用與已設定之應用程式相關聯的訊息佇列佇列路徑名稱。 若要覆寫目的地名稱，可為訊息佇列工作組安裝指定下列格式的路徑：<br/> Queue：<em>PathName</em> = <em>ComputerName</em>\PRI加值稅E $ \ AppName/new： Myproject. CMyClass<br/>
<blockquote>
[!Note]<br />
C 和 Microsoft Visual C++ 程式設計語言都需要兩個反斜線，以表示字串常值中的一個反斜線，例如芝加哥 \\ 薪資。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><em>Msmq.formatname</em><br/></td>
<td>當您將 COM + 應用程式標示為已排入佇列時，COM + 會建立其名稱與應用程式相同的訊息佇列佇列。 該佇列的訊息佇列格式名稱位於與 COM + 應用程式相關聯的 COM + 目錄中。 若要覆寫目的地名稱，可為訊息佇列工作組安裝指定下列格式的格式名稱：<br/> Queue：<em>msmq.formatname</em>= DIRECT = OS：<em>ComputerName</em>\PRI加值稅E $ \ AppName/new： ProgId<br/> 在 Active Directory 設定中， &quot; &quot; 不會將私用 $ 指定為佇列名稱的一部分。 <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 選擇性的佇列名字標記參數是由左至右處理。 請只指定每個關鍵字一次。 指定 *PathName* 參數會取代 *ComputerName* 和 *QueueName* 參數。 特定的 *msmq.formatname* 參數會先刪除 *ComputerName*、 *QueueName* 和 *PathName* 參數的知識。

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>將佇列元件接聽程式與特定私用佇列產生關聯

COM + 佇列的元件接聽程式只能從與標示為已排入佇列的 COM + 應用程式相關聯的佇列接收 當您將 COM + 應用程式標示為已排入佇列時，COM + 會建立其名稱與應用程式相同的訊息佇列佇列。 該佇列的訊息佇列格式名稱位於與 COM + 應用程式相關聯的 COM + 目錄中。 當 COM + 應用程式啟動並標示為接聽時，會啟動 COM + 應用程式進程中的接聽程式，並開啟佇列。 下表列出會影響訊息佇列訊息的佇列名字標記參數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>參數</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>AppSpecific</em><br/></td>
<td>指定不帶正負號的整數，例如 AppSpecific = 12345。<br/></td>
</tr>
<tr class="even">
<td><em>AuthLevel</em><br/></td>
<td>指定訊息驗證層級。 已驗證的訊息會經過數位簽署，而且需要憑證給傳送訊息的使用者。 可接受的值：<br/>
<ul>
<li>MQMSG_AUTH_LEVEL_NONE，0</li>
<li>MQMSG_AUTH_LEVEL_ALWAYS，1</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>傳遞</em><br/></td>
<td>指定訊息傳遞選項。 交易式佇列會忽略此值。 可接受的值：<br/>
<ul>
<li>MQMSG_DELIVERY_EXPRESS，0</li>
<li>MQMSG_DELIVERY_RECOVERABLE，1</li>
</ul></td>
</tr>
<tr class="even">
<td><em>EncryptAlgorithm</em><br/></td>
<td>指定訊息佇列用來加密和解密訊息的加密演算法。 可接受的值：<br/>
<ul>
<li>CALG_RC2，CALG_RC4</li>
<li><em>EncryptAlgorithm</em>訊息佇列可以接受的任何整數值。</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>HashAlgorithm</em><br/></td>
<td>指定密碼編譯雜湊函數。 可接受的值：<br/>
<ul>
<li>CALG_MD2，CALG_MD4，CALG_MD5，CALG_SHA，CALG_SHA1，CALG_MAC，CALG_SSL3_SHAMD5，CALG_HMAC，CALG_TLS1PRF</li>
<li><em>HashAlgorithm</em>訊息佇列可以接受的任何整數值。</li>
</ul></td>
</tr>
<tr class="even">
<td>日誌<br/></td>
<td>指定訊息佇列的訊息日誌選項。 可接受的值：<br/>
<ul>
<li>MQMSG_JOURNAL_NONE，0</li>
<li>MQMSG_DEADLETTER，1</li>
<li>MQMSG_JOURNAL，2</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>標籤</em><br/></td>
<td>指定最多 MQ_MAX_MSG_LABEL_LEN 個字元的訊息標籤字串。 <br/></td>
</tr>
<tr class="even">
<td><em>MaxTimeToReachQueue</em><br/></td>
<td>指定訊息抵達佇列的最長時間（以秒為單位）。 <br/> 可接受的值：<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>秒數</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>MaxTimeToReceive</em><br/></td>
<td>指定目標應用程式接收訊息的最長時間（以秒為單位）。 可接受的值：<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>秒數</li>
</ul></td>
</tr>
<tr class="even">
<td><em>優先順序</em><br/></td>
<td>指定允許的訊息佇列值內的訊息優先權層級。<br/> 可接受的值：<br/>
<ul>
<li>MQ_MIN_PRIORITY，0</li>
<li>MQ_MAX_PRIORITY，7</li>
<li>MQ_DEFAULT_PRIORITY，3</li>
<li>介於0和7之間的數位</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>PrivLevel</em><br/></td>
<td>指定用來加密訊息的隱私權等級。<br/> 可接受的值：<br/>
<ul>
<li>MQMSG_PRIV_LEVEL_NONE、無、0</li>
<li>MQMSG_PRIV_LEVEL_BODY，主體，</li>
<li>MQMSG_PRIV_LEVEL_BODY_BASE，BODY_BASE，1</li>
<li>MQMSG_PRIV_LEVEL_BODY_ENHANCED、BODY_ENHANCED、3</li>
</ul></td>
</tr>
<tr class="even">
<td><em>追蹤</em><br/></td>
<td>指定追蹤訊息佇列路由中使用的追蹤選項。<br/> 可接受的值：<br/>
<ul>
<li>MQMSG_TRACE_NONE，0</li>
<li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE，1</li>
</ul></td>
</tr>
</tbody>
</table>



 

您可以使用 COM 物件來取得一組完整的 COM + 系統管理 SDK 函數。 這可讓任何程式視需要啟動和停止 COM + 應用程式。

> [!Note]  
> 當 COM + 應用程式啟動時，它是正在執行的應用程式，而不是應用程式內的個別元件。 如果應用程式呼叫未排入佇列的元件，則會啟動包含元件的 COM + 應用程式。 如果已啟用 [接聽程式] 核取方塊，接聽程式也會啟動，並開始處理已排入佇列之元件的訊息。 雖然已排入佇列的元件服務可以透過這種方式來啟動，但如果您將已排入佇列和未排入佇列的元件封裝成單一的 COM + 應用程式，請確定您確實想要在執行未排入佇列的元件時，將佇列的元件啟動。 如果不是這種情況，請將已排入佇列的元件封裝成與其他元件不同的 COM + 應用程式。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟用元件佇列](activating-component-queues.md)
</dt> </dl>

 

 




