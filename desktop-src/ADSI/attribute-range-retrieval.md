---
title: 屬性範圍抓取
description: 多重值屬性幾乎可以有任意數目的值。 在許多情況下，它可能很有利，甚至是必要的，以限制查詢所抓取的值範圍。
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- 屬性範圍抓取 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994b1c4535ebce264386b088a53b730e679147f07b4bef9fe99d3a45a63461fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840575"
---
# <a name="attribute-range-retrieval"></a>屬性範圍抓取

多重值屬性幾乎可以有任意數目的值。 在許多情況下，它可能很有利，甚至是必要的，以限制查詢所抓取的值範圍。

範圍抓取需要在單一查詢中要求有限數目的屬性值。 要求的值數目必須小於或等於伺服器支援的最大值數目。 為了減少查詢必須與伺服器聯繫的次數，要求的值數目應盡可能接近此最大值。 若要讓應用程式能夠與所有 Windows 伺服器正常運作，則應該使用最大的1000數目。

屬性查詢的範圍規範需要下列格式：


```C++
range=<low range>-<high range>
```



其中「 &lt; 下限」 &gt; 是要抓取之第一個屬性值的以零為起始的索引，而「 &lt; 高範圍」 &gt; 是要抓取之最後一個屬性值的以零為起始的索引。 「範圍下限」會使用零 &lt; &gt; 來指定第一個專案。 萬用字元 (\*) 可用於「 &lt; 高範圍」 &gt; 以指定所有剩餘的專案。

下表列出範圍規範的範例。



| 範例      | 描述                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| 範圍 = 0-\*   | 取出所有屬性值。 這會受限於伺服器所加諸的限制。                |
| 範圍 = 0-500  | 從1取出至501st 值（含）。                                                |
| 範圍 = 2-3    | 取出第三和第四個值。                                                                  |
| 範圍 = 501-\* | 取出502nd 和所有剩餘的值。 這會受限於伺服器所加諸的限制。 |



 

有幾種不同的方式可捕獲屬性值的範圍。 [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)方法可以在自動化語言或 c + + 中使用。 **IADs. GetInfoEx** 方法是執行範圍抓取的慣用方法。 如需有關使用 **IADs GetInfoEx** 進行範圍抓取的詳細資訊，請參閱 [使用 IADs：： GetInfoEx 來取得範圍的提取](using-iads--getinfoex-for-range-retrieval.md)。

如果使用自動化語言，則 (ADO) 的 ActiveX 目錄物件，可以用來抓取屬性值的範圍。 如需使用 ADO 進行範圍抓取的詳細資訊，請參閱 [使用 ado 進行範圍](using-ado-for-range-retrieval.md)抓取。

如果使用 c + +， [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 和 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面可以用來取得屬性值的範圍。 如需使用 **>idirectorysearch** 和 **IDirectoryObject** 進行範圍抓取的詳細資訊，請參閱 [使用 >idirectorysearch 和 IDirectoryObject 進行範圍](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md)抓取。

 

 




