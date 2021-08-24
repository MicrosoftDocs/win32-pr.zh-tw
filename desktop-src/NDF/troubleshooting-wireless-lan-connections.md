---
title: 無線區域網路連線疑難排解
description: 在此案例中，使用者嘗試連線到無線區域網路，但無法連線。 您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3749b3e3a45ef68cb33b7d3658ca346dd4c6e0a8ba8ea11626573f4da6edfbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801815"
---
# <a name="troubleshooting-wireless-lan-connections"></a>無線區域網路連線疑難排解

在此案例中，使用者嘗試連線到無線區域網路，但無法連線。 您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。

首先，您可以使用 netsh 來啟動追蹤。 輸入 **netsh trace start 情節 = wlan tracefile = wlanwpp。 etl** 會開始追蹤在 wlan 案例下啟用的所有提供者，並將結果儲存至名為 wlanwpp 的檔案。 嘗試連接到無線區域網路之後，輸入 **netsh trace stop** 會終止，並相互關聯追蹤檔案。

然後，您可以在網路監視器中開啟 wlanwpp。 事件會依活動識別碼分組在左窗格中。

![使用網路監視器 (1) 疑難排解無線區域網路連線](images/1wlan.png)

ETL 包含其他已啟用之網路提供者的許多追蹤。 您可以套用篩選器，只顯示與 **WLAN \_ MicrosoftWindowsWlanAutoConfig** 提供者相關的事件。

![使用網路監視器 (2) 的無線區域網路連線疑難排解](images/2wlan.png)

套用篩選之後，您可以檢查 [框架摘要] 中的事件，以找出看起來相關的事件。 選取事件之後，以滑鼠右鍵按一下並指向 [尋找對話]，然後按一下 [NetEvent]。

![使用網路監視器 (3) 疑難排解無線區域網路連線](images/3wlan.png)

展開左窗格中的活動識別碼下的專案，可讓您查看連接嘗試的所有其他相關提供者。 若要查看其他提供者的事件，請在 [**顯示篩選**] 窗格中按一下 [**移除**]，以移除所有篩選。 您可以藉由在畫面格摘要中滾動來分析追蹤，視需要選取其他事件來收集詳細資訊。 在此情況下，[畫面格詳細資料] 窗格會提供失敗原因的資訊，這是因為使用者輸入錯誤的通過金鑰。

 

 




