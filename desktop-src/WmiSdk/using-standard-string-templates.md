---
description: 許多取用者（例如動態指令碼事件取用者或命令列事件取用者）都具有具有範本限定詞的字串屬性。
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: 使用標準字串範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850751"
---
# <a name="using-standard-string-templates"></a>使用標準字串範本

許多取用者（例如動態指令碼事件取用者或命令列事件取用者）都具有具有 **範本** 限定詞的字串屬性。 這些屬性會使用標準字串範本，來建立由取用者實例和部分事件所設定的字串。 標準字串範本的結構類似于 Microsoft Windows 環境變數規格。

下列清單顯示範本語言的一些範例：

-   字串「此處的部分文字」一律會產生字串「這裡有一些文字」。
-   "% CPUUtilization%" 一律會產生所傳遞事件的 **CPUUtilization** 屬性值。 如果屬性不是字串，則會轉換為字串;例如，"90" 或 "TRUE"。
-   「此處理器的 CPU 使用率目前為% CPUUtilization%」會將事件的 **CPUUtilization** 屬性值內嵌到字串中，產生像是「此處理器的 cpu 使用率目前為90」的內容。
-   "% TargetInstance. CPUUtilization%" 會抓取 **TargetInstance** 屬性之內嵌實例中的 **CPUUtilization** 屬性值。
-   "%%" 會產生單一的% sign。
-   如果要抓取的屬性是陣列，則會以下列格式產生整個陣列：「 (1、5、10、1024) 」。 如果陣列中只有一個元素，則會省略括弧。 如果陣列中沒有任何元素，則會產生 " () "。
-   如果屬性為内嵌物件，則會產生物件的 MOF 表示， (類似 [**IWbemClassObject：： GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) 方法) 。
-   如果要求的是物件內嵌陣列的屬性，則會將它視為具有陣列值的屬性。 例如：% MyEvents. TargetInstance. DriverLetter% 可能會產生 ' ( "C："、"D：" ) ' （如果 MyEvents 是內嵌實例修改事件的陣列）。

## <a name="string-literals"></a>字串常值

成對引號內的所有內容都會被視為字串常值，而且不會被取代。

下列範例顯示編譯器針對「CPU 使用率為% CPUUtilization%」所看到的字串。

``` syntax
CPU utilization is %CPUUtilization%
```

這個字串會產生下列輸出。

``` syntax
CPU utilization is 90
```

另一方面，編譯器會看到「CPU 使用率為 \\ "% CPUUtilization%"」字串，如下所示 \\ 。

``` syntax
CPU utilization is "%CPUUtilization%"
```

這個字串會產生下列輸出，不含變數替代。

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



