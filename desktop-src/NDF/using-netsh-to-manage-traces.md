---
title: 使用 Netsh 來管理追蹤
description: 在 Windows 7 中，您可以從命令提示字元使用 netsh.exe 來啟用和設定網路追蹤。 本節說明一些可協助疑難排解追蹤問題的 netsh.exe 命令，包括新的 netsh 追蹤功能。
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1cf869f60b69e227e78e19e8e05d3765ddb67d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119023"
---
# <a name="using-netsh-to-manage-traces"></a>使用 Netsh 來管理追蹤

在 Windows 7 中，您可以從命令提示字元使用 netsh.exe 來啟用和設定網路追蹤。 本節說明一些可協助疑難排解追蹤問題的 netsh.exe 命令，包括新的 **netsh 追蹤** 功能。 請注意，您必須從提升許可權的命令提示字元執行 netsh 命令。

## <a name="collecting-traces"></a>收集追蹤

案例是預先定義的追蹤提供者集合，可加以啟用以進行疑難排解。 若要顯示可用的網路相關案例清單，請輸入 **netsh trace show 案例** (**netsh trace show provider** 會列出每一個可用的提供者，包括與網路) 無關的提供者。

當您識別出與問題相關的案例時，您可以看到該案例中包含的所有提供者清單。 例如，若要查看在 InternetClient 案例下啟用的所有提供者，請輸入 **netsh trace show 案例 InternetClient**。

您可以針對指定案例或一組案例中的所有提供者啟動追蹤。 例如，若要針對在 InternetClient 案例下啟用的所有提供者啟動追蹤，請輸入 **netsh trace start 情節 = InternetClient**。 若要為多個案例捕捉提供者，您可以指定所有適當的案例，例如 **netsh trace start 情節 = 可共用的案例 = DirectAccess**。 請注意，一次只能啟用一個追蹤會話;在不同的檔案中，不可能同時從不同的提供者集合中捕捉追蹤資訊。

您也可以針對未包含在該特定案例中的其他提供者啟動追蹤。 例如，您可能想要針對在 WLAN 案例和 DHCP 提供者下啟用的所有提供者啟動追蹤。 若要這樣做，請輸入 **netsh trace start 情節 = wlan 提供者 = Microsoft-Windows-Dhcp-Client**。

您也可以輸入 **netsh trace show provider** ，後面接著提供者名稱，以查看特定提供者的更多詳細資料。

若要查看所有可用的選項和篩選，您可以輸入 **netsh trace start/？**。

若要停止追蹤，請輸入 **netsh trace stop**。

## <a name="using-the-output-files"></a>使用輸出檔案

停止追蹤時，預設會產生兩個檔案：「事件追蹤」記錄檔 (ETL) 檔和 .cab 檔。

追蹤事件會收集在 ETL 檔案中，您可以使用網路監視器之類的工具來查看這些事件。 ETL 檔案預設會命名為 nettrace，或者，您可以在啟動追蹤時包含 **tracefile = filename** ，以指定不同的名稱。

.cab 檔案包含有關系統上的軟體和硬體的豐富資訊，例如介面卡資訊、組建、作業系統和無線設定。 除非如上所述指定了其他名稱，否則 .cab 檔案預設會命名為 nettrace.cab。

此 .cab 檔案將包含兩個檔案，這些檔案一律會有相同的名稱。 .Etl 是 nettrace 中所含相同資訊的另一份複本。 report.html 檔案包含追蹤事件和所收集其他資訊的其他資訊。 若要接收最多可用的詳細資料，請在啟動追蹤時，包含命令 **report = yes** 。

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>使用篩選器減少 ETL 追蹤檔中的資料量

當捕捉經過很長一段時間時，ETL 追蹤檔案可能會變得非常大。 在啟用多個提供者的情況下，會產生高流量，ETW 緩衝區條件約束可能會導致某些追蹤被捨棄。 除了這項考慮之外，減少 ETL 追蹤檔中的資料量可讓您藉由減少要檢查的資料量來更輕鬆進行疑難排解。

您可以使用 Netsh 追蹤篩選器來減少 ETL 追蹤檔案的大小。 這些追蹤篩選器是可套用至個別提供者的 ETW 層級和關鍵字。

若要查看可以套用的篩選器清單，請輸入 **netsh trace start/？**

以下是一個篩選準則的範例 **： netsh trace Start InternetClient provider = Microsoft-Windows-TCPIP level = 5 關鍵字 =： ReceivePath，ui： SendPath**。

在此範例中，層級會設為5，這表示會顯示最大事件數目。 下表顯示可用的設定：



| 層級      | 設定              | 描述                                                                           |
|-------|---------------|----------------------------------------------------------------------------|
| 1     | 重大      | 只會顯示重大事件。                                        |
| 2     | Errors        | 將會顯示重大事件和錯誤。                                  |
| 3     | 警告      | 將會顯示重大事件、錯誤和警告。                       |
| 4     | 資訊 | 將會顯示重大事件、錯誤、警告和資訊事件。 |
| 5     | 「詳細資訊」       | 將會顯示所有事件。                                                  |



 

關鍵字 **ReceivePath** 和 Ui **： SentPath** 會篩選事件，只顯示在接收或傳送路徑上追蹤的事件。 輸入 **netsh trace show provider** ，後面接著提供者名稱，即可找到特定提供者的關鍵字完整清單。 例如，輸入 **netsh trace show Provider microsoft-windows-tcpip** 將會顯示有關 MICROSOFT windows tcpip 提供者的資訊，包括關鍵字清單。

Netsh 也支援封包篩選功能 (類似于網路監視器) 當封包捕捉開啟 (時，請設定 **[capture = yes]**) 。 您可以使用封包篩選，在追蹤檔案中捕捉有限數量的封包。 例如， **netsh trace start capture = yes ipv4. address = = x** . x. x，其中 X.X.X.X 是 IP 位址，只會以具有該特定來源或目的地位址的 ipv4 流量來捕捉封包。

如需有關如何使用封包篩選的詳細資訊，您可以輸入 **netsh trace Show capturefilterHelp**。

 

 




