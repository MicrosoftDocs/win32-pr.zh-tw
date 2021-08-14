---
title: 針對網際網路連線進行疑難排解
description: 在此案例中，使用者嘗試使用 HTTPs 通訊協定流覽至 www.msn.com，但無法連接。 您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fadeefe0413a5a6be5d3ec7f5676ef346e21bc1f4b9e4c3cca026b54d761784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133389"
---
# <a name="troubleshooting-internet-connections"></a>針對網際網路連線進行疑難排解

在此案例中，使用者嘗試使用 HTTPs 通訊協定流覽至 www.msn.com，但無法連接。 您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。

首先，您可以使用 netsh 來啟動追蹤。 輸入 **netsh trace start 情節 = InternetClient tracefile = msn。 etl** 會開始追蹤 InternetClient 案例下啟用的所有提供者，並將結果儲存到名為 msn 的檔案。 使用網頁瀏覽器嘗試連線到 www.msn.com 之後，輸入 **netsh trace stop** 會終止，並相互關聯追蹤檔案。

然後，您可以在網路監視器中開啟 msn 檔案。 事件會依活動識別碼分組在左窗格中。 使用篩選 **描述。包含 ( "msn" )** 只會顯示其通訊協定描述中包含字串 "msn" 的事件。

![使用網路監視器針對網際網路連線進行疑難排解 (1) ](images/internetclient1.png)

接下來，您可以在 [框架摘要] 中檢查事件，以找出看起來相關的事件。 選取事件之後，以滑鼠右鍵按一下並指向 [尋找對話]，然後按一下 [UTEvent] 以選取 UTEvent 層級的交談。

![使用網路監視器針對網際網路連線進行疑難排解 (2) ](images/internetclient2.png)

在左窗格中，會反白顯示相關聯的正規化活動，在此案例中為 UTEvent ActivityID 397。

![使用網路監視器針對網際網路連線進行疑難排解 (3) ](images/internetclient3.png)

藉由使用網路監視器來查看和篩選追蹤資訊，要檢查的事件數目已從1989減少為96。

 

 




