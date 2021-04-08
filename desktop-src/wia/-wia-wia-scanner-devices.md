---
description: Windows 映像取得 (WIA) 掃描器裝置會實作為 IWiaItem 物件的階層式樹狀結構。
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: WIA 1.0 中的 WIA 掃描器裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690556"
---
# <a name="wia-scanner-devices-in-wia-10"></a>WIA 1.0 中的 WIA 掃描器裝置

> [!Note]  
> 本主題討論使用 windows 映射取得 (WIA) 1.0 服務 (（Windows XP 或更早的) 所支援）之應用程式的掃描器裝置樹狀目錄。 如需 windows Vista 或更新版本) 所支援的 Windows 映像取得之裝置樹 (WIA) 2.0 (專案的詳細資訊，請參閱 [關於 IWiaItem2 專案樹狀結構](-wia-about-item-tree.md)。

 

Windows 映像取得 (WIA) 掃描器裝置會實作為 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件的階層式樹狀結構。 從根專案，應用程式可能會：

-   查詢掃描器功能
-   設定掃描器裝置屬性
-   控制檔送紙器

WIA 掃描器裝置與 WIA 攝影機裝置不同，因為在一般情況下，它不會將多個映射儲存在記憶體中。

在根專案底下，典型的掃描器物件具有單一 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件，代表裝置的資料收集功能，也就是掃描專案。 此專案已設定 [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) 旗標，以表示可以在此專案上進行資料傳輸。 應用程式會藉由設定掃描專案的屬性來設定掃描，然後執行掃描，並使用資料傳輸介面傳送資料。

下圖說明典型掃描器的 WIA 執行：

![一般掃描器的 wia 執行](images/wiscantr.gif)

典型的雙工掃描器會以 WIA 中的一個 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件來表示。 每個頁面會依序存取一次資料傳輸的上一頁和上一頁資料。 因此，雙工掃描器的表示方式與典型掃描器的標記法相同。

可以在單一掃描工作中掃描多個投影片的投影片掃描器，會將每個個別的影像表示為個別的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件。

下圖說明投影片掃描器的 WIA 標記法：

![投影片掃描器](images/wislscan.gif)

 

 



