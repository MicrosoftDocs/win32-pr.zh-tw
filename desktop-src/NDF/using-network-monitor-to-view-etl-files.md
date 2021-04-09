---
title: 使用網路監視器來查看 ETL 檔案
description: 網路監視器3.3 可讓使用者使用 Windows Vista 或更新版本) 來剖析、篩選和查看 ETL 檔案 (。
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "103945537"
---
# <a name="using-network-monitor-to-view-etl-files"></a>使用網路監視器來查看 ETL 檔案

[網路監視器 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) 可讓使用者使用 Windows Vista 或更新版本) 來剖析、篩選和查看 ETL 檔案 (。  (如果使用網路監視器3.2，您將需要從 [CodePlex](https://www.codeplex.com/NMParsers) 下載並安裝其他剖析器，才能轉譯網路追蹤事件。 ) 

相互關聯的 ETL 檔案會將相關的事件群組在一起。 下列圖例顯示在網路監視器中開啟的相互關聯檔案，並啟用交談。

![顯示網路監視器的螢幕擷取畫面，其中已醒目提示左側視窗中的相互關聯事件，並從下拉式清單中反白顯示 UTEvent。](images/ut-netmon1.png)

相互關聯事件會依左窗格中的活動分組。 您可以在 [框架摘要] 窗格中選取事件，然後以滑鼠右鍵按一下以選取網路事件層級的交談。 這將會在左窗格中顯示相關的活動。

從左窗格中選取特定活動並展開，將會顯示相互關聯事件的提供者清單。

![顯示網路監視器的螢幕擷取畫面，其中包含從左窗格選取的活動，以及右窗格中對應至該事件的事件。](images/ut-netmon2.png)

當您在左窗格中選取特定提供者時，將會在 [框架摘要] 窗格中顯示該提供者和活動特定的事件清單。

![顯示在左窗格中選取之特定提供者的螢幕擷取畫面，以及右上方窗格中反白顯示的提供者特定事件清單。](images/ut-netmon3.png)

篩選準則可以在網路監視器中套用，讓您更輕鬆地查看並尋找正確的事件或封包。 例如，您可以將篩選套用至選取的錯誤事件 (例如， **UTEvent。 Level = = 2**) 以特定色彩顯示。

![顯示 [編輯色彩篩選器] 對話方塊的螢幕擷取畫面。](images/ut-netmon4.png)

您也可以套用篩選，以不同的色彩標示不同的提供者，以便更輕鬆地查看結果。

![顯示以不同色彩標示的不同提供者範例的螢幕擷取畫面。](images/ut-netmon5.png)

若要套用篩選，請按一下 [**篩選**] 功能表上的 [ **ColorFilters** ]。

下表顯示實用篩選準則的一些範例。



| 篩選                                                                        | Description                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent。 Level = = 2                                          | 只篩選錯誤事件。                                        |
| UTEvent。 Level = = 3                                          | 只篩選警告事件。                                      |
| UTEvent.Header.Descriptor.Id = = 2001                                          | 只篩選事件識別碼為2001的事件。                           |
| WLAN \_ MicrosoftWindowsWLANAutoConfig                                          | 只篩選來自 WLAN 服務的事件。                            |
| N802 \_ MicrosoftWindowsNWiFi                                                   | 只篩選來自原生 Wifi 驅動程式的事件。                  |
| WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG 和 UTEvent.Header.Descriptor.Id = = 2001 | 僅篩選從 WLAN 服務發出的事件識別碼為2001的事件。 |



 

 

 




