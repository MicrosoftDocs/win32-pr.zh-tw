---
title: IAgentCharacter 準備
description: IAgentCharacter 準備
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de29c49960bbfd00a6e0d0e9ff1cb055a01cb930c414708fe9144ff0ff4b75af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725324"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter：:P 準備

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

抓取字元的動畫資料。

-   傳回 \_ [確定] 表示作業成功。 當函式傳回時， *pdwReqID* 會包含要求的識別碼。

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

值，表示要載入的動畫資料類型，必須是下列其中一項：



| 值                                                           | 描述                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| **const 不帶正負號簡短****準備 \_ 動畫 = 0;**<br/> | 字元的動畫資料。                              |
| **const 不帶正負號簡短****準備 \_ 狀態 = 1;**<br/>     | 字元的狀態資料。                                  |
| **const 不帶正負號簡短****準備 \_ WAVE = 2**<br/>       | 字元的音效檔 (。WAV 或。LWV 適用于語音輸出的) 。 |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

動畫或狀態的名稱。

動畫名稱是以使用 Microsoft Agent 字元編輯器儲存時為字元所定義的名稱為基礎。

針對狀態，此值可以是下列其中一項：



|                      | 描述                                     |
|----------------------|-------------------------------------------------|
| **"Gesturing"**      | 取得所有 **Gesturing** 狀態動畫。 |
| **"GesturingDown"**  | 取出 **GesturingDown** 動畫。       |
| **"GesturingLeft"**  | 取出 **GesturingLeft** 動畫。       |
| **"GesturingRight"** | 取出 **GesturingRight** 動畫。      |
| **"GesturingUp"**    | 取出 **GesturingUp** 動畫。         |
| **隱匿**         | 取得 **隱藏** 狀態動畫。    |
| **聽覺**        | 取出 **聽力** 狀態動畫。   |
| **閒置**         | 取得所有 **閒置** 狀態動畫。    |
| **"IdlingLevel1"**   | 取得所有 **IdlingLevel1** 動畫。    |
| **"IdlingLevel2"**   | 取得所有 **IdlingLevel2** 動畫。    |
| **"IdlingLevel3"**   | 取得所有 **IdlingLevel3** 動畫。    |
| **欣賞**      | 以取出 **接聽** 狀態動畫。 |
| **移動**         | 取得所有 **移動** 狀態動畫。    |
| **"MovingDown"**     | 取得所有 **移動** 動畫。          |
| **"MovingLeft"**     | 取得所有 **MovingLeft** 動畫。      |
| **"MovingRight"**    | 取得所有 **MovingRight** 動畫。     |
| **"MovingUp"**       | 取得所有 **MovingUp** 動畫。        |
| **男**        | 取得 **顯示** 狀態動畫的。   |
| **說話**       | 取得 **說話** 狀態動畫。  |



 

出於.WAV 檔，請將 *bszName* 設定為的 URL 或檔案規格。WAV 檔。 如果規格未完成，則會將它解讀為相對於 [**Load**](https://www.bing.com/search?q=**Load**) 方法中所使用的規格。

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

布林值，指定伺服器是否將 [**準備**](/windows/desktop/lwef/iagentcharacter--prepare) 要求排在佇列中。 **True** 會將要求排入佇列，並讓其後的任何動畫要求等到它所指定的動畫資料載入為止。 **False** 會以非同步方式抓取動畫資料。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 [**準備**](/windows/desktop/lwef/iagentcharacter--prepare) 要求識別碼之變數的位址。

</dd> </dl>

如果您使用 HTTP 通訊協定載入字元 (。ACF 檔) ，您必須先使用「 [**準備**](/windows/desktop/lwef/iagentcharacter--prepare) 」方法來取出動畫資料，然後才能播放動畫。 如果您使用 UNC 通訊協定將字元載入 (，就不能使用這個方法。ACS 檔案) 。 如果您使用 UNC 通訊協定 ( 載入該字元，您也無法使用「 **準備** 」來抓取字元的 HTTP 資料。) 的 ACS 字元檔。

以 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法取出的動畫或音效資料會儲存在瀏覽器的快取中。 後續的呼叫將會檢查快取，如果動畫資料已經存在，控制項會直接從快取載入資料。 載入之後，您可以使用 [**Play**](/windows/desktop/lwef/iagentcharacter--play) 或 [**朗讀**](/windows/desktop/lwef/iagentcharacter--speak) 方法來播放動畫或音效資料。

您可以使用逗號分隔來指定多個動畫和狀態。 不過，您無法在相同的 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 語句中混合類型。

 

