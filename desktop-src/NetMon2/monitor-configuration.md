---
description: 您可以使用網路監視器 UI 來設定監視器。 終端使用者可以使用儲存為 HTM 檔案的 HTML 表單，將設定準則傳遞到您安裝的網路監視器 SDK 的下列子資料夾中。
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: '監視 Configuration (網路監視器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b55765774df3be2722c448a1af264162bcd9cdc51ac958cc555bf820d646b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364696"
---
# <a name="monitor-configuration-network-monitor"></a>監視 Configuration (網路監視器) 

您可以使用網路監視器 UI 來設定監視器。 終端使用者可以使用儲存為 HTM 檔案的 HTML 表單，將設定準則傳遞到您安裝的網路監視器 SDK 的下列子資料夾中。

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

當使用者選取 [ **設定監視設定** ] 按鈕時，瀏覽器會產生 html **POST** 訊息，其中包含所有 HTML 表單元素的名稱和值。

當 MCSVC 呼叫 [IMonitor：:D oconfigure](imonitor-doconfigure.md) 方法時， *pConfiguration* 參數會指向 POST 訊息中的資料。 下列範例程式碼提供 POST 訊息資料的範例：

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

這項資料會以長 ASCII 字串的形式傳入。 字串會以什麼嗎的長度和區段的外觀顯示，例如% 3A% 5C 和% 0D% 0A。 這個 peculiarity 是由 HTML 所造成，方法需要將所有可能的 ANSI、DBCS 和 Unicode 字串放入 ASCII 格式。 例如， **DoConfigure** 方法會在每個變數名稱前面插入某些字元，例如連字號 (&) ，以將其識別為變數名稱。 % 3A% 5C 是冒號字元的編碼形式，而% 0D% 0A 表示換行鍵/換行字元。 下列範例程式碼提供由監視器所解釋的 HTML 程式碼。

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



