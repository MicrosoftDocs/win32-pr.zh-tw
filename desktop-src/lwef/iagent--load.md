---
title: IAgent 載入
description: IAgent 載入
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae718ee8c6566de42645c5c02c2efada90ef85ba0136a112bcf0420d18a7b511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725390"
---
# <a name="iagentload"></a>IAgent：： Load

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

將字元載入至 [**字元**](./iagent.md) 集合。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

必須是下列其中一項的 variant 資料類型：



| 值           | 描述                                                                      |
|------------|-----------------------------------------------------------------------|
| *filespec* | 指定字元之定義檔的本機檔案位置。 |
| *URL*      | 字元定義檔的 HTTP 位址。                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

接收字元識別碼之變數的位址。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 [**載入**](load-method.md) 要求識別碼之變數的位址。

</dd> </dl>

您可以從 Microsoft Agent 子目錄中指定相對路徑來載入字元， (不含冒號或開頭斜線字元) 。 這個前置詞會在當地語系化的% windows% msagent 目錄) 中，使用代理程式的字元目錄 (路徑 \\ 。 您也可以使用相對位址，在代理程式的 [字元] 目錄中指定您自己的目錄。

您無法將相同的字元從單一連接載入相同的字元 (一次以上的字元) 。 同樣地，您不能同時從單一連接載入預設字元和其他字元，因為預設字元可能與另一個字元相同。 不過，您可以使用 CoCreateInstance) 建立另一個連接 (，然後載入相同的字元。

Microsoft 代理程式的資料提供者支援載入以單一結構化檔案 ( 儲存的字元資料。ACS) 搭配字元資料和動畫資料，或個別的字元資料 (。ACF) 和動畫 (。ACA) 檔。 一般而言，使用單一結構化。ACS 檔案來載入儲存在本機磁片磁碟機或網路上的字元，並使用傳統的檔案通訊協定（例如 UNC 路徑)  (）進行存取。 使用不同的。ACF 和。當您想要從使用 HTTP 通訊協定存取它們的遠端網站個別載入動畫檔案時，ACA 檔案。

出於.ACS 檔案，使用 [**Load**](load-method.md) 方法可提供存取字元的動畫;載入之後，您可以使用 [**Play**](play-method.md) 方法來建立字元的動畫。 出於.ACF 檔案，您也可以使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來載入動畫資料。 **載入** 方法不支援下載。來自 HTTP 網站的 ACS 檔案。

載入字元不會自動顯示字元。 先使用 [**Show**](show-method.md) 方法讓字元變成可見。

 

 